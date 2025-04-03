FROM python:3.12

WORKDIR /app

COPY . .

RUN pip install poetry

RUN poetry config virtualenvs.create false \
    && poetry install --no-root

EXPOSE 8000

CMD ["poetry", "run", "python", "manage.py", "runserver", "0.0.0.0:8000"]
