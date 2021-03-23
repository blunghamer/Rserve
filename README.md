# Contribute

## clone repo

Java client uses a submodule, so clone into this as well

`git clone --recurse-submodules https://github.com/s-u/Rserve`

`
git submodule init
git submodule update
`

# Develop

## Build in tree (not recommended)

This pollutes the source tree with configure artefact use mkdist -r / mkduir -i

`
aclocal -I m4
autoheader
autoconf
## this should not be necessary since we don't use
## automake but a bug in autoconf 2.69 requires
## automake files even though they are not used
automake -ac 2>/dev/null 
touch shtool
rm -rf autom4te* aclocal*
`

## Install Locally

`
bash mkdist -i
`

## Check 

`
bash mkdist -c
`

## Make Distribution

`
bash mkdist 
`

## Clean

`
rm -rf autom4te* aclocal*
` 