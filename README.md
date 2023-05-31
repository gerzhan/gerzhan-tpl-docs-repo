# Шаблон документации для репозитория

- [gerzhan.github.io/gerzhan-tpl-docs-repo](https://gerzhan.github.io/gerzhan-tpl-docs-repo/?utm_source=github&utm_medium=organic&utm_campaign=github_readme&utm_content=github_page&utm_term=v0.0.1)
- [github.com/gerzhan/gerzhan-tpl-docs-repo](https://github.com/gerzhan/gerzhan-tpl-docs-repo)

## Инструкция

- скопируйте код репозитория и распакуйте zip-архив

```bash
# копирование текущей версии структуры документации
$curl -LJO https://github.com/gerzhan/gerzhan-tpl-docs-repo/archive/refs/heads/main.zip
```

- перенесите директорию `docs` в корневую директорию своего репозитория
- замените/удалите в `docs/index.html` блок `Yandex.Metrika counter`
- измените описание документации в конфигурации для `docsify`(window.$docsify) в файле `docs/index.html`
- установите `docsify` на локальной машине

```bash
$npm i docsify-cli -g
```

- добавить в `package.json` команду запуска сервера отображения документации

```diff
"script": {
+ "docs": "docsify serve ./docs -p 4233",
```

- запустите локальный сервер для просмотра(формирования) документации

```bash
$npm run docs
```

## Первоисточники

- [Defining an efficient documentation structure](https://www.iodigital.com/en/history/foreach/defining-an-efficient-documentation-structure)

<div align="center">
<img  title="Markdown" alt="Markdown" height=48 src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/208px-Markdown-mark.svg.png"/>
<img  title="Docsify" alt="Docsify" height=48 src="https://docsify.js.org/_media/icon.svg"/>
</div>
