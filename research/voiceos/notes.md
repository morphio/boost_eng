# VoiceOS: разбор двух записей экрана

Источники: `voiceOS_1.mp4` (V1, ~11 мин, установка и онбординг) и `voiceOS_2.mp4` (V2, ~2.8 мин, оплата и главное окно). Звука в записях нет. Важная оговорка: параллельно был запущен **Wispr Flow** (и Krisp). Часть всплывающих окон принадлежит им, а не VoiceOS; где принадлежность неочевидна, это помечено.

## 1. Процесс по шагам

**Установка (V1 0:00–0:30).** VoiceOS лежит в Applications (828 МБ). Сначала стандартное окно Gatekeeper «downloaded from the Internet», сразу за ним системный запрос «"VoiceOS" would like to control this Mac and access your data» (Accessibility; в macOS 26 раздел называется Device Control and Data Access). Затем полноэкранная интро-сцена с анимированным логотипом и субтитрами голосового ассистента: «Welcome to VoiceOS. I'm your assistant. So, what should I call you?» Имя и фамилия вводятся в две пилюли. Внизу кнопки «Skip intro» и выключение звука.

**Язык (0:46–1:08).** «What language do you speak? Choose all that apply and mark your primary language». Есть поиск и чекбоксы, основной язык отмечается звёздочкой «Primary». Выбраны Russian (Primary) и English. После этого ассистент отвечает уже по-русски: «Отлично, русский — так и поступим. Давайте вас настроим.»

**Вход (1:20–1:55).** «Welcome to VoiceOS. Write faster in all your apps with voice.» Вход по email или через Google. OAuth идёт в Chrome через supabase, затем страница «Login Successful. You can now return to VoiceOS and start using your voice as your keyboard» с кнопкой «Open VoiceOS» (deep link).

**Разрешения (1:55–3:30).** Экран «Enable core features» с тремя карточками:
- «Allow VoiceOS to use your microphone. Let VoiceOS transcribe your speech. Only active during dictation.» После выдачи: «Microphone permission granted. Your speech will be transcribed.»
- «Accessibility permission granted. VoiceOS can insert and edit text.»
- «Allow VoiceOS to see your screen. Only when you ask Agent Mode for help. Screenshots are never stored or shared.»

Справа показана анимация того системного диалога, который сейчас появится. Для Screen Recording есть плавающий помощник «Drag VoiceOS into the Screen & System Audio Recording list, then turn its switch on» с перетаскиваемой плашкой «VoiceOS · Drag me». Дальше идут Touch ID, «Quit & Reopen» и ещё один запрос «"VoiceOS" is requesting to bypass the system private window picker…». Input Monitoring отдельно не запрашивался, по крайней мере в кадре.

**Горячая клавиша Agent (3:30–4:54).** Тест клавиш: «When pressing control (left) + option (left) at the same time, do the keys light up blue?» Кнопки «Yes» и «No, change key». Затем «Ask a simple question: Hold ⌃+⌥, try saying "How can VoiceOS help me?"» с кнопками «Not working?» и «Next». Ответ выезжает в чёрной панели из **нотча** вверху экрана. Внутри видео-подсказки: «Hold the same key and circle anything with your cursor. I'll see it» и «And connect to these apps…» с сеткой иконок (Slack, Gmail, Notion, Linear и т. д.). На 3:43 открылось окно Wispr Flow с подсказкой «AirPods aren't the best for dictation». Это вмешательство Wispr; причина неясна, предполагаю конфликт клавиш.

**Агент и Gmail (5:00–7:05).** «Let's connect your email»: Gmail, Outlook или Apple Mail. Подключение идёт через Composio; на экране согласия Google доступы снимаются галочками по отдельности, и пользователь их не отметил. Затем «You're connected. Gmail is ready to use in VoiceOS.» Задание «Do a task with your voice: "Send an email to VoiceOS team saying 'I completed my first task'"». В нотче сверху стенограмма сказанного по-русски, ниже редактируемая карточка «New Message» (To, тема «Первая задача выполнена», текст, кнопка Send) и подсказка «Type or hold option control to speak». Пользователь дописал в письмо текст руками. После «Sending ✓» пришла ошибка: «Не удалось отправить письмо: приложению не хватает разрешений (scopes) для доступа к Gmail. Вы можете нажать кнопку Next…» Ошибка внятная и на языке пользователя. Потом слева выезжает боковой нотч с сохранёнными задачами: «Access your saved tasks here. Reopen any saved interaction… ask a follow-up», переключение по Option+Tab.

