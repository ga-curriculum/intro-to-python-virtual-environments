<h1>
  <span class="headline">Intro to Python Virtual Environments</span>
  <span class="subhead">Concepts</span>
</h1>


**Learning objective:** By the end of this lesson, you will be able to **implement** a virtual environment for a project with the Python dependencies `pipenv` and **explain** the purpose of `Pipfile` and `Pipfile.lock` files in the `pipenv` environment.

## About

In this short lesson we will discuss what `pipenv` does and how to use it.

## What is a `Virtual Environment`in Python?

A virtual environment in Python is like a separate space where you can work on your Python projects without affecting your computer's main setup. It keeps each project's tools and libraries isolated so they don't interfere with each other or with other programs you're running.

Some reasons we will use virtual environments in our API build:

1. Keep projects codebases separate
1. Make projects easier to share
1. Testing new, experimental libraries

## Installing Dependencies with Pipenv

To use `pipenv`, create a new Python project folder and navigate to it.

Now rather than using `pip` to install dependencies for an application, you can use `pipenv`.


For example:

```sh
pipenv install fastapi
```

This will automatically create two key files: `Pipfile` and `Pipfile.lock`. These are used to keep track of the project's dependencies and their versions. It is designed to declare broad dependencies in a more manageable way.

## Pipfile

The `Pipfile.lock` is automatically updated each time the `Pipfile` changes. It's a snapshot of the exact versions of each package being used, along with their transitive dependencies, at a specific point in time. This means that if you share your project with someone else, you can guarantee they will install exactly the same dependencies as you have, ensuring consistent behavior across different environments. Keep both of these files in version control. Visit the [pipenv documentation](https://pipenv.pypa.io/en/latest/pipfile.html) for more details on the differences between `Pipfile` and `Pipfile.lock`.

Using `pipenv` to install your packages means that you can collaborate on projects, simply clone or download the repo and type `pipenv install` to install all the dependencies.

## How It Works

When you install a package with `pipenv`, it creates a _virtual environment_ for that project. This mimics a development environment where only the packages you have installed for that project exist. It does this by installing all the packages to a uniquely named folder somewhere in the file system of your laptop.

## Testing Pipenv

In the current working directory as your virtual environment, create a file called `main.py` and save the following simple code in it:

```py
# main.py

print("pipenv is working!")
```

In order to have Python execute the `main.py` file in the virtual environment, you need to prefix any command with `pipenv run` So for example:

```sh
pipenv run python main.py
```

Confirm that you see the message `pipenv is working!`.

