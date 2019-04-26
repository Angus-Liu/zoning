# 更新日志

## [ⅴ2.0.18] - 2019-04-26
- 2018 年数据发布，对应`npm`版本号为`v2.0.18`
- 爬取的站点有速率限制，需间隔时间爬取
- 目前未实现爬取完自动弹出下载，需要手动调用下载方法

## 2019-04-16
- 重新发布 `npm zoningjs`，包含`zoning-3.json`、`zoning-4.json`

## [ⅴ2.0.0] - 2019-01-28
- 修复已知Bug，存在相同层级节点ID长度不一致的问题
    - `4413` 节点的子节点为 `441302`、`441303`等，为6位数，基本上都是6位数
    - 而存在少数的情况，非6位数，而是直接9位数
    - 如 `4419` 的下一级是 `441900001`、`441900002`等，为9位数
    - 取前6位造成节点ID重复，且对应的子数据未抓取到
    - 是在设置ID为主键时，提示有重复数据而发现的问题