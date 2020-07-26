#include <stdio.h>
#include <cs50.h>

int main(void)
{
    printf("<학점 계산 프로그램>\n종료를 원하면 '-1'을 입력하세요.\n");
    printf("점수: 95   90   85   80   75   70   65   60   0\n학점: A+   A    B+   B    C+   C    D+   D    F\n");
    
    for(int i = 0; true; i++)
    {
        float point = get_float("성적을 입력하세요. (0 ~ 100) : ");
        
        if(point == -1)
        {
            printf("학점프로그램을 종료합니다.\n");
            break;
        }
        else if(point > 100 || point < 0 )
        {
            printf("** %.0f 성적을 올바르게 입력하세요. 범위는 0 ~ 100 입니다.\n", point);
        }
        else if(point >= 95)
        {
            printf("학점은 A+입니다.\n");
        }
        else if(point >= 90)
        {
            printf("학점은 A입니다.\n");
        }
        else if(point >= 85)
        {
            printf("학점은 B+입니다.\n");
        }
        else if(point >= 80)
        {
            printf("학점은 B입니다.\n");
        }
        else if(point >= 75)
        {
            printf("학점은 C+입니다.\n");
        }
        else if(point >= 70)
        {
            printf("학점은 D+입니다.\n");
        }
        else if(point >= 65)
        {
            printf("학점은 D입니다.\n");
        }
        else
        {
            printf("학점은 F입니다.\n");
        }
    }
}
