# Желтая книга Morpheus

В этом документе описываются технические детали полной ноды Morpheus, смарт-контракта Morpheus и связанных с ними доказательств. Представлено в том виде, в котором это было написано в Белой книге, подготовленной анонимными разработчиками Morpheus, Trinity и Neo. 
Ссылка на статью здесь: https://github.com/SmartAgentProtocol/SmartAgents/blob/main/MorpheusWP.md 

## Локальная версия Morpheus 0.0.5 уже доступна на:
---------
**Версия Morpheus 0.0.5 для Mac**
- Скачать с Google Drive: https://drive.google.com/file/d/1x-wR4HWjKqT_g6VRjrWPXu3rVm9ukOc9/view?usp=sharing
- SHA 256 хэш для проверки: 9092d543023fb95086cf4a7039d42cbcbbdf5283d670c4de6396b3d89e57b064
- Версия: Morpheus-0.0.5-x64.dmg

---------
**Версия Morpheus 0.0.5 для Linux Debian**
- Скачать: https://drive.google.com/file/d/1PQ3n7LXeJHe_jmkYLDUQ9fWjZQTWbHCB/view?usp=sharing
- Инструкция: Для установки выполните эту команду:
sudo dpkg -i /path/to/your/morpheus.deb
ПРИМЕЧАНИЕ: В приведенной выше команде замените "/path/to/your/morpheus.deb" на ваш путь к файлу morpheus_0.0.5_amd64.deb file.
- SHA -хэш для проверки:
b227e7bcb21ec9e8e2b4bf9510a2e1f224953fe5
Версия: morpheus_0.0.5_amd64.deb
---------

Первое взаимодействие с Morpheus 22 октября 2023 года.
![FirstInteractionWithMorpheus20231022](https://github.com/MorpheusAIs/Morpheus/assets/1563345/35509f3a-4346-4f58-bb60-f7881fd10f7e)

## Смарт-контракты Morpheus
Ончейн действия, которые должны быть подтверждены смарт-контрактом Morpheus.

1. Форк смарт-контракта N2 Yield развернутый на Arbitrum
- A) Блокировка ETH через Thorchain, пожертвование дохода кодерам + провайдерам вычислений.
- B) Рассчет пропорционально пожертвованных ETH 

2. Вечное доказуемое уничтожение MOR:
- A) Адрес сжигания или функция сжигания токенов MOR.

3. ERC20 образец контракта на выпуск MOR
- A) Токены MOR ежедневно выпускать для Капитала + Сообщества пропорционально пожертвованной доходности ETH.
- B) Токены MOR ежедневно минтить для Кодеров + Провайдеров вычислений пропорционально сожженному MOR через комиссиии.

4. Доказательство Morpheus - демонстрация конфиденциальности, открытого кода и безопасности
- A) Публикация списка аудированных Агентов и их Smart Rank оценки.
- B) Публикация списка аудированных LLM и их Smart Rank оценки.
- C) Публикация списка смарт-контрактов и их Smart Rank оценки.
- D) Публикация списка Подсказок и их Smart Rank оценки.

5. Защитные средства
- A) Выплата MOR и ETH в случае взлома, ошибок, багов или других атак, которые приводят к убыткам.
- B) Заранее определенный набор сценариев для выплат. Политика форков/откатов в экстремальных случаях.
- C) Разработчики отвечают за определение случаев атак и их устранение. 
- D) Фонды для вознаграждения за баги / белым хакерам.
- E) Фонды для защиты от национальных государственных игроков.

## Схемы смарт-контракта Morpheus
Схемы и описания минта и сжигания MOR.
Описания необходимых смарт-контрактов.
Диаграммы с подробным описанием распределения ETH. 

