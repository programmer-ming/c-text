# c-text

int main(void)
{
    char sex;
    char sports;
    char diet;
    float myHeight;
    float faHeight;
    float moHeight;
    printf("Are you a boy(M) or a girl(F)?");
    scanf(" %c", &sex);
    printf("Please input your father's height(cm):");
    scanf("%f", &faHeight);
    printf("Please input your mother's height(cm):");
    scanf("%f", &moHeight);
    printf("Do you like sports(Y/N)?");
    scanf(" %c", &sports);
    printf("Do you have a good habit or a diet(Y/N)?");
    scanf(" %c", &diet);
    if(sex == 'M'|| sex == 'm')
        myHeight = (faHeight + moHeight) * 0.54;
    if(sex == 'F'|| sex == 'f')
        myHeight = (faHeight * 0.923 + moHeight)/2.0;
    if(sports == 'Y'|| sports == 'y')
        myHeight = myHeight * (1+0.02);
    if(diet == 'Y'|| diet == 'y')
        myHeight = myHeight * (1+0.015);
    printf("Your future height will be %f(cm)\n", myHeight);
    return 0;
}
