{% if cookiecutter.template == "vision" -%}
FROM waggle/plugin-base:1.1.1-ml
{%- elif cookiecutter.template == "usbserial_sensor" -%}
FROM python:3.11
{%- elif cookiecutter.template == "minimal" -%}
FROM python:3.11
{%- elif cookiecutter.template == "tutorial" -%}
FROM waggle/plugin-base:1.1.1-ml
{%- endif %}

WORKDIR /app

COPY requirements.txt .
RUN pip3 install --no-cache-dir -r requirements.txt

COPY . .

ENTRYPOINT ["python3", "main.py"]
