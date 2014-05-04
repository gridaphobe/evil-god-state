# Evil God State

This is an [evil-mode][] state for using [god-mode][].

It provides a command `evil-execute-in-god-state` that switches to `god-mode` for the next command. I bind it to `,`

```lisp
(evil-define-key 'normal global-map "," 'evil-execute-in-god-state)
```

for an automatically-configured leader key.

[evil-mode]: https://gitorious.org/evil/
[god-mode]: https://github.com/chrisdone/god-mode
