Create a file: .vscode/tasks.json. In the tasks.json file, add the build command.

Build command for Windows users:
Python


{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "Run Python File",
      "type": "shell",
      "command": "python",
      "args": [
        "${file}",
        "<",
        "input.txt",
        ">",
        "output.txt"
      ],
      "presentation": {
        "reveal": "never"
      },
      "group": {
        "kind": "build",
        "isDefault": true
      },
      "problemMatcher": []
    }
  ]
}


Build command for Mac users:
Python


{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "run",
      "type": "shell",
      "command": "python3 ${file} < input.txt > output.txt",
      "group": {
        "kind": "build",
        "isDefault": true
      }
    }
  ]
}


For other OS, please use AI to generate equivalent build commands.
