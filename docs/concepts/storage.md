---
order: 3
---

# Variables and storage

## Variables

You can use variables inside your flow definition by using a special syntax: <code v-pre>{{variableName}}</code>.

Variables can be used on each task property that is documented as **dynamic**.

Dynamic variables will be rendered thanks to the Pebble templating engine. Pebble allows the processing of variables with filters and functions. More information on variable processing can be found in the [developer guide](../developer-guide/variables/).

Flows, tasks, executions, triggers, and schedules have default variables; for example <code v-pre>{{ flow.id }}</code> allows accessing the identifier of a flow inside an execution.

Flow inputs will be available as variables via  <code v-pre>{{ inputs.nameOfTheInput }}</code>, and tasks output attributes will be available as variables via <code v-pre>{{ outputs.nameOfTheTask.nameOfTheOutputAttribute }}</code>.

Most variables will be stored inside the context of the execution and directly passed from task to task. Some variables are of a special type and will be stored inside Kestra's internal storage. Those variables will be automatically fetched from the internal storage when needed.

## Internal storage

Kesta's internal storage allows storing arbitrary-sized files inside a dedicated storage area.

If an output attribute is stored inside the internal storage, it will be retrievable from a variable named <code v-pre>{{outputs.nameOfTheTask.nameOfTheOutputAttribute}}</code>. Kestra will automatically fetch the file when the variable is used.

Inputs of type <code v-pre>FILE<code v-pre> will be automatically stored inside the internal storage.

On the **Outputs** tab of an execution, if an output attribute is from the internal storage, there will be a link to download it.