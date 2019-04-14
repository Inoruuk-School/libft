# LIBFT

## 1 Fonctions obligatoire

• memset
• bzero
• memcpy
• memccpy
• memmove
• memchr
• memcmp
• strlen
• strdup
• strcpy
• strncpy
• strcat
• strncat
• strlcat
• strchr
• strrchr
• strstr
• strnstr
• strcmp
• strncmp
• atoi
• isalpha
• isdigit
• isalnum
• isascii
• isprint
• toupper
• tolower

## 2 Fonctions supplémentaires

• ft_memalloc
Prototype void * ft_memalloc(size_t size);
Description Alloue (avec malloc(3)) et retourne une zone de mémoire
“fraiche”. La mémoire allouée est initialisée à 0. Si l’allocation
échoue, la fonction renvoie NULL.
Param. #1 La taille de la zone de mémoire à allouer.
Retour La zone de mémoire allouée.
Fonctions libc malloc(3)

• ft_memdel
Prototype void ft_memdel(void **ap);
Description Prend en paramètre l’adresse d’un pointeur dont la zone pointée doit être libérée avec free(3), puis le pointeur est mis à
NULL.
Param. #1 L’adresse d’un pointeur dont il faut libérer la mémoire puis le
mettre à NULL.
Retour Rien.
Fonctions libc free(3).

• ft_strnew
Prototype char * ft_strnew(size_t size);
Description Alloue (avec malloc(3)) et retourne une chaîne de caractère
“fraiche” terminée par un ’\0’. Chaque caractère de la chaîne
est initialisé à ’\0’. Si l’allocation echoue, la fonction renvoie
NULL.
Param. #1 La taille de la chaîne de caractères à allouer.
Retour La chaîne de caractères allouée et initialisée à 0.
Fonctions libc malloc(3)

• ft_strdel
Prototype void ft_strdel(char **as);
Description Prend en paramètre l’adresse d’une chaîne de caractères qui
doit être libérée avec free(3) et son pointeur mis à NULL.
Param. #1 L’adresse de la chaîne de caractère dont il faut libérer la mémoire et mettre le pointeur à NULL.
Retour Rien.
Fonctions libc Free(3).

• ft_strclr
Prototype void ft_strclr(char *s);
Description Assigne la valeur ’\0’ à tous les caractères de la chaîne passée
en paramètre.
Param. #1 La chaîne de caractères à clearer.
Retour Rien.
Fonctions libc Aucune.

• ft_striter
Prototype void ft_striter(char *s, void (*f)(char *));
Description Applique la fonction f à chaque caractère de la chaîne de
caractères passée en paramètre. Chaque caractère est passé
par adresse à la fonction f afin de pouvoir être modifié si
nécessaire.
Param. #1 La chaîne de caractères sur laquelle itérer.
Param. #2 La fonction à appeler sur chaque caractère de s.
Retour Rien.
Fonctions libc Aucune.

• ft_striteri
Prototype void ft_striteri(char *s, void (*f)(unsigned int,
char *));
Description Applique la fonction f à chaque caractère de la chaîne de
caractères passée en paramètre en précisant son index en premier argument. Chaque caractère est passé par adresse à la
fonction f afin de pouvoir être modifié si nécessaire.
Param. #1 La chaîne de caractères sur laquelle itérer.
Param. #2 La fonction à appeler sur chaque caractère de s et son index.
Retour Rien.
Fonctions libc Aucune.

• ft_strmap
Prototype char * ft_strmap(char const *s, char (*f)(char));
Description Applique la fonction f à chaque caractère de la chaîne de caractères passée en paramètre pour créer une nouvelle chaîne
“fraiche” (avec malloc(3)) résultant des applications successives de f.
Param. #1 La chaîne de caractères sur laquelle itérer.
Param. #2 La fonction à appeler sur chaque caractère de s.
Retour La chaîne “fraiche” résultant des applications successives de f.
Fonctions libc malloc(3)

• ft_strmapi
Prototype char * ft_strmapi(char const *s, char
(*f)(unsigned int, char));
Description Applique la fonction f à chaque caractère de la chaîne de
caractères passée en paramètre en précisant son index pour
créer une nouvelle chaîne “fraiche” (avec malloc(3)) résultant
des applications successives de f.
Param. #1 La chaîne de caractères sur laquelle itérer.
Param. #2 La fonction à appeler sur chaque caractère de s en précisant son index.
Retour La chaîne “fraiche” résultant des applications successives de

• ft_strequ
Prototype int ft_strequ(char const *s1, char const *s2);
Description Compare lexicographiquement s1 et s2. Si les deux chaînes
sont égales, la fonction retourne 1, ou 0 sinon.
Param. #1 La première des deux chaînes à comparer.
Param. #2 La seconde des deux chaînes à comparer.
Retour 1 ou 0 selon que les deux chaînes sont égales ou non.
Fonctions libc Aucune.

