# init
`repo init -u https://github.com/yEsPaP/ndk_manifest -b master -m default.xml`

# sync:
`repo sync -c -j$(nproc --all) --no-tags --no-clone-bundle --optimized-fetch --prune`

# build:
set python2 to default:

`rm /usr/bin/python`

`ln -s /usr/bin/python2.7 /usr/bin/python`

build

`python ndk/checkbuild.py --no-build-tests`
