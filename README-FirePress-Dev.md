## Set your local dev environment

- Update ENV `theme_path`
- It assumes that you use [nvm](https://github.com/nvm-sh/nvm) to manage node versions.

```
theme_path="/Volumes/960G/_pascalandy/11_FirePress/Github/firepress-org/Casper"
#
## set node version
cd ${theme_path} && \
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"
#
#nvm install v12.18.4 &&\
#nvm use v12.18.4 &&\
#
nvm install 'lts/*' --reinstall-packages-from=current &&\
nvm use --lts &&\
nvm install-latest-npm &&\
node --version;
```

## update your theme

```
yarn install &&\
yarn dev;
```

## compile your theme
```
## compile your theme
yarn test:ci &&\
yarn test &&\
yarn pretest &&\
yarn test &&\
yarn zip &&\
cd dist && echo; pwd; echo; ls -AlhF; echo; du -sh;
```