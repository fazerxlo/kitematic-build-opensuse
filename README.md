#kitematic-build-opensuse#

Script to build kitematic on openSUSE:Build Service


##Manual build procedure openSUSE 15.0##

**Prerequisities RPM**

*	make
*	aj
*	git


**Prerequisities installed by procedure**

*	nvm
*	nodejs
*	npm
*	npm packages (a lot of them)


**Build Procedure**

	git clone https://github.com/docker/kitematic.git
	
	cd kitematic
	curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.30.1/install.sh | bash
	. ~/.nvm/nvm.sh
	export NVM_DIR="$HOME/.nvm"
	[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm
	
	nvm install 6.16.0
	nvm alias default v6.16.0
	
	make

**Run application**

	npm start

**Build RPM**

	npm install grunt grunt-cli
	npm run release:redhat:x64

**TODO**

*	spec file
*	manual rpm creation by rpmbuild


**Links**

[https://en.opensuse.org/openSUSE:Build_Service_Tutorial](https://en.opensuse.org/openSUSE:Build_Service_Tutorial)
[https://rpm-packaging-guide.github.io/](https://rpm-packaging-guide.github.io/)
[https://en.opensuse.org/openSUSE:Packaging_nodejs](https://en.opensuse.org/openSUSE:Packaging_nodejs)

