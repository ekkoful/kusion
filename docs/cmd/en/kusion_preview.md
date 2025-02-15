## kusion preview

Preview a series of resource changes within the stack

### Synopsis

Preview a series of resource changes within the stack.

Create or update or delete resources according to the KCL files within a stack. By default, Kusion will generate an execution plan and present it for your approval before taking any action.

```
kusion preview [flags]
```

### Examples

```
  # Preview with specifying work directory
  kusion preview -w /path/to/workdir
  
  # Preview with specifying arguments
  kusion preview -D name=test -D age=18
  
  # Preview with specifying setting file
  kusion preview -Y settings.yaml
  
  # Preview with ignored fields
  kusion preview --ignore-fields="metadata.generation,metadata.managedFields"
```

### Options

```
  -D, --argument stringArray     Specify the top-level argument
  -C, --backend-config strings   backend-config config state storage backend
      --backend-type string      backend-type specify state storage backend
  -d, --detail                   Automatically show plan details after previewing it
  -h, --help                     help for preview
      --ignore-fields strings    Ignore differences of target fields
      --no-style                 no-style sets to RawOutput mode and disables all of styling
      --operator string          Specify the operator
  -O, --overrides strings        Specify the configuration override path and value
  -Y, --setting strings          Specify the command line setting files
  -w, --workdir string           Specify the work directory
```

### SEE ALSO

* [kusion](kusion.md)	 - kusion manages the Kubernetes cluster by code

###### Auto generated by spf13/cobra on 22-Nov-2022
