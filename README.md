# Learning-github-actions

### My first workflow
```
name: my-first-workflow
on: workflow_dispatch
jobs:
	first-job:
		runs-on: ubuntu-latest
		steps:
			- name: Print greeding
				run: echo "Hello world!"
			- name: Print goodbye
				run: echo "bye!"
```

### NodeJS Test workflow
```
name: Test Projet
on: push
jobs:
	test: 
		runs-on: ubuntu-latest
		steps: 
			- name: Get code
				uses: actions/checkout@v4.1.1
			- name: Install NodeJS
				uses: actions/setup-node@v3
				with:
					node-version: 18
			- name: Install dependencies
				run: npm ci
			- name: Run Tests
				run: npm test
			
					
```