# get_next_line

Ce projet a pour but de vous faire coder une fonction qui renvoit une ligne terminée par un retour à la ligne lue depuis un descripteur de fichier

GCL Get_Next_Line utilise la 
[LIBFT](https://github.com/yataji/libft)

main pour tester la fonction:

```
#include <stdio.h>
#include <fcntl.h>
#include <stdlib.h>
#include "get_next_line.h"

int     main(int ac, char **av)
{
        int     fd;
        char    *line;

        fd = open(av[1], O_RDWR);
        while (get_next_line(fd, &line))
        {
                printf("|%d| %s\n", fd, line);
                free(line);
        }
        printf("|%d| %s", fd, line);
        return (0);
}
```
