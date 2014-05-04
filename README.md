# Evil God State

This is an [evil-mode][] state for using [god-mode][].

It provides a command `evil-execute-in-god-state` that switches to `god-mode` for the next command. I bind it to `,`

```lisp
(evil-define-key 'normal global-map "," 'evil-execute-in-god-state)
```

for an automatically-configured leader key.

Since `evil-god-state` includes an indicator in the mode-line, you may want to use `diminish` to keep your mode-line uncluttered, e.g.

```lisp
(add-hook 'evil-god-start-hook (lambda () (diminish 'god-local-mode)))
(add-hook 'evil-god-stop-hook (lambda () (diminish-undo 'god-local-mode)))
```

[evil-mode]: https://gitorious.org/evil/
[god-mode]: https://github.com/chrisdone/god-mode
