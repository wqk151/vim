### 修改vimrc
```
cp ~/.vimrc ~/.vimrc_bak
curl https://raw.githubusercontent.com/wqk151/vim/master/vimrc-server > ~/.vimrc
```

### airline配置

参考:/root/.vim/plugged/vim-airline/doc/airline.txt

### Go 使用YCM自动补全修复

```
cd ~/.vim/bundle
git clone git@github.com:Valloric/YouCompleteMe.git
cd YouCompleteMe
git submodule update --init --recursive
python install.py --go-completer
cd third_party/ycmd/third_party/
rm -rf gocode
git clone https://github.com/nsf/gocode.git
cd gocode
go mod init
go build .
```

### ale 对Go语法检查

```
go vet 单个文件时无法识别同包的自定义类型
将ale卸载重新安装
```
