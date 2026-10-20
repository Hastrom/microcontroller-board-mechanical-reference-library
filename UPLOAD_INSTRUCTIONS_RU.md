# Как опубликовать эту версию на GitHub

Рекомендуется **новый отдельный публичный репозиторий**, например `microcontroller-board-mechanical-reference-library`: существующий `relay-module-stl-reference-library` распространяет другую коллекцию под CC0, тогда как здесь требуется **CC BY-SA 4.0** и отдельная атрибуция. Нельзя механически заменить лицензию CC0 в уже существующем проекте или смешать условия без разграничения.

1. Откройте https://github.com/new под своим аккаунтом. Создайте **пустой** публичный репозиторий `microcontroller-board-mechanical-reference-library` без автоматического README/LICENSE/.gitignore.
2. Скачайте `Microcontroller_Board_STL_STEP_Public_Release_v1_3_RC1.bundle` и сохраните его в папку «Загрузки».
3. Откройте PowerShell в «Загрузках» и выполните:

```powershell
git clone .\Microcontroller_Board_STL_STEP_Public_Release_v1_3_RC1.bundle microcontroller-board-mechanical-reference-library
cd .\microcontroller-board-mechanical-reference-library
git remote set-url origin https://github.com/Hastrom/microcontroller-board-mechanical-reference-library.git
git push -u origin main
```

4. Откройте страницу репозитория и убедитесь, что файлы, `LICENSE`, `THIRD_PARTY_SOURCES.md`, `CATALOG.csv` и модели появились.
5. Перед отправкой рекомендуется проверить ещё раз юридические условия источников и модельные размеры на имеющихся платах. Git Bundle содержит локальную историю, а ZIP — обычные файлы, выберите любой один способ загрузки, не оба сразу.

Важное: при публикации модели станут видимыми третьим лицам. В авторском коммите используется нейтральный placeholder Git; если хотите персонализировать автора, сделайте это самостоятельно в Git перед отправкой.
