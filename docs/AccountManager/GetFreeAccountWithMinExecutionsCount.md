---
layout: docsMember
permalink: docs/AccountManager/GetFreeAccountWithMinExecutionsCount/

categories:
    - Менеджер аккаунтов

title:          GetFreeAccountWithMinExecutionsCount
member:
    type:       method
    name:       GetFreeAccountWithMinExecutionsCount(bool throwExceptionIfNoFreeAccounts, string exceptionMessage)
    summary:    'Возвращает свободный аккаунт с наименьшим количеством запусков.'
    returns:    'Аккаунт.'
    params:
        - name:  throwExceptionIfNoFreeAccounts
          value: 'Если true и все аккаунты заняты, то метод выбросит исключение.'
        - name:  exceptionMessage
          value: 'Сообщение исключения'

---

```csharp
var account = manager.GetFreeAccountWithMinExecutionsCount();
    
if (account == null)
    project.SendInfoToLog("Все аккаунты заняты", true); 
    
project.SendInfoToLog("Логин: " + account.Login, true); 
project.SendInfoToLog("Пароль: " + account.Password, true);
```
