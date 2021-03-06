# Пример надстройки области задач для Excel 2016, позволяющей отслеживать бюджет учебного заведения

Область применения: Excel 2016

Этот пример показывает, как с помощью интерфейсов API JavaScript в Excel 2016 создать надстройку, позволяющую отслеживать бюджет учебного заведения. Надстройка представлена в двух вариантах — для редактора кода и для Visual Studio.

![Пример надстройки, позволяющей отслеживать бюджет учебного заведения](../images/CollegeBudgetTracker_tracker.PNG)

## Проверка
### Версия для редактора кода

Самый простой способ развернуть и проверить надстройку — скопировать манифест в сетевую папку.

1.  Создайте в сетевой папке дочернюю папку (например, \\\MyShare\CollegeBudgetTracker).  
2.  Скопируйте манифест (CollegeBudgetTrackerManifest.xml) в сетевую папку (например, \\\MyShare\MyManifests).
3.  Добавьте общую папку, содержащую этот манифест, в качестве доверенного каталога приложений в Excel.

    А. Запустите Excel и откройте пустую электронную таблицу.  
    
    Б. Откройте вкладку **Файл** и выберите пункт **Параметры**.
    
    В. Выберите пункт **Центр управления безопасностью** и нажмите кнопку **Параметры центра управления безопасностью**.
    
    Г. Выберите элемент **Надежные каталоги надстроек**.
    
    Д. В поле **URL-адрес каталога** введите путь к сетевой папке, созданной на шаге 3, и выберите элемент **Добавить каталог**.
    
   Установите флажок **Показывать в меню** и нажмите кнопку **ОК**. Появится сообщение о том, что параметры будут применены при следующем запуске Office. 
        
4.  Проверьте и запустите надстройку. 

    А. На вкладке **Вставка** в Excel 2016 выберите элемент **Мои надстройки**. 
    
    Б. В диалоговом окне **Надстройки Office** выберите элемент **Общая папка**.
    
    В. Выберите команду **College Budget Tracker** (Надстройка для отслеживания студенческого бюджета) на вкладке Главная. Надстройка откроется в области задач и создаст таблицы и диаграммы на активном листе для отслеживания студенческого бюджета, как показано на схеме. 
      
   ![Пример надстройки, позволяющей отслеживать бюджет учебного заведения](../images/CollegeBudgetTracker_tracker.PNG) 

    Г. Добавьте данные о расходах и доходах с помощью вкладок **Add expenses** (Добавление расходов) и **Add income** (Добавление доходов) и обратите внимание на динамическое изменение данных таблиц и диаграмм.
    
      ![Пример надстройки, позволяющей отслеживать бюджет учебного заведения](../images/CollegeBudgetTracker_taskpane1.PNG) 

Чтобы использовать манифест в собственной надстройке, измените элемент <SourceLocation> в файле манифеста так, чтобы он указывал на общую папку файла Home.html.
    
### Версия для Visual Studio
1.  Скопируйте проект в локальную папку и откройте файл Excel-Add-in-JS-CollegeBudgetTracker.sln в Visual Studio.
2.  Нажмите клавишу F5, чтобы собрать и развернуть пример надстройки. Запустится Excel, а надстройка откроется в области задач справа от пустого листа, как показано на представленном ниже рисунке. 
        
  ![Пример надстройки, позволяющей отслеживать бюджет учебного заведения](../images/CollegeBudgetTracker_tracker.PNG) 

3.  Добавьте данные о расходах и доходах с помощью вкладок **Add expenses** (Добавление расходов) и **Add income** (Добавление доходов) и обратите внимание на динамическое изменение данных и диаграмм.

  ![Пример надстройки, позволяющей отслеживать бюджет учебного заведения](../images/CollegeBudgetTracker_taskpane1.PNG) 


### Подробнее

Интерфейсы API JavaScript в Excel предоставляют существенно расширенные возможности для разработки надстроек. Ниже указаны лишь некоторые из доступных ресурсов. 

1.  [Общие сведения о создании надстроек Excel](https://github.com/OfficeDev/office-js-docs/blob/master/excel/excel-add-ins-programming-overview.md)
2.  [Обозреватель фрагментов кода для Excel](http://officesnippetexplorer.azurewebsites.net/#/snippets/excel)
3.  [Примеры кода надстроек Excel](https://github.com/OfficeDev/office-js-docs/blob/master/excel/excel-add-ins-code-samples.md) 
4.  [Справочник по API JavaScript для надстроек Excel](https://github.com/OfficeDev/office-js-docs/blob/master/excel/excel-add-ins-javascript-reference.md)
5.  [Создание первой надстройки Excel](https://github.com/OfficeDev/office-js-docs/blob/master/excel/build-your-first-excel-add-in.md)
