# 偃师

周穆王西巡狩，越昆仑，不至弇山。反还，未及中国，道有献工人名偃师。穆王荐之，问曰：“若有何能？”偃师曰：“臣唯命所试。然臣已有所造，愿王先观之。”穆王曰：“日以俱来，吾与若俱观之。”翌日偃师谒见王。王荐之，曰：“若与偕来者何人邪？”对曰：“臣之所造能倡者。”穆王惊视之，趋步俯仰，信人也。巧夫！领其颅，则歌合律；捧其手，则舞应节。千变万化，惟意所适。王以为实人也，与盛姬内御并观之。技将终，倡者瞬其目而招王之左右侍妾。王大怒，立欲诛偃师。偃师大慑，立剖散倡者以示王，皆傅会革、木、胶、漆、白、黑、丹、青之所为。王谛料之，内则肝胆、心肺、脾肾、肠胃，外则筋骨、支节、皮毛、齿发，皆假物也，而无不毕具者。合会复如初见。王试废其心，则口不能言；废其肝，则目不能视；废其肾，则足不能步。穆王始悦而叹曰：“人之巧乃可与造化者同功乎？”诏贰车载之以归。
夫班输之云梯，墨翟之飞鸢，自谓能之极也。弟子东门贾、禽滑釐闻偃师之巧以告二子，二子终身不敢语艺，而时执规矩。

偃师是《列子·汤问》中记载的一位工匠，善于制造能歌善舞的人偶。

## 构建

- debug版本：`make`
- release版本：`make build=release`

## 运行

在某个`$PATH`目录中添加`build/yanshi`的symbolic link。

`yanshi a.ys -o a.cc`

## 语法

### 支持`:`，兼容ANTLR很多语法

## contrib

### Vim

语法高亮、Synaptics编辑时检查错误

```zsh
ln -sr contrib/vim/compiler/yanshi.vim ~/.vim/compiler/
ln -sr contrib/vim/ftdetect/yanshi.vim ~/.vim/ftdetect/
ln -sr contrib/vim/ftplugin/yanshi.vim ~/.vim/ftplugin/
ln -sr contrib/vim/syntax/yanshi.vim ~/.vim/syntax/
ln -sr contrib/vim/syntax_checker/yanshi ~/.vim/syntax_checker/
```

### Zsh

命令行补全

```
# ~/.zshrc
fpath=(~/.zsh $fpath)

# ln -sr contrib/zsh/_yanshi ~/.zsh/
```

## 源文件

```
src
  common.{cc,hh}
  main.{cc,hh}
  syntax.{cc,hh}
  loader.{cc,hh}
  fsa.{cc,hh}
  fsa_anno.{cc,hh}
  compiler.{cc,hh}
  parser.y
  lexer.l
  location.cc
```

## 原理
