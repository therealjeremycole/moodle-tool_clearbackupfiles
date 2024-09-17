![Moodle Plugin CI](https://github.com/doiphode/moodle-tool_clearbackupfiles/actions/workflows/moodle-ci.yml/badge.svg)

# tool_clearbackupfiles

This admin tool clears all backup files from the server. It is useful for freeing up space from dev and test servers once they are refreshed from production.

It also gives a report of how many .mbz files were deleted and how much space was cleared.

## Instructions
The backup files can be deleted from `/admin/tool/clearbackupfiles/index.php` and you can find logs at `/report/log/index.php`. The default Moodle events are used to create log entries.

### To Do

- [ ] Add option to include/exclude "component=backup AND filearea=course"
- [ ] Add option to include/exclude "component=backup AND filearea=activity"
- [ ] Add option to include/exclude "component=user AND filearea=backup AND filename NOT LIKE 'Sharingcart-%'"
- [ ] Add option to include/exclude "component=user AND filearea=backup AND filename LIKE 'Sharingcart-%'"
- [ ] Add option to include/exclude "component=user AND filearea=private"
- [ ] Add option to include/exclude "filearea=attachment"
- [ ] Add preview of amount of data that would be deleted by selecting each option
