# Bang Bang (my baby shot me down)

Having lived in bash for an awfully long time before coming to fish,
my fingers had learned to use a subset of the history substitution.
Most notably, when I needed to tell a program to [make me a sandwich],
I'd `sudo !!`, and there were countless times I'd `mkdir <something>; cd !$`.
Coming to fish, this was hard to get over.

This was before `abbr` became part of fish, 
and in the discussion around how `abbr` would be implemented there was a suggestion about using key bindings to experiment with it.
From that discussion, I took the inspiration for these bindings.
The really nice thing about these versus `abbr` is that they expand immediately (no whitespace needed)
and they expand anywhere, not just at the beginning of the line.

For instance:

```
> which myscript.sh
/usr/local/opt/bin/myscript.sh
> less (!!)
```

works - and as a bonus over the bash use case, the !! expands in place, so you can edit it.
