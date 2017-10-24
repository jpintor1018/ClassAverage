# TestAverage

#include <iostream>

using namespace std;

int main()

{

    int num,num2=0, num3=0,num4=0,t ;
    double test[25], sum=0, average;
    char name[20];

    cout<<"Enter how many students\n";
    cin>>num;
    for(int a=0; a<num; a++)
        {
            cout<<"Enter Student's Name\n";
            cin>>name;
            cout<<"Enter Test Score\n";
            cin>>test[a];
            sum=sum+test[a];
        }
            average=sum/num;
            cout<<"Class average is: "<<average<<endl;
            for(int a=0;a<num;a++)
                {
                    if(test[a]<average)
                        num2=num2+1;
                    else
                        cout<<endl;
                }
                for(int a=0;a<num;a++)
                    {
                        if (test[a]>=average)
                            num3=num3+1;
                        else
                            cout<<endl;
                    }

    cout<<"Number of Students whose test scores are below average: "<<num2<<endl;
    cout<<"Number of students whose test scores are above average: "<<num3<<endl;

                for (int a=0;a<num;a++)
                    {
                        for (int b=num-1;b>=a;b--)
                        {


                             if (test[b-1]>test[b])
                                    {
                                         {


                                      t=test[b-1];
                                      test[b-1]=test[b];
                                      test[b]=t;
                                         }
                                    }
                         }


                    }
                    for ( t=0;t<num; t++)
                        cout<<test[t];

}