**Импорт словаря (7:10).** VoiceOS нашёл установленный Wispr Flow и предложил «Import your keywords» или «Skip for now».

**Диктовка (7:13–10:20).** «Dictation Mode: VoiceOS transcribes your words, removing filler words and correcting mistakes.» Тест клавиши «When pressing fn does the key light up blue?» Затем «Try dictating» в макетах Messages («Hold down fn key and try saying "Planning on going to the gym. Emoji" then release») и Email («Hi Bob…»). Нужно кликнуть «Click here to start», чтобы поле получило фокус. Режим hold-to-talk: держишь клавишу, говоришь, отпускаешь, и текст вставляется в поле с курсором. Индикатор — чёрная пилюля внизу по центру: точки в простое, волна во время речи, спиннер на обработке. Владелец не установлен: у Wispr такая же пилюля, а у VoiceOS есть настройка «Hide dictation pill». Русская диктовка вышла с ошибками («Привет пуку… Напиши Симу Куку»). Пользователь сам надиктовал: «Что-то качество распознавания не очень хорошее». Позже текст вставлялся **дважды** («почему-то два раза всё время повторяется»). Предполагаю, что обе программы висят на fn. Английское письмо распознано чисто, с абзацами.

**Пейвол (10:30, V2 0:00–0:36).** «Start your 7-day free trial»: Yearly $11.99/mo (Save 60%) или Monthly $29.99/mo, «No payment due now», «Then $29.99 per month. Cancel anytime.», ссылка «Are you a student?». Рядом отзывы и «20,000+ voicepilled». Оплата через Stripe (Apple Pay, Google Pay, Link), «Due today $0». После оплаты: «Give a friend 1 month free» с инвайт-ссылкой и конфетти.

**Главное окно (V2 0:37–2:45).** Dashboard, Insights, History, Dictation, Agent, Apps, Settings (подробно в разделе 2). Insights пока закрыт: «Insights locked · 9 of 100 sessions. Put VoiceOS to work, your stats are taking shape behind the glass.» Режим Edit в действии не показан, есть только переключатель «Edit selected text — Rewrite, translate, or fix highlighted text».

## 2. Экраны и элементы UI

