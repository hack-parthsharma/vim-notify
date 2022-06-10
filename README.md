# vim-notification

Message notification system for Vim

## Usage

```vim
call notification#show('Hello World')
```

```vim
call notification#show(#{
\  text: 'Hello World',
\})
```

If you want to specify waiting time to stay the notification on screen:

```vim
call notification#show(#{
\  text: 'Hello World',
\  wait: 300,
\})
```

To handle clicked/closed event:

```vim
function! s:my_clicked(data) abort
  echo a:data
endfunction

call notification#show(#{
\  text: 'Hello World',
\  clicked: function('s:my_clicked', ['Hi!']),
\})
```

