# Press.one Docs 

## 本地编辑及预览(热更新)
```
yarn install;
yarn start;
```

## 文档结构
* 每个子文件夹相当于一个子路径。_sidebar.md 用于定义当前路径的目录，_navbar.md 用于定义当前路径的导航内容。如果当前路径不包含，则沿用父级目录的相应文件，直至项目根路径。
* 除了根目录入口文档被设置成了 index.md 外，其余路径如果文档皆为默认 README.md 文件。
```.
└── docs
    ├── index.md
    ├── README.md
    ├── other.md
    ├── _sidebar.md
    ├── _navbar.md
    └── flying-pub
        ├── README.md
        ├── other.md
        └── _sidebar.md
```
那么对应的访问页面将是
```
docs/index.md              => https://docs.prsdev.club
docs/other.md              => https://docs.prsdev.club/#/other
docs/flying-pub/README.md  => https://docs.prsdev.club/#/flying-pub/
docs/flying-pub/other.md   => https://docs.prsdev.club/#/flying-pub/other
```
* 文档需要设置一级或二级标题才可被本地搜索索引，该索引缓存在浏览器本地，有效期为默认的一天。也就是说，更新文档后至多需要一天搜索功能才能跟上，也可手动删除 localstorege 刷新后重新生成本地索引。