• ft_strnequ
Prototype int ft_strnequ(char const *s1, char const *s2,
size_t n);
Description Compare lexicographiquement s1 et s2 jusqu’à n caractères
maximum ou bien qu’un ’\0’ ait été rencontré. Si les deux
chaînes sont égales, la fonction retourne 1, ou 0 sinon.
Param. #1 La première des deux chaînes à comparer.
Param. #2 La seconde des deux chaînes à comparer.
Param. #3 Le nombre de caractères à comparer au maximum.
Retour 1 ou 0 selon que les deux chaînes sont égales ou non.
Fonctions libc Aucune.

• ft_strsub
Prototype char * ft_strsub(char const *s, unsigned int
start, size_t len);
Description Alloue (avec malloc(3)) et retourne la copie “fraiche” d’un
tronçon de la chaîne de caractères passée en paramètre. Le
tronçon commence à l’index start et a pour longueur len. Si
start et len ne désignent pas un tronçon de chaîne valide,
le comportement est indéterminé. Si l’allocation échoue, la
fonction renvoie NULL.
Param. #1 La chaîne de caractères dans laquelle chercher le tronçon à
copier.
Param. #2 L’index dans la chaîne de caractères où débute le tronçon à
copier.
Param. #3 La longueur du tronçon à copier.
Retour Le tronçon.
Fonctions libc malloc(3)

• ft_strjoin
Prototype char * ft_strjoin(char const *s1, char const
*s2);
Description Alloue (avec malloc(3)) et retourne une chaîne de caractères
“fraiche” terminée par un ’\0’ résultant de la concaténation
de s1 et s2. Si l’allocation echoue, la fonction renvoie NULL.
Param. #1 La chaîne de caractères préfixe.
Param. #2 La chaîne de caractères suffixe.
Retour La chaîne de caractère “fraiche” résultant de la concaténation des deux chaînes.
Fonctions libc malloc(3)

• ft_strtrim
Prototype char * ft_strtrim(char const *s);
Description Alloue (avec malloc(3)) et retourne une copie de la chaîne
passée en paramètre sans les espaces blancs au debut et à la
fin de cette chaîne. On considère comme espaces blancs les
caractères ’ ’, ’\n’ et ’\t’. Si s ne contient pas d’espaces
blancs au début ou à la fin, la fonction renvoie une copie de
s. Si l’allocation echoue, la fonction renvoie NULL.
Param. #1 La chaîne de caractères à trimmer.
Retour La chaîne de caractère “fraiche” trimmée ou bien une copie de s sinon.
Fonctions libc malloc(3)

• ft_strsplit
Prototype char ** ft_strsplit(char const *s, char c);
Description Alloue (avec malloc(3)) et retourne un tableau de chaînes de
caractères “fraiches” (toutes terminées par un ’\0’, le tableau
également donc) résultant de la découpe de s selon le caractère
c. Si l’allocation echoue, la fonction retourne NULL. Exemple :
ft_strsplit("*salut*les***etudiants*", ’*’) renvoie
le tableau ["salut", "les", "etudiants"].
Param. #1 La chaîne de caractères à découper.
Param. #2 Le caractère selon lequel découper la chaîne.
Retour Le tableau de chaînes de caractères “fraiches” résultant de la découpe.
Fonctions libc malloc(3), free(3)

• ft_itoa
Prototype char * ft_itoa(int n);
Description Alloue (avec malloc(3)) et retourne une chaîne de caractères
“fraiche” terminée par un ’\0’ représentant l’entier n passé
en paramètre. Les nombres négatifs doivent être gérés. Si l’allocation échoue, la fonction renvoie NULL.
Param. #1 L’entier à convertir en une chaîne de caractères.
Retour La chaîne de caractères représentant l’entier passé en paramètre.
Fonctions libc malloc(3)

• ft_putchar
Prototype void ft_putchar(char c);
Description Affiche le caractère c sur la sortie standard.
Param. #1 Le caractère à afficher.
Retour Rien.
Fonctions libc write(2).

• ft_putstr
Prototype void ft_putstr(char const *s);
Description Affiche la chaîne s sur la sortie standard.
Param. #1 La chaîne de caractères à afficher.
Retour Rien.
Fonctions libc write(2).

• ft_putendl
Prototype void ft_putendl(char const *s);
Description Affiche la chaîne s sur la sortie standard suivi d’un ’\n’.
Param. #1 La chaîne de caractères à afficher.
Retour Rien.
Fonctions libc write(2).

• ft_putnbr
Prototype void ft_putnbr(int n);
Description Affiche l’entier n sur la sortie standard.
Param. #1 L’entier à afficher.
Retour Rien.
Fonctions libc write(2).

