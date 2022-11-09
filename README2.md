docker build -t stocks_products .
docker images
docker run --name stocks stocks_products
docker run --name stocks -d stocks_products
docker run --name stocks -p 8000:8000 stocks_products
docker volume create stocks
docker volume ls
docker run --name stocks -p 8000:8000 -v stocks:/app/ stocks_products
