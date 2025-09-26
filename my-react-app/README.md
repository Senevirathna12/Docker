# create new image

docker build -t image-new .


# create volume corectly for track the file updating

docker run --name react-container-new -p 4000:3000 --rm `
  -v /app/node_modules `
  -v ${pwd}:/app `
  -e CHOKIDAR_USEPOLLING=true `
  -e WATCHPACK_POLLING=true `
  image-new