• ft_putchar_fd
Prototype void ft_putchar_fd(char c, int fd);
Description Ecrit le caractère c sur le descripteur de fichier fd.
Param. #1 Le caractères à écrire.
Param. #2 Le descripteur de fichier.
Retour Rien.
Fonctions libc write(2).

• ft_putstr_fd
Prototype void ft_putstr_fd(char const *s, int fd);
Description Ecrit la chaîne s sur le descripteur de fichier fd.
Param. #1 La chaîne de caractères à écrire.
Param. #2 Le descripteur de fichier.
Retour Rien.
Fonctions libc write(2).

• ft_putendl_fd
Prototype void ft_putendl_fd(char const *s, int fd);
Description Ecrit la chaîne s sur le descripteur de fichier fd suivi d’un
’\n’.
Param. #1 La chaîne de caractères à écrire.
Param. #2 Le descripteur de fichier.
Retour Rien.
Fonctions libc write(2).

• ft_putnbr_fd
Prototype void ft_putnbr_fd(int n, int fd);
Description Ecrit l’entier n sur le descripteur de fichier fd.
Param. #1 L’entier à écrire.
Param. #2 Le descripteur de fichier.
Retour Rien.
Fonctions libc write(2).

## 3 Fonction Bonus 

• ft_lstnew
Prototype t_list * ft_lstnew(void const *content, size_t
content_size);
Description Alloue (avec malloc(3)) et retourne un maillon “frais”. Les
champs content et content_size du nouveau maillon sont
initialisés par copie des paramètres de la fonction. Si le paramètre content est nul, le champs content est initialisé à
NULL et le champs content_size est initialisé à 0 quelque
soit la valeur du paramètre content_size. Le champ next
est initialisé à NULL. Si l’allocation échoue, la fonction renvoie
NULL.
Param. #1 Le contenu à ajouter au nouveau maillon.
Param. #2 La taille du contenu à ajouter au nouveau maillon.
Retour Le nouveau maillon.
Fonctions libc malloc(3), free(3)

• ft_lstdelone
Prototype void ft_lstdelone(t_list **alst, void (*del)(void
*, size_t));
Description Prend en paramètre l’adresse d’un pointeur sur un maillon et
libère la mémoire du contenu de ce maillon avec la fonction
del passée en paramètre puis libère la mémoire du maillon
en lui même avec free(3). La mémoire du champ next ne
doit en aucun cas être libérée. Pour terminer, le pointeur sur
le maillon maintenant libéré doit être mis à NULL (de manière
similaire à la fonction ft_memdel de la partie obligatoire).
Param. #1 L’adresse d’un pointeur sur le maillon à libérer.
Retour Rien.
Fonctions libc free(3)

• ft_lstdel
Prototype void ft_lstdel(t_list **alst, void (*del)(void *,
size_t));
Description Prend en paramètre l’adresse d’un pointeur sur un maillon et
libère la mémoire de ce maillon et celle de tous ses successeurs l’un après l’autre avec del et free(3). Pour terminer,
le pointeur sur le premier maillon maintenant libéré doit être
mis à NULL (de manière similaire à la fonction ft_memdel de
la partie obligatoire).
Param. #1 L’adresse d’un pointeur sur le premier maillon d’une liste à
libérer.
Retour Rien.
Fonctions libc free(3)

• ft_lstadd
Prototype void ft_lstadd(t_list **alst, t_list *new);
Description Ajoute l’élément new en tête de la liste.
Param. #1 L’adresse d’un pointeur sur le premier maillon d’une liste.
Param. #2 Le maillon à ajouter en tête de cette liste.
Retour Rien.
Fonctions libc Aucune.

• ft_lstiter
Prototype void ft_lstiter(t_list *lst, void (*f)(t_list
*elem));
Description Parcourt la liste lst en appliquant à chaque maillon la fonction f.
Param. #1 Pointeur sur le premier maillon d’une liste.
Param. #2 L’adresse d’une fonction à laquelle appliquer chaque maillon
de la liste.
Retour Rien.
Fonctions libc Aucune.

• ft_lstmap
Prototype t_list * ft_lstmap(t_list *lst, t_list *
(*f)(t_list *elem));
Description Parcourt la liste lst en appliquant à chaque maillon la fonction f et crée une nouvelle liste “fraiche” avec malloc(3) résultant des applications successives. Si une allocation échoue,
la fonction renvoie NULL.
Param. #1 Pointeur sur le premier maillon d’une liste.
Param. #2 L’adresse d’une fonction à appliquer à chaque maillon de la
liste pour créer une nouvelle liste.
Retour La nouvelle liste.
Fonctions libc malloc(3), free(3).

