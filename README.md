# Outcome review (sample room)

A sample room for [bnbloc](https://github.com/luckylhb90/bnbloc), built only
with what any member can use: a room package, an AI schedule and the `runs`
source (agent conversations, read only with the organization admin's
consent).

Install it from the Library ("Create a room from this"). The room asks your
organization admin to let it read conversations; once they agree, turn on
its daily task. Everything in it is meant to be changed: the schedule's
words, its time, what it reports and to whom. Ask in the room, or save your
version as your own component.

Nothing here is part of the platform. It is an example of what a room can
do, published like anyone's content.

## Publish

```sh
COPYFILE_DISABLE=1 tar --format ustar -cf /tmp/outcome-review.tar component.json README.md
# create it in your Library (POST /v1/content-components, application/x-tar),
# then, as a super admin, share it with every organization:
bnbloc content promote <id> --rollout auto
```
