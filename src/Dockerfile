FROM zhu327/gemini-openai-proxy:latest
COPY ./ /app
WORKDIR /app
RUN mkdir -p /tmp/app
RUN cp gemini /tmp/app && chmod +x /tmp/app/gemini
CMD ["/app/gemini"]
CMD ["gunicorn", "--bind", "0.0.0.0:5000", "run:app"]
