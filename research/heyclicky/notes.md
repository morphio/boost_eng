# HeyClicky: разбор записи экрана (23,7 мин, без звука)

Источник: `heyclicky.mp4`, 30 контактных листов и несколько кадров в полном размере. На машине установлены Wispr Flow, Krisp, Cluely, VoiceOS. Всё, что описано ниже, относится к HeyClicky, если не оговорено иное. Догадки помечены «(предп.)».

## 1. Процесс по шагам

- **0:00–0:17. Запуск из /Applications.** Открывается тёмное окно-карточка «Welcome to HeyClicky. A tiny AI buddy that lives on your Mac.» с синей кнопкой Play и пилюлей «Sign in with Google». Сайт heyclicky.com показывает демо «heyclicky, find 10 tiktok creators…» → «on it!» под заголовком «spawn agents with your voice».
- **0:17–0:36. Вход.** Google OAuth через Supabase, в согласии приложение называется «Clicky». Дальше страница `api.heyclicky.com/auth-callback` с текстом «You're signed in. HeyClicky should be open now. You can close this tab.» и кнопкой «Open HeyClicky», затем системный диалог Chrome «Open HeyClicky?». Остальной онбординг идёт в тёмной карточке поверх этой веб-страницы.
- **0:37–1:00. Анкета.**
  - «How'd you find this? We're a tiny team, and knowing where you heard about us helps a ton.» Чипы с иконками: Instagram Ad … ChatGPT, Claude, A friend, Other.
  - «Pick the style you like»: персонаж Dreamy Cloud (облачко с глазами ^ ^) или Puff Pals.
  - «Pick a color — Click one to bring me to life. Choose wisely.» Четыре точки: красная, синяя, жёлтая, зелёная.
- **~1:05–2:05. Разрешения.** Приложение «переезжает в чёлку»: чёрная панель выезжает из notch.
  - «Hi, Alexandr. I'm HeyClicky.», затем «I live in your notch now. Need permissions to get started.» [Let's start].
  - Accessibility: «I need accessibility permissions. Click Open System Settings when Mac asks.» [Waiting…], затем «Drag me into the Accessibility list.» [Open]. Внизу окна System Settings висит плитка «I'm HeyClicky — drag me into the list above.», которую можно перетащить в список.
  - Screen & System Audio Recording: системное «Quit & Reopen», затем в чёлке «Got it! Screen Recording is ready.» [✓ Granted]. Следом «Complete screen access. Click Grant Access to verify screen capture…» и системный запрос «bypass the system private window picker».
  - Финал: «All set. Turn your sound on and tap the button below.» [Meet HeyClicky]. Прогресс показан тремя чёрточками-степперами.
- **2:09–4:00. Знакомство.** Рядом с курсором появляется **зелёный треугольник-курсор** (выбранный цвет) с подписью-пилюлей «hi, im heyclicky». За курсором следует плавающее видео основателя (~180×100, скругления, полоса прогресса, таймер «58s»). Приложение само открывает spacex.com (подпись «Researching your competitors now.»), а затем черновик Gmail на hi@heyclicky.com: «jk my twitter dm's got way too crazy, so email me here».
- **4:25–16:42. Интерактивный тур** (точки-пейджер, «Back», «Skip demo», иконка ноты для звука):
  1. «First, can I hear you? Say anything out loud. If the bars dance, your mic works… Bluetooth ones get flaky.» Показаны эквалайзер-бары, пилюля «"Testing, testing, 1, 2, 3"» и выбор «MacBook Air Microphone». Ответ у курсора: «loud and clear ٩(◕‿◕)۶».
  2. «This is how you talk to me. Hold the keys down… I'm listening the whole time you hold them.» Клавиши ⌃ control + ⌥ option рисуются как keycaps и подсвечиваются зелёным при нажатии. Пример фразы: «"My name is Alexandr"».
  3. «I'm curious about you. Four quick questions…» Это голосовое интервью с маскотом-облаком: персиковые пузыри реплик, пилюля-состояние «Listening… release to send» / «HeyClicky is speaking…», рядом поле «Or type here». Пользователь рассказал про инструмент для учителей английского, и бот ответил «That sounds like a thoughtful quality boost for teachers and their students».
  4. «I can draw on your screen» («Find and draw something interesting on my screen»). Подпись под примером меняется: listening… → thinking… → speaking…. Курсор **летит по дуге со шлейфом**, потом обводит элемент зелёным скруглённым прямоугольником, ставит стрелку от руки и метку («ios ai project folder», «managerial bookmark»).
  5. «Circle anything, ask about it»: зажать клавиши и обвести курсором. Пример в видео: мышцы на анатомическом рисунке.
  6. «Not in the mood to talk? Type. Double-tap control… ChatGPT style. But, just a note I use Claude in the background!» Сверху выезжает поле «ask HeyClicky…», ответ появляется **текстом в чёлке**. Был задан вопрос по-русски, и ответ пришёл по-русски с иконкой копирования.
  7. «There's one more thing… Voice, drawing, text mode, agents…» [Show me].
