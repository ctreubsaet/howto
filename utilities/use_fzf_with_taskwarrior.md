# Use FZF with Taskwarrior

You can combine the inbuilt lists of Taskwarrior to filter your tasks based on the input from FZF.

You can find all tasks with a specific tag:
```
$ task +$(task _tags | fzf)
```

You can find all tasks in a specific project:
```
$ task project:$(task _projects | fzf)
```

You can easily switch to another context:
```
$ task context $(task _context | fzf)
```

You can find a specific task in a list with a '{id}:{description}' format:
```
$ task $(task _zshids | fzf | cut -d":" -f1)
```
