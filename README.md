# Build
mvn clean package && docker build -t br.edu.ifpb/security-messenger .

# RUN

docker rm -f security-messenger || true && docker run -d -p 8080:8080 -p 4848:4848 --name security-messenger br.edu.ifpb/security-messenger 