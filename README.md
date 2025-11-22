# Шаблон документации для репозитория

- [gerzhan.github.io/gerzhan-tpl-docs-repo](https://gerzhan.github.io/gerzhan-tpl-docs-repo/?utm_source=github&utm_medium=organic&utm_campaign=github_readme&utm_content=github_page&utm_term=v0.0.1)
- [github.com/gerzhan/gerzhan-tpl-docs-repo](https://github.com/gerzhan/gerzhan-tpl-docs-repo)

## Инструкция

### Копирование шаблона

- скопируйте архив из удаленного репозитория и распакуйте zip-архив локально в своем репозитории

```bash
# копирование текущей версии шаблона документации для репозитория(проекта)
$curl -LS https://github.com/gerzhan/gerzhan-tpl-docs-repo/archive/refs/heads/main.zip -o docs-tpl.zip
# распаковка только директории с документацией в корне собственного репозитория
$unzip ./docs-tpl.zip 'gerzhan-tpl-docs-repo-main/docs/*' -d './docs'
$mv ./docs/gerzhan-tpl-docs-repo-main/docs/* ./docs/
$rm ./docs/gerzhan-tpl-docs-repo-main/docs/
# удалить архив
$rm docs-tpl.zip
```

### Первичная настройка шаблона

- замените/удалите файл `docs/README.md`
- замените/удалите в `docs/index.html` блок `Yandex.Metrika counter`
- измените описание документации в конфигурации для `docsify`(window.$docsify) в файле `docs/index.html`
- установите `docsify` на локальной машине глобавльно или добавьте в корневой `package.json`

```bash
# установить глобально
$npm i docsify-cli -g
# установить локально
$npm i -D docsify-cli
```

- добавить в `package.json` команду запуска сервера отображения документации (при необходимости изменить порт `4233` на другой доступный)

```diff
"script": {
+ "docs": "docsify serve ./docs -p 4233",
```

### Локальный запуск разработки документации

- запустить локальный сервер для формирования и просмотра документации

```bash
$npx run docs
```

## Примечание

Вы можете изменить имя директории с `docs` на любое другое имя (_docs, 'repodocs' и т.п.). Использование имени `docs` позволят настроить [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#troubleshooting-publishing-from-a-branch) для этой директории.

## Первоисточники

- [Defining an efficient documentation structure](https://www.iodigital.com/en/history/foreach/defining-an-efficient-documentation-structure)

<div align="center">
<img  title="Markdown" alt="Markdown" height=48 src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/208px-Markdown-mark.svg.png"/>
<img  title="Docsify" alt="Docsify" height=48 src="https://docsify.js.org/_media/icon.svg"/>
</div>
