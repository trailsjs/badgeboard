## Pulling from here:

```sh
~/your-org.github.io$ git pull https://github.com/repo-utils/badgeboard.git
~/your-org.github.io$ make ; make db
~/your-org.github.io$ git commit index.html src/db.json -m 'rebuild'
~/your-org.github.io$ git push
```

You'll probably need to resolve merge conflicts after you do `git pull`.

## Creating new badgeboard:

1\. clone this repo

```sh
~$ git clone https://github.com/repo-utils/badgeboard.git your-org.github.io
```

2\. change `config.yaml`
3\. change `.gitignore`, unignore autogenerated files, see comments there
4\. make it:

```
~/your-org.github.io$ make
```

5\. test it:

```
~/your-org.github.io$ firefox index.html
```

6\. add autogenerated files so they will appear on github pages:

```
~/your-org.github.io$ git add src/db.json index.html
~/your-org.github.io$ git commit src/db.json index.html -m 'rebuild'
```

