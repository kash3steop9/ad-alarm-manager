# Alarm Manager for AppDaemon

This automatically arms and disarms the alarm as well as provides various telegram commands.

```yaml
alarm_manager:
  module: alarm_manager
  class: AlarmManager
  dependencies: sentry
  alarm: alarm_control_panel.home
  telegram:
    - !secret telegram_group_id_home
  reminder_time: "23:45:00"
  deactivate_time: "07:00:00"
  activation_delay: 15
  alarm_code: !secret simplisafe_code
```

It currently requires some custom scripts. I may rewrite this to be reusable, but it's primarily here to make it easier to manage/install the code on my own installations.
