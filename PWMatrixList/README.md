Example of creating a PWMatrixList object:
  library(TFBSTools)
  library(JASPAR2014)

  db <- file.path(system.file("extdata", package="JASPAR2014"), "JASPAR2014.sqlite")
  opts <- list()
  opts[["species"]] <- 9606
  opts[["type"]] <- "SELEX"
  opts[["all_versions"]] <- FALSE
  siteList <- getMatrixSet(db, opts)
  siteList2 <- getMatrixSet(JASPAR2014, opts)

  saveRDS(siteList, "siteList.rds")
  saveRDS(siteList2, "siteList2.rds")
