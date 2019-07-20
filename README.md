# daeun

# initialize
git clone https://github.com/star16m/daeun.git daeun
git status
git submodule init
git submodule update

# build
cd ${project.root.dir} && docker build --tag 'daeun-image' -f ./docker/Dockerfile .

# run
docker run -d --name daeun -p 9803:9803 -v /Users/star16m/project/hugos/daeun/public:/usr/share/nginx/html:ro daeun-image