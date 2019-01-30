FROM python:3.6
RUN pip install Flask==1.0.2
RUN useradd -ms /bin/bash admin
USER admin
WORKDIR /app
COPY pyapp /app
CMD ["python", "app.py"]