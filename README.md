# CBT791
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 791 is from Anthony S. Rudd (by way of Ken Tomiak) and    *   FILE 791
//*           contains a REXX function written in Assembler, that   *   FILE 791
//*           accomplishes GETMAIN and FREEMAIN functionality from  *   FILE 791
//*           within REXX.  For further documentation, see comments *   FILE 791
//*           in the GETMAIN code.                                  *   FILE 791
//*                                                                 *   FILE 791
//*           email:  ARudd@t-online.de                             *   FILE 791
//*                                                                 *   FILE 791
//*    Problem addressed:                                           *   FILE 791
//*                                                                 *   FILE 791
//*    The REXX language provides a large library of functions.     *   FILE 791
//*    This library includes a function to access main storage      *   FILE 791
//*    directly (the STORAGE function).  However, there is no       *   FILE 791
//*    direct way of allocating main storage from REXX - the        *   FILE 791
//*    following GETMAIN function addresses this problem.           *   FILE 791
//*                                                                 *   FILE 791
//*                                                                 *   FILE 791
//*    A DESCRIPTION OF THE GETMAIN FUNCTION                        *   FILE 791
//*                                                                 *   FILE 791
//*    The GETMAIN function has two sub-functions:                  *   FILE 791
//*                                                                 *   FILE 791
//*    *      OBTAIN, which allocates a block of main storage.      *   FILE 791
//*                                                                 *   FILE 791
//*    *      RELEASE, which releases (ie frees) a previously       *   FILE 791
//*          allocated main storage block.                          *   FILE 791
//*                                                                 *   FILE 791
//*    The main storage blocks are allocated above the              *   FILE 791
//*    16-megabyte address line in subpool 1.  The MVS STORAGE      *   FILE 791
//*    service is used both to allocate and deallocate main         *   FILE 791
//*    storage.                                                     *   FILE 791
//*                                                                 *   FILE 791
//*    Calling sequence                                             *   FILE 791
//*                                                                 *   FILE 791
//*    To allocate a main storage block, code:                      *   FILE 791
//*                                                                 *   FILE 791
//*          addr = GETMAIN('OBTAIN',length);                       *   FILE 791
//*                                                                 *   FILE 791
//*    where OBTAIN is the function to be performed (as usual       *   FILE 791
//*    for REXX functions, only the first character is used, ie     *   FILE 791
//*    'O' is also valid), length is the number of bytes to be      *   FILE 791
//*    allocated, and addr is returned with the decimal (start)     *   FILE 791
//*    address of the allocated main storage block.                 *   FILE 791
//*                                                                 *   FILE 791
//*    To free a previously allocated main storage block, code:     *   FILE 791
//*                                                                 *   FILE 791
//*          frc = GETMAIN('RELEASE',addr,length);                  *   FILE 791
//*                                                                 *   FILE 791
//*    where RELEASE is the function to be performed (only the      *   FILE 791
//*    first character is used, ie 'R' is also valid), addr is      *   FILE 791
//*    the decimal (start) address of the main-storage block to     *   FILE 791
//*    be released, length is the number of bytes to be             *   FILE 791
//*    released, and frc is the function return code.               *   FILE 791
//*                                                                 *   FILE 791
//*    Note that part of an allocated block can be released.        *   FILE 791
//*                                                                 *   FILE 791
//*    The standard REXX function value -3 indicates that REXX      *   FILE 791
//*    detected an error condition while trying to perform the      *   FILE 791
//*    function (eg the function could not be located).             *   FILE 791
//*                                                                 *   FILE 791
//*                                                                 *   FILE 791
```
