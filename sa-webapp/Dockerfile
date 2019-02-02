FROM openjdk:8-jdk-alpine
# Environment Variable that defines the endpoint of sentiment-analysis python api.
ENV SA_LOGIC_API_URL http://localhost:5000
# copy and unpack sentiment-analysis-web-0.0.1-SNAPSHOT.jar under target dir to root / of container
ADD target/sentiment-analysis-web-0.0.1-SNAPSHOT.jar /
# This web app uses port 8080 (for info only) 
EXPOSE 8080
# Execute this commands once we launch/run container
CMD ["java", "-jar", "sentiment-analysis-web-0.0.1-SNAPSHOT.jar", "--sa.logic.api.url=${SA_LOGIC_API_URL}"]
