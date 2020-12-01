![Test](https://github.com/ganttify/action-notify-slack/workflows/Test/badge.svg)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# Notify Slack Action

Send Github Actions workflow status notifications to Slack regarding failures, warnings or even success.

### Example workflow

```yaml
steps:
  - uses: ravsamhq/notify-slack-action@master
    if: always()
    with:
      status: ${{ job.status }}
      notify_when: 'failure' # default is 'success,failure,warnings'
      title: Custom title for your notification
    env:
      SLACK_WEBHOOK_URL: ${{ secrets.SLACK_WEBHOOK_URL }} # required
```
