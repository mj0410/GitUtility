### Basic Git Bash
```shell
git clone link

git add *
git commit -m "update"
git push

git pull

git reset commit_id # return to the status before that commit
git rm -r --cached # remove cache
```

### Markdown
:smiley: [emoticon](https://gist.github.com/rxaviers/7360908)

```
hyperlink    [link name](link)
image        <img src="image link" width="size(num)">
new line     <br/>
empty space  &nbsp;
```

```
```diff
+ Green
- Red
! Orange
@@ Pink @@
# Gray
```

```
```mermaid
    graph BT;
        layer_b[Previous Layer];
        layer_t[Filter concatenation];
        filter1[1X1 Conv Layer];
        filter2[3X3 Conv Layer];
        filter3[5X5 Conv Layer];
        layer_b --> filter1;
        layer_b --> filter2;
        layer_b --> filter3;
        filter1 --> layer_t;
        filter2 --> layer_t;
        filter3 --> layer_t;
```