### Распределение вознаграждений MOR смарт-контрактом Morpheus
![new-buckets](https://github.com/SmartAgentProtocol/SmartAgents/assets/76454555/cd57bae7-2a56-4a55-bf3e-1f810f3fba9c)

### Пример распределения токенов MOR в 1й день и 2й день.
![Untitled spreadsheet - Google Sheets 2023-10-15 13-28-08](https://github.com/MorpheusAIs/Morpheus/assets/76454555/6ff7869d-bbd6-46b5-8673-6a59b75906e1)

## Пример расчета распределения для вкладчика адреса 0x123 ETH

### Первый этап
![Diagram1ofETHDontator](https://github.com/SmartAgentProtocol/SmartAgents/assets/1563345/fead528c-d628-449e-a3a3-2f53904f4a3d)

### Второй этап
![ETHGivenDiagram2](https://github.com/MorpheusAIs/Morpheus/assets/1563345/915020e8-d342-48bc-85ee-367de0325680)

### Третий этап
![Diagram3ForETHGiven](https://github.com/MorpheusAIs/Morpheus/assets/1563345/a3f455af-56de-4c6b-9688-5b9e91673e5a)

## Пример расчета распределения поставщика вычислений с адресом 0x123

### Первый этап
![MORForCompute](https://github.com/SmartAgentProtocol/SmartAgents/assets/1563345/bef69c69-0420-441f-97f0-7e8195844f57)

### Второй этап
![MORForCompute2](https://github.com/SmartAgentProtocol/SmartAgents/assets/1563345/a6f30da5-5441-4f0a-be80-c5798f5920cd)

### Круговая диаграмма распределения токенов MOR
![mordist](https://github.com/MorpheusAIs/Morpheus/assets/76454555/4157efe7-6abf-404a-87f9-a8dc76cd4799)

## Инструменты разработчика и технический стек Morpheus.
- Llama2 - надежный LLM с открытым исходным кодом, запускаемый локально.
- Ollama - пак для простой установки Llama2.
- LangChain - инструмент разработчика для подключения LLM к векторным хранилищам и API.
- LangSmith Editor - низкоуровневый код для создания агентов на LangChain.
- SmartContractRank Algorithm - подбор смарт-контрактов для пользователя на основе его намерений.
- AgentRank Algorithm - создание специализированных агентов для выполнения действий пользователя.
- PromptRank Algorithm - создание подсказок для пользователей на основе прогнозируемого намерения/действия.
- Filecoin - хранение данных и предоставление облачных вычислений.
- Akash Network - открытая вычислительная сеть для запуска LLM-агентов.
- Wallets - Shapeshift, Exodus, другие варианты с открытым исходным кодом.

## Схема полной ноды Morpheus для агента / LLM для действий Web3. 
Аудиты агентов, проводимые кодерами, генерирующими "доказательство агента", что заявленные функции агента соответствуют представленным. И, конечно, не содержит вредоносного кода.

Место для описания процесса аудита, кто может проводить аудит и как сертифицировать его результаты. А также стимулы, выплачиваемые аудиторам.

Доказательство вычислений, генерируемое в момент взаимодействия с пользователем и показывающее выражеаемое намерение, совпадает с выбором смарт-контракта и подтвержденные пользователем стоимости транзакций. 

## Схема пользователей и контрибьюторов Morpheus
![Morpheus User   Contributor Diagram](https://github.com/MorpheusAIs/Morpheus/assets/1563345/2cff8d70-c116-472f-a431-8a82bfa22f9b)

### Схема, показывающая UX поток от запроса пользователя до подтверждения Web3 действия.
![UX flow for prompted web3 tasks and ticketing](https://github.com/MorpheusAIs/Morpheus/assets/76454555/942b20fb-d67e-4a57-af2c-cd24a89690a5)

### Схема, показывающая версию Morpheus уствновленную локально.
![MorpheusLocalDiagram](https://github.com/SmartAgentProtocol/SmartAgents/assets/1563345/a0564914-cddb-42e4-b0f4-8c2310db6a66)

### Схема, показывающая уствноленную версию Morpheus P2P.
![MorpheusP2PDiagram](https://github.com/SmartAgentProtocol/SmartAgents/assets/1563345/a7eeb31f-3d38-4233-a45f-e9b91ad84ba2)

### Схема, показывающая децентрализованную версию Morpheus.
![MorpheusDecentralized](https://github.com/SmartAgentProtocol/SmartAgents/assets/1563345/1699f2de-cc18-42e8-a05c-32b3307baa20)

## Сообщество
- Смарт-Агенство - Разработчики-фрилансеры, создающие сценарии использования / агентов для пользователей Morpheus.
- Глобальное сообщество разработчиков - Растущее сообщество разработчиков, стартапов и пользователей.
- Сообщество набирает держателей ETH для пожертвования доходности разработчикам, вычислителям и сообществу Morpheus.
- Распределенная группа разработки - Разработчики смарт-контрактов для кодирования смарт-контракта Morpheus.
- Morpheus Dapps - Платформа для интеграции Morpheus со смарт-агентом пользователя.