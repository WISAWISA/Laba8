#include <stdio.h>

#define YES 1

#define NO 0

#define gets(a) fgets(a, sizeof(a), stdin)

int main()

{

char arr[1000];

char *str;

char *start;

char *del;

int cnt;

int flag;

gets(arr);

str = arr;

start = arr;

cnt = 0;

flag = NO;

while( *str != '\0' )

{

if( (*str < 'a' || *str > 'z') && (*str < 'A' || *str > 'Z') )

{

if( (flag == YES) && (cnt % 2 == 1) )

{

del = start;

while( *del++ = *str++ );

str = start;

cnt = 0;

}

flag = NO;

}

else

{

if( flag == NO )

start = str;

cnt++;

flag = YES;

}

str++;

}

puts(arr);

getchar();

return 0;

}
