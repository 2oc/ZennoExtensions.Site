---
layout: docsMember
permalink: docs/BrowserManager/Load/

categories:
    - Настройка браузера

title:          Load
member:
    type:       method
    name:       Load(string path)
    summary:    'Загружает объект профиля браузера, сохраненный в файл.'
    returns:    'Профиль браузера'
    params:
        - name:  path
          value: 'Путь к файлу.'

---

```csharp
// Загружаем из файла
string profile = BrowserManager.Load("C:\\Zenno\\Profiles\\1.txt");

// Применяем к ZennoPoster'у
BrowserManager.Setup(profile, instance, project);
```
