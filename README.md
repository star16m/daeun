# daeun

# build
cd ${project.root.dir} && docker build --tag 'daeun-image' -f ./docker/Dockerfile .

# run
docker run -d --name 'daeun' -p 9803:9803 daeun-image
