export NODE_HOME=/opt/node-v24.2.0-linux-x64

export PATH=$PATH:$NODE_HOME/bin
which node
echo npm is `npm -v`

if [ -d fab_group_deps.ts.adligo.org ]; then 
  rm -fr fab_group_deps.ts.adligo.org
fi


git clone https://github.com/adligo/fab_group_deps.ts.adligo.org
cd fab_group_deps.ts.adligo.org
npm i

echo now setup your COMMON_FAB_NODE_MODULES environment variable in the fab_group.ts.adligo.org
dir=`pwd`
echo projects Jenkins build to $dir/node_modules