- **Состояния** дублируются в чёлке: Listening (оранжевый микрофон в меню-баре), Thinking, Thinking deeper, Speaking (волна), Drawing on your screen…. Возле курсора: маленький зелёный эквалайзер (слушает), спиннер (думает), пилюля с текстом (ответ). Основной ответ звучит голосом (выбирается в Settings → Voice). Текстом показываются только короткие подписи.
- **16:42–21:30. Home** (⌃⌘A, выезжает из чёлки «джинном»). Приветствие «Evening, Alexandr. Hold Control + Option and tell me what to take off your plate.» Слева список агентов, **созданных автоматически по интервью**: Study Pal (spaced repetition), Market Scout (ESL-конкуренты), Build Lab (mistake detector), Shippy, Research Buddy (сделал PDF-бриф по SpaceX: «3 progress messages», карточка «spacex…rch.pdf», «NEXT STEPS»). В чатах агентов есть цветные карточки-подсказки «Suggested: send one and I'll get started». В «Suggested for you» лежат предложения вида «I'll build a clickable prototype of your mistake detector… Want me to do it? [No] [Adjust] [✓ Yes, do it]».
- **Агенты на краю экрана.** Справа сверху висит стопка аватаров. При наведении открывается поповер («Shippy • Done», текст вопроса, [Follow up — hold control + option], [Type…], «History»). Это реализация «Clicky agent» в фоне.
- **18:33. Paywall** «Choose your HeyClicky plan» (Monthly/Yearly «Save 20%»):
  - Free $0: 25 talk / 25 agent messages в месяц, «plenty of dictation».
  - Pro $20 (Popular): unlimited talk и dictation, 150 agent messages.
  - Max $100: 1000 agent messages.
  - Пользователь выбрал «Use HeyClicky for free».
- **19:00–20:00. Settings.**
  - Account: «You're on the Free plan» со счётчиками 0/25.
  - General: Show in Dock, Show in screen recordings, Quick peek on notch hover, updates, WhatsApp community.
  - Invite & Earn: 25%, калькулятор «$13,650».
  - Voice: скорость 0.5–1.5x и 10 голосов (Cedar, Marin…).
  - Microphone: выбор входа и «Test microphone».
  - Dictation: языки и словарь.
  - Cursor: 4 цвета, «Hide floating cursor».
  - Agents: Auto-approve extra usage, Always allow computer use, Suggest agent tasks, Speak when a Clicky starts or finishes, Show updates beside the cursor.
  - Integrations: Notion, Linear, GitHub, Google Docs/Calendar, Calendly, Canva и др., плюс «Add custom connector».
- **22:00–23:00.** В Gmail появилось письмо от имени пользователя. Его, вероятно, надиктовали или сгенерировал Clicky (предп.).

## 2. Экраны и стиль

