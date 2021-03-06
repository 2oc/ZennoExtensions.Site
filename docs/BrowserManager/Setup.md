---
layout: docsMember
permalink: docs/BrowserManager/Setup/

categories:
    - Настройка браузера

title:          Setup
member:
    type:       method
    name:       Setup(ZennoExtensions.BrowserManager.Model.Profile profile, Instance instance, IZennoPosterProjectModel project)
    summary:    'Применяет конфигурацию к ZennoPoster&lsquo;y.'
    returns:    'void'
    params:
        - name:  profile
          value: 'Профиль браузера.'
        - name:  instance
          value: 'Экземпляр <see cref="T:ZennoLab.CommandCenter.Instance" />'
        - name:  project
          value: 'Экземпляр <see cref="T:ZennoLab.InterfacesLibrary.ProjectModel.IZennoPosterProjectModel" />'

---

```csharp
// Создаем объект правил генерации
var generationRules = new GenerationRules();

// Указываем чтобы использовался случайно Firefox или Chrome
generationRules.BrowserType = BrowserType.GoogleChrome | BrowserType.MozillaFirefox;

// Генерируем профиль браузера
var profile = BrowserManager.Generate(generationRules);

// Применяем к ZennoPoster'у
BrowserManager.Setup(profile, instance, project);
```
