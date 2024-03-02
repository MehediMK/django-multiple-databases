# Library Project

This is a Django project for managing a library app. It demonstrates how to configure multiple databases using database routing.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

- Python 3.x
- Django

### Installing

1. Clone the repository:

   ```bash
   git clone https://github.com/MehediMK/django-multiple-databases.git
   ```

2. Navigate into the project directory:

   ```bash
   cd library_project
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Apply migrations:

   ```bash
   python manage.py migrate
   ```

5. Run the development server:

   ```bash
   python manage.py runserver
   ```

6. Visit `http://127.0.0.1:8000/` in your browser to access the application.

## Built With

- [Django](https://www.djangoproject.com/) - The web framework used


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.


**Dockerfile:**

```Dockerfile
# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set the working directory in the container
WORKDIR /code

# Copy the current directory contents into the container at /code
COPY . /code/

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Run the Django development server
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
```