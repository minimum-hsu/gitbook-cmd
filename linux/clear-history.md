---
tags: ['linux', 'bash']
---

# Clear History

This command only clears your current shell history. After you exited, no history could be recorded before this command.

```bash
history -c
```

If you want to clear all recorded history, you can remove ~/.bash\_history file, but there are still some commands to be recorded after you exited.

```bash
rm ~/.bash_history
```

You can use some tips to truly clear all history

```bash
cat /dev/null > ~/.bash_history && history -c && exit
```

