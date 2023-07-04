Щоб отримати інформацію про користувача Slack, нам потрібно скористатися Slack API.

Для цього в bash виконаємо наступний код

```
curl --location 'https://slack.com/api/users.info?user=<member-id>' --header 'Authorization: Bearer <token>'
```

де `<token>` - токен доступу Slack App, `<member-id>` - унікальний аунтифікатор користуча, дані якого потрібно отримати.

Щоб отримати `<token>` - токен доступу Slack App:
1. Переходимо за посиланням https://api.slack.com/
2. Далі `Your Apps`
3. Далі `Create New App` та створюємо утиліту.
4. Відкриваємо утиліту, яку щойно створили, та переходимо в `Features` - `OAuth & Permissions` - `User OAuth Token`(Не `Bot User OAuth Token`)

Щоб отримати `<member-id>`:
1. Відкриваємо `Profile` - `...` - `Copy member ID`.

