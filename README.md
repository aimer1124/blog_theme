# blog_theme

- Modified from `theme`: [https://github.com/tufu9441/maupassant-hexo.git](https://github.com/tufu9441/maupassant-hexo.git)。

## 调整项

### 添加页脚中站点的访问数量

- 删除`post.jade`中的`busuanzi`js引用

- 添加`footer.jade`中的数据显示
```
| Total
if theme.busuanzi == true
  span#busuanzi_container_site_pv
    span= ' '
    span(rel='nofollow')#busuanzi_value_site_pv
    span(rel='nofollow')= ' ' + __(' hits, ')
  span#busuanzi_container_site_uv
    span(rel='nofollow')#busuanzi_value_site_uv
    span(rel='nofollow')= ' ' + __(' vistors.')
```

- 添加`after_footer.jade`中`busuanzi`的引用

```
if theme.busuanzi == true
  script(src='https://dn-lbstatics.qbox.me/busuanzi/2.3/busuanzi.pure.mini.js', async)
