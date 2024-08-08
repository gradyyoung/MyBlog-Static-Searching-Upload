> 用于推送我的网站至algolia建立索引：https://www.ygang.top/


algolia官网：https://www.algolia.com/

algolia后台：https://dashboard.algolia.com/

使用的ui框架：https://docsearch.algolia.com/docs/api

# 手动推送

mac 需要有docker环境和homebrew
注意：需要在`.env`中填写自己的key

```shell
# 安装jq
brew install jq

# 运行dockerrun.sh脚本
docker run -it --env-file=.env -e "CONFIG=$(cat docsearch-config.json | jq -r tostring)" algolia/docsearch-scraper
```

# github action推送
参考`.github/workflows/MyBlog-Static-Searching-Upload.yml`文件进行配置

 
