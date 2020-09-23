<div align="center">

## Fake File


</div>

### Description

Create a file of any type, filled with x bytes. (x = user specified). Exercises file I/O.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Drat911](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/drat911.md)
**Level**          |Beginner
**User Rating**    |4.0 (20 globes from 5 users)
**Compatibility**  |C
**Category**       |[Files](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files__3-2.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/drat911-fake-file__3-2644/archive/master.zip)

### API Declarations

```
#include <stdio.h>
```


### Source Code

```
/*
 Fakefile.c by Drat911 (drat911@nwez.com)
 Creates a filename of your choice, filled with characters.
 Usefull for making dummy files, and disguising them as anything ELSE =)
*/
#include <stdio.h>
int main() {
 FILE *ifile;
 long int bytes, i;
 char filename[50], fullfilename[55];
 printf("Fakefile by Drat911 (drat911@nwez.com)\n\n");
 printf("Please enter a filename to write to (Ex: test.exe): ");
 scanf("%s",&filename);
 printf("\n");
 printf("Please enter the size in bytes (1000000 = 1mb): ");
 scanf("%d",&bytes);
 sprintf(fullfilename, "c:\\%s",filename);
 ifile = fopen(fullfilename,"w");
 if (ifile == NULL) {
  printf("Could not open %s for writing. Exiting...\n");
  system("PAUSE");
  exit(0);
 }
 printf("Filling %s with %d characters...\n",fullfilename,bytes);
 for ( i = 0; i < bytes; ++i) {
  fputc('$',ifile);
 }
 printf("Done!\n");
 system("PAUSE");
 return 0;
}
```

