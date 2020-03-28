# xdebug-win
How to install xDebug (debugger and profiler tool for PHP) on Windows


## 1. Access Xdebug website
[xDebug website](https://xdebug.org/)

## 2. Download a .dll
Download a .dll file on Xdebug website

## 3. Copy to extensions directory
Copy .dll file to extensions directory
 
## 4. Configuration of php.ini
zend_extension = php_xdebug.dll

xdebug.remote_enable = 1

xdebug.remote_autostart = 1'

## 5. Donwload PHP Debug Extension (VS Code)
[PHP Debug Extension](https://marketplace.visualstudio.com/items?itemName=felixfbecker.php-debug)


## 6. Create a launch.json file
```
{
    ...

    "configurations": [
        {
            "name": "Listen for XDebug",
            "type": "php",
            "request": "launch",
            "port": 9000,
            "pathMappings": {
                "/vagrant": "${workspaceFolder}",
            }
        },
        {
            "name": "Launch currently open script",
            "type": "php",
            "request": "launch",
            "program": "${file}",
            "cwd": "${fileDirname}",
            "port": 9000
        }
    ]
```
