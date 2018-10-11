FROM tensorflow/tensorflow:1.9.0

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 5000

ENV FLASK_APP ./app.py
ENV FLASK_DEBUG=1

# CMD [ "python", "flask run", "--host=0.0.0.0" ]
CMD [ "python", "app.py" ]

#FLASK_APP=app.py FLASK_DEBUG=1 python -m flask run
# docker run -p 5000:5000 detect_image:Dockerfile