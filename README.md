# vim for server
<p>cp ~/.vimrc ~/.vimrc_bak</p>
<code>curl https://raw.githubusercontent.com/wqk151/vim/master/vim-for-server > ~/.vimrc</code>

### airline配置
<p>/root/.vim/plugged/vim-airline/doc/airline.txt</p>

### Go 自动补全修复

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

### ale 对Go检查
go vet 单个文件时无法识别同包的自定义类型
将ale卸载重新安装
