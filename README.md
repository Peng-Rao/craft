## 简介

`Vue3` + `Djangorestframework` 前后端分离社交网站。主要包括**博文内容管理、用户管理、消息推送、聊天等功能**。

博文：

![image-20231030101001890](https://rao-picgo-1307731364.cos.ap-nanjing.myqcloud.com/image-20231030101001890.png)

聊天系统：

![image-20231030101821377](https://rao-picgo-1307731364.cos.ap-nanjing.myqcloud.com/image-20231030101821377.png)

## 前端

核心框架：`Vue3`、`Vue Router`、`pinia`，UI 主要由 `tailwindcss` 构建。

## 后端

核心框架：`djangorestframework`，主要使用 `simplejwt` 进行 `token` 授权，使用`drf-spectacular` 进行文档管理。

## 开发环境

### 后端启动

1. 克隆本项目 `https://github.com/Raopend/craft.git`
2. 安装相关依赖：

```python
cd craft_backend
pip install -r requirements.txt
```

3. 执行数据库迁移

```shell
python manage.py makemigrations
python manage.py migrate

# 如需创建 superuser 则需要在 shell 中创建
python manage.py shell
from accounts.models import User
User.objects.create_superuser(name, email, password)
```

4. 启动服务

```python
python manage.py runserver
```

## 前端启动

1. 安装相关包

```
cd craft_frontend
npm install
```

2. 启动

```
npm run serve
```