- **Интро-оверлей:** затемнённый рабочий стол, субтитры, озвучка, ввод имени, «Skip intro».
- **Мастер онбординга:** прогресс-бар сверху, «Back» и выключение звука снизу, «Not working?» рядом с «Next». На каждом шаге карточка с клавишами-«капсами», которые подсвечиваются при нажатии.
- **Top notch (агент):** стенограмма, ответ, карточки действий (черновик письма с Send), строка ввода «Type or hold … to speak».
- **Side notch:** история задач агента с поиском.
- **Пилюля диктовки** внизу экрана.
- **Dashboard:** «Good afternoon, Alexandr», подсказки «Dictation Mode — Hold fn in any text field» и «Agent Mode — Hold option control to ask», рефералка (Invite friends, Affiliate 25%), видеотуториалы.
- **History:** поиск, фильтры «All Apps» и «Dictate Mode», «Showing 6 of 9 sessions». В карточке: приложение, режим, «3m ago», текст и кнопки retry, flag, delete, copy. Исходной версии рядом с исправленной нет.
- **Dictation:** *Polishing* — None («Keeps your original wording»), Light («Removes self-corrections, fixes formatting»), Polished («Smooths phrasing for clarity»), у каждого уровня пример «до/после». *Writing Style by destination* — вкладки Personal Chat, Work Chat, Email, Other и стили Formal, Casual, Very Casual, Excited с превью сообщения; «Pinned apps always dictate in this style», «+ Pin app». *Spelling* — Import, Add, примеры VoiceOS, Claude, lmk, GTM. *Replacements* — сказанная фраза заменяется текстом (например, «my calendar link → https://cal.com/…»).
- **Agent:** голос (Slow/Normal/Fast, «Sky — Warm and friendly»). «About you» с Memories (0). Actions: Point and ask about your screen, Create prompt, Edit selected text, Set reminders, Control music, Open app.
- **Apps:** магазин интеграций (Official/Custom), из них подключён Gmail. В карточке приложения 7 действий, у каждого своё разрешение: «Ask permission» или «Don't ask».
- **Settings → General:** горячие клавиши для Agent, Dictation («Hold to dictate»), Hands-Free Dictation («Double tap» / «Press once»), Hands-Free Agent, «Paste Last Transcript», «Open sidebar». Также Languages («Russian + 1 more»), Launch at Login, Show in dock, **Context Awareness** («Use limited text content from the app to spell names correctly»), **Private mode** («none of your dictation data will be stored or used for model training…», по умолчанию **выключен**), блок видимости пилюли и нотчей, выбор микрофона, Interaction sounds.
- **Appearance:** тема и стиль нотча (Liquid Glass / Solid Black).
- **Subscription:** Free (100 диктовок и 25 запросов агенту в неделю), Pro $11.99, Team $13.99 за место (минимум 2).
- **Account:** версия 0.1.39, Delete account. Имя здесь подписано «Used to understand the content on the screen».

## 3. Что удачно / что неудачно

**Удачно**
- Онбординг ведёт голос, он сразу переключается на родной язык пользователя.
- Каждое разрешение объяснено одной строкой «зачем» и с ограничением («Only active during dictation», «Screenshots are never stored»). Перед системным диалогом показан его макет.
- Помощник «перетащи меня в список» и тест «клавиши подсвечиваются?» с вариантом «No, change key».
- Обучение через действие: макеты Messages и Email с готовой фразой для произнесения.
- Стили письма зависят от адресата, у каждого уровня полировки пример «до/после».
- Импорт словаря из конкурента.
- Ошибка агента объяснена понятно и по-русски.

**Неудачно**
- Онбординг очень длинный: ~11 минут, около 20 шагов, браузер открывается дважды, пейвол появляется до того, как пользователь получил ценность.
- Нет защиты от конфликта с другими диктовщиками на той же клавише, отсюда двойная вставка.
- Не проверяется, выданы ли OAuth-доступы. Пользователь узнаёт об этом только из ошибки отправки.
- Низкое качество русской диктовки.
- Private mode выключен по умолчанию.
- В History нет «было → стало», то есть не видно, что именно исправлено.
- Insights закрыт до 100 сессий.

## 4. Что можно взять нам

1. **Онбординг с разрешениями.** Одна страница-чеклист «Enable core features»: у каждого разрешения строка «зачем» и «когда активно», статус ✓, а до системного окна показан его макет. Для Screen Recording пригодится плашка «перетащи сюда». Для репетитора: микрофон и системный звук (две дорожки), Screen Recording для скриншотов ДЗ, Accessibility только для режима ученика. Каждое разрешение просим тогда, когда нужна функция, а не всё сразу.
2. **Горячие клавиши.** Hold-to-talk плюс hands-free (double tap). Тест «нажмите — подсветилось?» с «Change key». При старте проверяем другие диктовщики (Wispr, VoiceOS, macOS Dictation) и предупреждаем о конфликте. Скриншот ДЗ делаем отдельным хоткеем с таким же тестом.
3. **Индикатор.** Маленькая пилюля с тремя состояниями: тишина, речь (волна), обработка. Для записи урока индикатор должен быть постоянным: таймер и уровни обеих дорожек, чтобы было видно, что пишется и голос ученика.
4. **История исправлений.** В отличие от VoiceOS, храним пару «оригинал → исправление» с подсветкой diff, тегом типа ошибки, приложением и временем. Нужны фильтры по приложению, типу и периоду и кнопка «пометить как неверное» (у VoiceOS есть флаг).
5. **Контекст приложения.** Аналог «Writing Style by destination»: стиль и строгость проверки зависят от приложения (мессенджер — мягко, письмо или эссе — строго). Аналог Spelling/Replacements: личный словарь ученика (имена, термины), чтобы их не считать ошибками.
6. **Приватность.** Короткие обещания прямо на экранах разрешений. Приватный режим включён по умолчанию для ученика. Явно сказать, что хранится локально, что уходит в облако и что видит репетитор. Пауза захвата в одно касание.
7. **Режим ученика («reverse Wispr»).**
   - Уровни как Polishing: «только подсказать» (подчеркнуть и дать намёк) → «исправить и записать» → «отполировать».
   - По умолчанию показываем подсказку, а не готовый ответ.
   - Объяснение привязано к русскому: «в русском нет артикля, поэтому…».
   - Обучение через действие, как «Try dictating»: в онбординге ученик пишет фразу с типичной ошибкой и сразу видит, как работает подсказка.
8. **Карточка ученика.** Аналог Insights, но открытый сразу: топ повторяющихся ошибок и динамика. Пустое состояние делаем полезным, а не «locked».
9. **Онбординг короче.** Первый результат за 2–3 минуты, интеграции и оплата после первой ценности.