- **Карточка онбординга:** тёмно-серая (#3a3a3c-подобная), радиус ~16 px, мягкая тень, контент по центру. Заголовок белый, semibold, ~20 px. Подзаголовок серый, ~13 px. Первичная кнопка — пилюля с **голубым градиентом и внутренним бликом** («стеклянная»), вторичная — светло-серая пилюля.
- **Notch-панель:** чисто чёрная, скругления только снизу, выезжает из чёлки. В ней 1–2 строки текста и одна кнопка.
- **Курсор-компаньон:** залитый треугольник выбранного цвета ~14 px рядом с системным курсором. Ярко-зелёные пилюли-подписи с белым текстом и каомодзи. Аннотации рисуются от руки, зелёным, с полупрозрачным шлейфом.
- **Home/Settings:** почти чёрное окно (#111–#1c1c1e), сайдбар с аватарами-облачками, синяя подсветка выбранного пункта, крупные градиентные пилюли «Hold Control + Option to talk». Пастельные карточки (голубая, розовая, жёлтая).
- **Сайт и auth-страница светлые**, крупный жирный гротеск («You're signed in.»).
- Общий тон: игривый, маскот, каомодзи, разговорные тексты от первого лица («I live in your notch now»). Движение: genie из чёлки, дуговой полёт курсора, «танцующие» бары.

## 3. Что удачно / что неудачно

**Удачно**
- Разрешения объясняются по одному. Есть плитка «drag me into the list», статус «Waiting…» → «✓ Granted», понятно, что делать.
- Каждая функция обучается действием: проверка микрофона с барами, нажатие реальных клавиш, демонстрация рисования на экране.
- Персонализация по интервью: готовые агенты и задачи под рассказ пользователя о продукте.
- Состояния видны в трёх местах: чёлка, курсор, пилюля. Ответ в текстовом режиме сохраняет язык вопроса (русский).
- «Skip demo», «Back», пейджер.

**Неудачно**
- Онбординг длинный, ~16 мин в этой записи, с паузами на «thinking». Интервью из 4 вопросов затягивается.
- Карточка онбординга живёт поверх браузера и перекрывается другими окнами. Были случайные открытия Dock и контекстного меню закладок.
- Демо **без спроса открыло сайты и Gmail-черновик** основателям. Это навязчиво и выглядит как реклама.
- Тёмная тема с плотным мелким серым текстом (~11 px) читается плохо. Много декоративного шума.
- Paywall появляется сразу после тура, хотя ценность пользователь почувствовал не в полной мере. Реферальный экран с «$13,650» выглядит как маркетинг.
- Двойной экран Screen Recording, требующий Quit & Reopen, сбивает.

## 4. Что можно взять нам

1. **Онбординг разрешений:** по одному шагу на право, с причиной («Нужен микрофон, чтобы записывать вас; системный звук — чтобы записывать ученика»). Перетаскиваемая плитка приложения, живой статус и автоматический переход после выдачи. Сразу проверка: эквалайзер для **двух дорожек** (mic и system audio) с фразой «Скажите "Testing, 1, 2, 3"» и предупреждением про Bluetooth.
2. **Хоткей учим действием:** рисуем keycaps, которые подсвечиваются при реальном нажатии, и делаем тестовый скриншот домашки прямо в онбординге.
3. **Пилюля записи наверху** (у нас вместо чёлки, в светлом стиле VoiceOS): состояния Готов → Запись (таймер, два мини-индикатора уровня tutor/student) → Скриншот сохранён (вспышка-подпись) → Обработка → Карточка готова. Короткие подписи-пилюли рядом, как «loud and clear».
4. **Указание на UI для обучения репетитора:** coach-marks со шлейфом и обводкой элемента («Здесь карточка ученика»). Только по запросу или в первом запуске, с кнопкой «Пропустить».
5. **Голос для ученика (позже):** push-to-talk с удержанием клавиш, «Listening… release to send», альтернатива «Or type here». Подсказки вместо ответов могут выводиться в маленькую пилюлю у курсора, объяснения — с отсылкой к русскому.
6. **Персонализация:** 2–3 вопроса при старте (уровень учеников, формат уроков), чтобы шаблоны карточки ошибок сразу были «под вас».
7. **Приватность:** чего *не* делать — без спроса открывать сайты и черновики. Явно показывать, когда идёт запись (иконка в меню-баре и пилюля), и дать переключатель «Show in screen recordings».
8. **Settings-структура** как у них: Account/Plan со счётчиками использования, Microphone с тестом, Shortcuts, словарь терминов (имена учеников).
9. **Стиль:** брать их пилюли с мягким градиентом и состояния, но в светлой палитре. Шрифт крупнее 13 px, без каомодзи для взрослой аудитории репетиторов (для учеников-детей можно).
