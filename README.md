# ahhadle-relay

사내 AHHADLE 서버의 Slack 로그인용 https 중계 페이지입니다.

Slack OAuth는 Redirect URL로 https만 허용합니다. 이 페이지가 Slack이 돌려준 `code`, `state`, `error`만 골라 사내 서버 `http://172.16.0.210:4173/api/slack/oauth/callback`으로 그대로 이동시킵니다. 이 페이지는 값을 저장하거나 외부로 보내지 않으며, 이동할 주소는 고정돼 있습니다. `code`는 Client Secret 없이 쓸 수 없는 일회용 값입니다.
