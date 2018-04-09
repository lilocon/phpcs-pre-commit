# pre-commit


# 使用方法

将pre-commit文件copy到.git/hooks目录即可


# 配合composer使用


将pre-commit文件copy到composer.json所在目录

在composer.json中添加以下代码
```
        "post-install-cmd": [
            "php -r \"copy('pre-commit', '.git/hooks/pre-commit');  chmod('.git/hooks/pre-commit', 0755);\""
        ],
        "post-update-cmd": [
            "php -r \"copy('pre-commit', '.git/hooks/pre-commit');  chmod('.git/hooks/pre-commit', 0755);\""
        ]
```