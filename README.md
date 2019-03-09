# jsalgo
> Algorithms in javascript for interviews

##  Bring up a virtual environment
I personally like isolating my codebases from my host environment. 
Provision script includes `node v8`, `npm` ,`jest` and `zsh`
```sh
$ vagrant up
$ vagrant ssh
$ cd /jsalgos
```
## Test a specific file
```sh
$ jest anagrams/test.js
```
## Debug 
Insert a breakpoint as `debugger` in your code
```javascript
function palindrome(str) {

	reversed = ''

	for (let char of str) {
		reversed = char + str
	}
	debugger;
	return str === reversed
}
palindrome('asa')
```
In the terminal inspect the file
```
$ node inspect index.js
```
type `c` or `continue` to execute and hit the breakpoint (`debugger`) you'll get something that looks like this

```
break in index.js:23
 21 		reversed = char + str
 22 	}
>23 	debugger;
 24 	return str === reversed
 25 }
```
Enter `repl` mode to print out variables
```
$ repl
```
## Todo
Travis build
