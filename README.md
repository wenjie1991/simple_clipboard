This is a small tool for *inux, which simulate the system clipboard tool (like `xsel`) in terminal.

The `clipboard` is writen in Perl 6. First, [instal the Perl6]<https://rakudo.org/files/star/source>.

Them put the `clipboard` into the Linux system `PATH`.

Put text into clipboard:
```
echo "something put int clipboard" | clipboard -i
```

Get text from clipboard:
```
clipboard -o
```


I put the following lines in the `.vimrc` file to enable quick paste in vim by adding:
```
nmap \ap :r !clipboard -o
```
Then, you can type `\ap` in the normal mode of Vim, then the text in clipboard will append after the cursor.

Most of the time, it works with `readlink` to get the full path of a file, then paste it into script.
