SET(SUBDIR_DEFINED 1 PARENT_SCOPE)
SET(SUBDIR_UNDEFINED PARENT_SCOPE)

# The above sets should not affect the current scope.
IF(DEFINED SUBDIR_UNDEFINED)
  PASS("SubdirScope Undefine Test" "(${SUBDIR_UNDEFINED})")
ELSE(DEFINED SUBDIR_UNDEFINED)
  FAILED("SubdirScope Undefine Test" "(${SUBDIR_UNDEFINED})")
ENDIF(DEFINED SUBDIR_UNDEFINED)
IF(DEFINED SUBDIR_DEFINED)
  FAILED("SubdirScope Define Test" "(${SUBDIR_DEFINED})")
ELSE(DEFINED SUBDIR_DEFINED)
  PASS("SubdirScope Define Test" "(${SUBDIR_DEFINED})")
ENDIF(DEFINED SUBDIR_DEFINED)
