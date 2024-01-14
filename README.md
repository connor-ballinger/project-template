# project-template
A basic template repo for projects which provides a folder structure and initiates a `renv` library.

## Instructions

At https://github.com/connor-ballinger/project-template, click "Use this template" and follow the prompts.

Alternatively, in RStudio, click "New project - Version Control - Git" and paste the repository address:
https://github.com/connor-ballinger/project-template.

Some code to tidy things up a bit (probably a much better way of doing this...):

```
list.files(pattern = ".gitkeep", all.files = TRUE, recursive = TRUE) |> 
  file.remove()

proj_name <- getwd() |>
  basename()
file.rename("project-template.Rproj", paste0(proj_name, ".Rproj"))
rm(proj_name)
```

## Notes

`renv` assists with reproducibility by managing a project-specific library. 
Documentation can be found [here](https://rstudio.github.io/renv/articles/renv.html).
