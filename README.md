# Astro 快速搭建简单的 web 应用

## sitemap 自动生成

使用方法：替换 `astro.config.mjs`中 site 为项目域名

## github 工作流自动化部署

替换`main.yml`文件下尾行为 Webhook URL

```
curl -X GET https://xxx.com/api/deploy/uJPy7WJ
```

## 数据监控

在 `layout.astro` 文件中替换为新创建的谷歌统计 id

```
    <!-- Google tag (gtag.js) -->
    <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXX"
    ></script>
    <script>
      window.dataLayer = window.dataLayer || [];
      function gtag(...args: any[]) {
        window.dataLayer.push(args);
      }
      gtag("js", new Date());
      gtag("config", "G-XXXX");
    </script>
```
