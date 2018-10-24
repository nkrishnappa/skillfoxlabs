
# Modules

## Standard

Here is the folder layout of a standard module.
```
$ tree standard-module/
.
├── README.md
├── main.tf
├── variables.tf
├── outputs.tf
```
Key Files:
  * main.tf - should be the primary entry point.
  * variables.tf - Any variables defined in `main.tf` and should have one or two sentence descriptions that explain their purpose.
  * outputs.tf - Any output of the module and should have one or two sentence descriptions that explain their purpose.


## Nested modules
```
$ tree nested-module/
.
├── README.md
├── main.tf
├── variables.tf
├── outputs.tf
├── modules/
│   ├── nestedA(external use)/
│   │   ├── README.md
│   │   ├── variables.tf
│   │   ├── main.tf
│   │   ├── outputs.tf
│   ├── nestedB(internal use)/
│   │   ├── variables.tf
│   │   ├── main.tf
│   │   ├── outputs.tf
│   ├── .../
```
Nested Module - Nested modules should exist under the `modules/` subdirectory.

Key differences between Standard and Nested you will see in the `modules/` folder:
  * If there *is not* `README.md` like in the `nextedB` folder example its a internal use module.
  * If there *is* `README.md` like in the `nextedA` folder example its a external use module.
