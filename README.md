# Quzi-in-c-programing
I’m currently learning C programming 💻 and built a console-based quiz application. As a beginner 🌱, this project strengthened my understanding of core concepts like variables, arrays, loops, and conditionals 🧠. I focused on learning the logic behind the code and growing step by step 🚀


```
#include <stdio.h>
int main()
{
    int set_num;
    int mgiven[10],pgiven[10],cgiven[10];
    int mans[10]={2,2,3,3,4,2,4,3,2,3},pans[10]={3,2,2,3,4,3,2,3,4,3},cans[10]={3,3,3,3,2,3,3,3,3,3};
    int mmark=0,pmark=0,cmark=0;
    printf("ATTEND ALL THE SET\nALL THE BEST\n");
    again:
    printf("ENTER 1 FOR SET 1 - MATHS\nENTER 2 FOR SET 2 - PHYSICS\nENTER 3 FOR SET 3 - CHEMISTRY\n");
    scanf("%d",&set_num);
    if (set_num==1)
    {
        int mconfirm;
        printf("YOU HAVE SELECTED MATHS \nTO CONTINUE PRESS 1 \nTO CHANGE SET ENTER 0\n");
        scanf("%d",&mconfirm);
        switch(mconfirm)
        {
            case 1:
            {
                printf("----------Maths Questions----------\n");
                printf("Q1. The value of 7^0 is\n1) 0  2) 1  3) 7  4) Undefined\n");
                printf("Q2. Which of the following is a prime number?\n1) 21  2) 29  3) 51  4) 39\n");
                printf("Q3. Sum of first 10 natural numbers is\n1) 45  2) 50  3) 55  4) 60\n");
                printf("Q4. Square root of 144 is\n1) 10  2) 11  3) 12  4) 13\n");
                printf("Q5. Triangle with all sides equal is\n1) Right  2) Scalene  3) Isosceles  4) Equilateral\n");
                printf("Q6. The value of 2^5 is\n1) 16  2) 32  3) 64  4) 128\n");
                printf("Q7. Which is an even number?\n1) 13  2) 17  3) 21  4) 24\n");
                printf("Q8. Perimeter of square with side 5 cm is\n1) 10  2) 15  3) 20  4) 25\n");
                printf("Q9. Decimal form of 1/4 is\n1) 0.2  2) 0.25  3) 0.4  4) 0.5\n");
                printf("Q10. Which number is divisible by 9?\n1) 234  2) 512  3) 918  4) 407\n");
                mstart:
                printf("ENTER ANSWER\n");
                for (int i=0;i<10;i++)
                {
                    scanf("%d",&mgiven[i]);
                }
                for (int i=0;i<10;i++)
                {
                    if (mgiven[i]<0 || mgiven[i]>4)
                    {
                        printf("ENTER ONLY THE OPTIONS NUMBER\n");
                        goto  mstart;
                    }
                    else  if (mgiven[i]==mans[i])
                        mmark++;
                }
                printf("MATHS MARK = %d\n",mmark);
                printf("TO CONTINUE WITH OTHER EXAM ENTER 1 OR TO END EXAM ENTER 0\n");
                int mend;
                scanf("%d",&mend);
                switch (mend)
                {
                    case 1:
                        goto again;
                    case 0:
                        goto endmark;
                }
                break;
            }
            case 0:
            {
                goto again;
            }
            default :
           {
                printf("TO CONTINUE PRESS 1 \nTO CHANGE SET ENTER 0\n");
                break;
            }
        }

    }
    else if (set_num==2)
    {
        int pconfirm;
        printf("YOU HAVE SELECTED PHYSICS \nTO CONTINUE PRESS 1 \nTO CHANGE SET ENTER 0\n");
        scanf("%d",&pconfirm);
        switch(pconfirm)
        {
            case 1:
            {
                printf("----------Physics Questions----------\n");
                printf("Q1. SI unit of force\n1) Joule  2) Pascal  3) Newton  4) Watt\n");
                printf("Q2. Electrical to mechanical energy\n1) Generator  2) Motor  3) Transformer  4) Battery\n");
                printf("Q3. Speed is\n1) D×T  2) D/T  3) T/D  4) F/M\n");
                printf("Q4. Unit of electric current\n1) Volt  2) Ohm  3) Ampere  4) Coulomb\n");
                printf("Q5. Highest energy light\n1) Red  2) Yellow  3) Green  4) Violet\n");
                printf("Q6. Force pulling objects to earth\n1) Magnetic  2) Electrostatic  3) Gravitational  4) Nuclear\n");
                printf("Q7. SI unit of work\n1) Watt  2) Joule  3) Newton  4) Pascal\n");
                printf("Q8. Renewable energy source\n1) Coal  2) Petrol  3) Wind  4) Diesel\n");
                printf("Q9. Speed of light max in\n1) Water  2) Glass  3) Air  4) Vacuum\n");
                printf("Q10. Temperature measuring instrument\n1) Barometer  2) Ammeter  3) Thermometer  4) Voltmeter\n");
                pstart:
                printf("ENTER ANSWER\n");
                for (int i=0;i<10;i++)
                {
                    scanf("%d",&pgiven[i]);
                }
                for (int i=0;i<10;i++)
                {
                    if (pgiven[i]<0 || pgiven[i]>4)
                    {
                        printf("ENTER ONLY THE OPTIONS NUMBER\n");
                        goto  pstart;
                    }
                    else  if (pgiven[i]==pans[i])
                        pmark++;
                }
                printf("MATHS MARK = %d\n",pmark);
                printf("TO CONTINUE WITH OTHER EXAM ENTER 1 OR TO END EXAM ENTER 0\n");
                int pend;
                scanf("%d",&pend);
                switch (pend)
                {
                    case 1:
                        goto again;
                    case 0:
                        goto endmark;
                }
                break;
            }
            case 0:
            {
                goto again;
            }
            default :
           {
                printf("TO CONTINUE PRESS 1 \nTO CHANGE SET ENTER 0\n");
                break;
            }
        }

    }
    else if (set_num==3)
    {
        int cconfirm;
        printf("YOU HAVE SELECTED CHEMISTRY\nTO CONTINUE PRESS 1 \nTO CHANGE SET ENTER 0\n");
        scanf("%d",&cconfirm);
        switch(cconfirm)
        {
            case 1:
            {
                printf("----------Chemistry Questions----------\n");
                printf("Q1. Symbol of Sodium\n1) So  2) S  3) Na  4) N\n");
                printf("Q2. Gas needed for respiration\n1) Nitrogen  2) CO2  3) Oxygen  4) Hydrogen\n");
                printf("Q3. pH of pure water\n1) 5  2) 6  3) 7  4) 8\n");
                printf("Q4. Noble gas\n1) Oxygen  2) Nitrogen  3) Helium  4) Hydrogen\n");
                printf("Q5. Rusting of iron is\n1) Reduction  2) Oxidation  3) Neutralization  4) Evaporationt\n");
                printf("Q6. Main component of LPG\n1) Methane  2) Ethane  3) Propane  4) CO2\n");
                printf("Q7. Acid in lemon\n1) Acetic  2) HCl  3) Citric  4) Sulphuricl\n");
                printf("Q8. Liquid metal\n1) Iron  2) Copper  3) Mercury  4) Aluminium\n");
                printf("Q9. Smallest unit of element\n1) Molecule  2) Compound  3) Atom  4) Ion\n");
                printf("Q10. Gas turning lime water milky\n1) Oxygen  2) Nitrogen  3) CO2  4) Hydrogen\n");
                cstart:
                printf("ENTER ANSWER\n");
                for (int i=0;i<10;i++)
                {
                    scanf("%d",&cgiven[i]);
                }
                for (int i=0;i<10;i++)
                {
                    if (cgiven[i]<0 || cgiven[i]>4)
                    {
                        printf("ENTER ONLY THE OPTIONS NUMBER\n");
                        goto  cstart;
                    }
                    else  if (cgiven[i]==cans[i])
                        cmark++;
                }
                printf("CHEMISTRY MARK = %d\n",cmark);
                printf("TO CONTINUE WITH OTHER EXAM ENTER 1 OR TO END EXAM ENTER 0\n");
                int cend;
                scanf("%d",&cend);
                switch (cend)
                {
                    case 1:
                        goto again;
                    case 0:
                        goto endmark;
                }
                break;
            }
            case 0:
            {
                goto again;
            }
            default :
           {
                printf("TO CONTINUE PRESS 1 \nTO CHANGE SET ENTER 0\n");
                break;
            }
        }

    }


    endmark:
    printf("----------TOTAL MARKS----------\n");
    printf("%d / 30\n",mmark+pmark+cmark);
    return 0;
}
```
## OUTPUT
<img width="1852" height="1062" alt="5" src="https://github.com/user-attachments/assets/6fd568fd-caab-442c-b92c-a75586412fb5" />
<img width="1834" height="990" alt="6" src="https://github.com/user-attachments/assets/9bb6b95e-ed22-489b-9553-d35095e276fb" />
<img width="1838" height="383" alt="7" src="https://github.com/user-attachments/assets/3a9bd86c-b0eb-42f9-8f15-91b34e9a6c38" />

