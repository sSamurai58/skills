# UX-тексты

## Проблема подписи кнопки

**Никогда не используйте «OK», «Submit» или «Yes/No».** Это лениво и неоднозначно. Используйте паттерны verb + object:

| Bad | Good | Why |
|-----|------|-----|
| OK | Save changes | Говорит, что произойдёт |
| Submit | Create account | Фокус на результате |
| Yes | Delete message | Подтверждает действие |
| Cancel | Keep editing | Проясняет, что значит «cancel» |
| Click here | Download PDF | Описывает назначение |

**Для destructive actions** называйте разрушение:
- «Delete», не «Remove» (delete постоянно, remove подразумевает recoverable)
- «Delete 5 items», не «Delete selected» (показывайте count)

## Error Messages: The Formula

Каждое сообщение об ошибке должно отвечать: (1) Что случилось? (2) Почему? (3) Как исправить? Пример: «Email address isn't valid. Please include an @ symbol.» — не «Invalid input».

### Error Message Templates

| Situation | Template |
|-----------|----------|
| **Format error** | "[Field] needs to be [format]. Example: [example]" |
| **Missing required** | "Please enter [what's missing]" |
| **Permission denied** | "You don't have access to [thing]. [What to do instead]" |
| **Network error** | "We couldn't reach [thing]. Check your connection and [action]." |
| **Server error** | "Something went wrong on our end. We're looking into it. [Alternative action]" |

### Don't Blame the User

Переформулируйте ошибки: «Please enter a date in MM/DD/YYYY format» — не «You entered an invalid date».

## Empty States Are Opportunities

Empty states — моменты онбординга: (1) Кратко признайте, (2) Объясните ценность заполнения, (3) Дайте ясное действие. «No projects yet. Create your first one to get started.» — не просто «No items».

## Voice vs Tone

**Voice** — personality бренда, согласованный повсюду.
**Tone** адаптируется к моменту.

| Moment | Tone Shift |
|--------|------------|
| Success | Celebratory, brief: "Done! Your changes are live." |
| Error | Empathetic, helpful: "That didn't work. Here's what to try..." |
| Loading | Reassuring: "Saving your work..." |
| Destructive confirm | Serious, clear: "Delete this project? This can't be undone." |

**Никогда не используйте humor для ошибок.** Пользователи уже раздражены. Будьте helpful, не cute.

## Writing for Accessibility

**Link text** должен иметь standalone meaning: «View pricing plans», не «Click here». **Alt text** описывает информацию, не изображение: «Revenue increased 40% in Q4», не «Chart». Используйте `alt=""` для decorative images. **Icon buttons** нуждаются в `aria-label` для контекста screen reader.

## Writing for Translation

### Plan for Expansion

Немецкий текст ~на 30% длиннее английского. Закладывайте место:

| Language | Expansion |
|----------|-----------|
| German | +30% |
| French | +20% |
| Finnish | +30-40% |
| Chinese | -30% (fewer chars, but same width) |

### Translation-Friendly Patterns

Держите числа отдельно («New messages: 3», не «You have 3 new messages»). Используйте полные предложения как единые строки (порядок слов зависит от языка). Избегайте abbreviations («5 minutes ago», не «5 mins ago»). Давайте переводчикам контекст, где появляются строки.

## Consistency: The Terminology Problem

Выберите один термин и придерживайтесь его:

| Inconsistent | Consistent |
|--------------|------------|
| Delete / Remove / Trash | Delete |
| Settings / Preferences / Options | Settings |
| Sign in / Log in / Enter | Sign in |
| Create / Add / New | Create |

Постройте terminology glossary и enforced его. Variety создаёт путаницу.

## Avoid Redundant Copy

Если заголовок уже объясняет — intro избыточен. Если кнопка ясна — не объясняйте снова. Скажите один раз, скажите хорошо.

## Loading States

Будьте конкретны: «Saving your draft...», не «Loading...». Для долгих ожиданий задавайте ожидания («This usually takes 30 seconds») или показывайте progress.

## Confirmation Dialogs: Use Sparingly

Большинство confirmation dialogs — провал дизайна; рассмотрите undo вместо них. Когда подтверждение необходимо: назовите действие, объясните последствия, используйте конкретные button labels («Delete project» / «Keep project», не «Yes» / «No»).

## Form Instructions

Показывайте format через placeholders, не инструкции. Для неочевидных полей объясняйте, зачем спрашиваете.

---

**Избегайте**: Jargon без объяснения. Обвинения пользователей («You made an error» → «This field is required»). Vague errors («Something went wrong»). Смены terminology ради variety. Humor для ошибок.
