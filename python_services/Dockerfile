FROM python:3.12

WORKDIR /app

COPY requirements.txt requirements.txt
RUN pip install --upgrade uv
RUN uv pip install --system -r requirements.txt
COPY ./app .
COPY ./data ./data
# fetch the llm from huggingface
COPY ./bin .
RUN python fetch_recs_llm.py

