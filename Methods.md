|Method Name|Description|Parameters|Return Type|
|---|---|---|---|
|add|Adds a new step.|[Object step](https://github.com/rstaib/jquery-steps/wiki/Step-Object)|Object wizard|
|insert|Inserts a new step to a specific position.|Integer index, [Object step](https://github.com/rstaib/jquery-steps/wiki/Step-Object)|Object wizard|
|remove|Removes a specific step by an given index.|Integer index|Boolean|
|getCurrentStep|Gets the current step object.|-|[Object step](https://github.com/rstaib/jquery-steps/wiki/Step-Object)|
|getCurrentIndex|Gets the current step index.|-|Integer|
|getStep|Gets a specific step object by index.|Integer index|[Object step](https://github.com/rstaib/jquery-steps/wiki/Step-Object)|
|next|Routes to the previous step.|-|Boolean|
|previous|Routes to the next step.|-|Boolean|
|finish|Triggers the onFinishing and onFinished event.|-|void|
|skip|Skips an certain amount of steps. Not yet implemented!|Integer count|Boolean|