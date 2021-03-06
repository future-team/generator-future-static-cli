# gfs-cli
cli for f2e future static 

## Install

```bash
$ npm install -g gfs-cli
```

## Usage
### gfs
Default show help
```bash
$ gfs 
```

### project template
Supported project template generated by `future-static` maps list: 

| project type | cli template | file type |
| ------------- |:-------------:| -----:|
| webpack+react+redux+cortex | react-redux | web, component|
| webpack+react | react-dm | web(default) |
| webpack+jquery+handlebars+cortex | -- | -- |
| module-template(jquery or react) | -- | -- |
| module-ts-template | -- | -- |

you can use it like:
```bash
# add `webpack+react+redux+cortex` component files
$ gfs add --template react-redux --type component --name question-detail

# add `webpack+react+redux+cortex` web files
$ gfs add --template react-redux --type web --name question

# add `webpack+react` web files
$ gfs add --template react-dm --name question
```

### gfs add <project-type> <generator-name> <name> <options>
Add generator-name to current project
```bash
$ gfs add --template react-redux --type component --name question-detail
$ gfs add --template react-redux --type web --name question
```  

###gfs rm <project-type> <generator-name> <name> <options>
Remove generator-name from current project, it will give a prompt before remove
```bash
$ gfs rm --template react-redux --type component --name question-detail
$ gfs rm --template react-redux --type web --name question
```

### npm alias
Some aliases for npm script, this dependency your `package.json` script config
```bash
$ gfs build
$ gfs dev
$ gfs demo
$ gfs start
```

## Test
```bash
$ npm run test
```