# easyfile

## Install
```sh
npm install easyfile --save
```

## What easyfile do?

1. Map some sync method as default name:

```js
easyfile.exists = fs.existsSync;
easyfile.chmod = fs.chmodSync;
easyfile.chown = fs.chownSync;
easyfile.append = fs.appendeasyfileSync;
easyfile.stat = fs.statSync;
easyfile.read = fs.readeasyfileSync;
easyfile.readlink = fs.readlinkSync;
easyfile.readdir = fs.readdirSync;
easyfile.rename = fs.renameSync;
easyfile.rmdir = fs.rmdirSync;
easyfile.unlink = fs.unlinkSync;
```

2. `mkdir` is `mddirp`

```js
easyfile.mkdir('/newpath/newpath/newpath');
```

3. `copy` support file and dir

```js
easyfile.copy('fromfile', 'tofile');
easyfile.copy('fromdir', 'todir');
```

4. `write` could force write and backup

```js
easyfile.write('tofile', data, {
  force: true,
  backup: true
});
```
