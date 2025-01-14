//c++ game created by mamazi😄
/************************************/
/* fig: mamazio game                */
/* By: mamazi               */
/************************************/
#include <stdio.h>
#include <conio.h>
#include <iostream>
#include <ctype.h>
#include <time.h>
#include <string.h>
#include <windows.h>
using namespace std;


int NumbersOfG=0;
int NUMS=0; 

//________________________________________________
void printMainMenu()
{

  	 cout<<"  ** * * * * * * * * * * * * * * * * * * * * * * * * * * * **"<<endl;     
     cout<<"  *                                                         *"<<endl;
	 cout<<"  *                     "<<char (218)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (191)<<"                      *"<<endl;
     cout<<"  *";
	 for( int tt=1;tt<22;tt++)
		 cout<<char (196);
	 cout<<char (179)<<"  mini game "<<char (179);
 for(int tt=1;tt<23;tt++)
		 cout<<char (196);
    	 cout<<"*\n  *                     "<<char(192)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (196)<<char (217)<<"                      *"<<endl;


	 
     cout<<"  *                                                         *"<<endl;
     cout<<"  ** * * * * * * * * * * * * * * * * * * * * * * * * * * * **"<<endl;
}
    
//________________________________________________
void printCredits()
{
     system("cls");
     int CREDIT_NUMS=50;
     char* creditln1=new char[CREDIT_NUMS];
     printMainMenu();
     creditln1="\n\tpooya mini game (hads kalamat)\n\tversion:1.0.0\n\tsakhte shode tavasot:\t\t  pooya hpx\n\n\t soalat khod ra be email ma ersal konid :  \n\n\t\t\t\t   pooyahplife@gmail.com\n\n\t\t\t\t    \n";
     for(int i=0;i<strlen( creditln1);i++)
     {
             cout<<creditln1[i];
             Sleep(20);
     }
     cout<<"\n\t   ";
     system("pause");
}
//________________________________________________
bool areEqual(char* string1,char* string2)
{
     bool result=true;
     if(strlen(string1)==strlen(string2))
     {
        for(int i=0;i<strlen(string1) && i<strlen(string2);i++)
        {
            if(string1[i]!=string2[i])
            {
                 result=false;
            }
        }
     }  
     else
     {
         result=false;
     }
     return result;
}
//________________________________________________
bool isCharacterOf(char character,char *string)
{
     bool ico=false;
     for(int i=0;i<strlen(string);i++)
             if(toupper(string[i])==toupper(character))
                ico=true;
     return ico;
}

//________________________________________________
int *findTarget(char character,char *string)
{
    int t=0;
    for(int i=0;i<strlen(string);i++)
            if(toupper(string[i])==toupper(character))
                t++;
    int *a=new int[t];
    NUMS=t;
    t=0;
    for(int i=0;i<strlen(string);i++)
    {
            if(toupper(string[i])==toupper(character))
            {
                 a[t]=i;
                 t++;
            }
    }
    return a;
}

//________________________________________________
void meno(){
    cout<<"  *                                                         *\n  *  yek gozine ra baraye edame entekhab konid?!!                            *"<<endl;
    cout<<"  *                                                         *"<<endl;
    cout<<"  *   1.hads kalmat                                     *"<<endl;
    cout<<"  *   2.bazi 101                                      *"<<endl;
	cout<<"  *   3.Darbareye ma                                           *"<<endl;
    cout<<"  *   yek dokmee ra baraye khorj negah darid                            *"<<endl;
    cout<<"  *                                                         *"<<endl;
    cout<<"  ** * * * * * * * * * * * * * * * * * * * * * * * * * * * **"<<endl;
    cout<<"      ";}

//_________________________________________________
void welcome(char ww[10])
{
	        for(int tt2=47;tt2>25;tt2--)
	{
        cout<<"\n\n\n\n\n\n\n\n\n\n";
		for(int tt1=tt2;tt1>0;tt1--)
		             cout<<char (0);	
        cout<<ww;
	    Sleep(70);
		system("cls");
	}
Sleep(300);
system("cls");
Sleep(400);
}


//====================================================================================================================
//====================================================================================================================


int main()
{
    srand(time(NULL));
	char** words=new char*[70];
    for(int i=0;i<50;i++)
    {
            words[i]=new char[70];
    }
//----------------------------------------------------------------------------------------------------------------------------------
	words[0]="mother_board";words[1]="keyboard";words[2]="mouse";words[3]="monitor";words[4]="modem";
    words[5]="peugeot";words[6]="ferrari";words[7]="mclaren";words[8]="mitsubishi";words[9]="jaguar";words[10]="bugatti";words[11]="Lamborghini";words[12]="Chevrolet";words[13]="Audi";words[14]="toyota";words[15]="Viper";words[16]="mercedes-benz";
    words[16]="Afghanistan";words[17]="Albania";words[18]="Algeia";words[19]="America";words[20]="Angola";words[21]="Argentina";words[22]="Armenia";words[23]="Australia";words[24]="Azerbaijan";words[25]="Bangladesh";words[26]="Belarus";words[27]="Belgium";words[28]="Benin";words[29]="Bolivia";words[30]="Bosnia_Herzegovina";words[31]="Brazil";words[32]="Britain";words[33]="Bulgaria";words[34]="Cameroon";words[35]="Canada";
    words[36]="sheraz";words[37]="rasht";words[38]="oshnaveyeh";words[39]="tehran";words[40]="tabriz";words[41]="boshehr";words[42]="sari";words[43]="gorgan";words[44]="sanandaj";words[45]="mhabad";words[46]="saghez";words[47]="sardasht";
    words[48]="c++";words[49]="java";words[50]="asp.net";words[51]="vb.net";words[52]="delphi";words[53]="pascal";words[54]="visual_basic";words[55]="basic";
//----------------------------------------------------------------------------------------------------------------------------------

 
   	welcome("mohammadrezaio game loading...");	
	int fails=0;
    int ans2;
    int rnd;
    char ch1;
    char word[27];
    
                      int save1,save2;
		               char key1[2]="y";
				      int key;
                      char *tahera=new char[40];
					  int tt1;
					  int rnd2;

    MainMenu:
    system("cls");
    printMainMenu();
    int ans=0;
    meno();
    cin>>ans;
    switch(ans)
    {
//+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++               
	                case 1 : 
                        GetAnswer2:
                        NumbersOfG=0;
                        srand(time(NULL));
                        system("cls");
                        printMainMenu();
                        cout<<"     soalat darmord zir ast:"<<endl;
                        cout<<"     1.sakht afzar\n     2.mashin\n     3.keshvar ha\n     4.shahr ha\n     5.zaban haye barname nevisi     ";
                        cin>>ans2;
                       //________________________________________________________________
						switch(ans2)
                        {
                                    case 1: rnd=rand()%5;break;
                                    case 2: rnd=rand()%12+5;break;
                                    case 3: rnd=rand()%20+16;break;
                                    case 4: rnd=rand()%11+36;break;
									case 5: rnd=rand()%7+48;break;
									default :cout<<"     adad  1 , 2 , 3 , 4 or 5 entekhab konid\n";
                                            system("pause");
                                            goto GetAnswer2;
                                            break;
                        }
                       //_________________________________________________________________ 
						unsigned int n;
                        for (n=0; n<strlen(words[rnd]); n++) word[n]='-';
                        word[n]='\0';
                        fails=strlen(words[rnd])*2-n/2;
                        while(fails>0)
                        {
                                
                                system("cls");
                                printMainMenu();
                                if(!(isCharacterOf('-',word)))
                                {
                                     cout<<endl<<"     "<<word<<"\n";
                                     
									 
																
							         char *taher1=new char[40];
							
						        	taher1=" khyli khoob bood shooma barande shodid.\n";
							        cout<<"\n\n\n\n           ";
					        		for(int t1=0;t1<40;t1++){
					         		cout<<taher1[t1];
						        	Sleep(50);}
						         	cout<<"\n\n\n\n\n\n                          ";		
						        	system("pause");					
                                    goto MainMenu;
                                }
                                cout<<endl<<"     "<<word<<"\n";
                                cout<<"\n     horof mored nazer khod ra vared konid: (forsat haye khata"<<fails<<")" ;
                                cin>>ch1;
                                findTarget(ch1,words[rnd]);
                                if(isCharacterOf(ch1,words[rnd]))
                                        for(int i=0;i<NUMS;i++)
                                        {
                                                if(word[findTarget(ch1,words[rnd])[i]]!=ch1)
                                                {
                                                       word[findTarget(ch1,words[rnd])[i]]=ch1;
                                                }
                                                else
                                                {
                                                     cout<<"     in mored ghblan entkhab shode.";getch();break;
                                                }
                                        }
                                else
                                        fails-=1;
                        }
                        if(fails==0)
                        {
                            system("cls");							
							char *taher=new char[20];
							
							taher="   GAME OVER\n    ";
							cout<<"\n\n\n\n\n\n\n\n\n\n\n                               ";
							for(int t1=0;t1<16;t1++){
							cout<<taher[t1];
							Sleep(100);}
							cout<<"\n\n\n\n\n\n\n\n\n\n\n                          ";		
							system("pause");						}
						 printCredits();
						goto MainMenu;
//++++++++++++++++++++++++++++++  101 Game  +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++               
				   case 2:                     
					  save1=0;
				      save2=0;
				   system("cls");
				   printMainMenu();
				   strcpy(key1,"y");
				   cout<<"\n           be bazi 101 khosh omadin\n  ";
                   cout<<"\t 1.shoro bazi 101\n \t   ya yek shomare ra baraye bargasht entekhab konid\n";
				   cin>>key;
				   if (key!=1 ) goto MainMenu;				 
				   system("pause");
				   while (!strcmp(key1,"y")){
				   system("cls");
				   printMainMenu();
				   rnd=rand()%99+1;
                   cout<<" adad jadid = "<<rnd<<endl;
				   save1+=rnd;
				   cout<<"\n jam adad shoma Number = "<<save1<<endl;
				   if (save1>101){ 
					cout<<"adad kharej shode 101 \n";
				   Sleep(2500);
				   goto lose;}
					   
				   cout<<"\n\n\n\t aya mikhahid in adad ra vared konid? !!!(y,n) : ";
				   cin>>key1;
				   }
                
//................................................................
                   system("pause");
                   system("cls");
				   printMainMenu();
				   cout<<"\n\t\t  bot adad ra vared kard.......\n\n";
                   srand(time(NULL));
				   rnd=rand()%99+1;
                   cout<<" adad jadid= "<<rnd<<endl;
				   save2+=rnd;
				   cout<<"\n jaam adad  = "<<save2<<endl;
                   Sleep(1000);
				   rnd2=rand()%3;
				   if (save2<40)
					   if(rnd2!=1){
						   Sleep(2000);
						   system("cls");
						   printMainMenu();
						   srand(time(NULL));
				           rnd=rand()%99+1;
                           cout<<" adad jadid= "<<rnd<<endl;
				           save2+=rnd;
				           cout<<"\n jaam adad  = "<<save2<<endl;
					   }

                    Sleep(1000);
				   rnd2=rand()%2;
				   if (save2<60)
					   if(rnd2==1){
						   Sleep(2000);
						   system("cls");
						   printMainMenu();
						   srand(time(NULL));
				           rnd=rand()%99+1;
                           cout<<" adad jadid= "<<rnd<<endl;
				           save2+=rnd;
				           cout<<"\n jaam adad  = "<<save2<<endl;
					   }
                      

					     Sleep(1000);
				   rnd2=rand()%4;
				   if (save2<80)
					   if(rnd2==1){
						   Sleep(2000);
						   system("cls");
						   printMainMenu();
						   srand(time(NULL));
				           rnd=rand()%99+1;
                           cout<<" adad jadid= "<<rnd<<endl;
				           save2+=rnd;
				           cout<<"\n jaam adad  = "<<save2<<endl;
					   }

	               Sleep(1000);
				   rnd2=rand()%6;
				   if (save2<90)
					   if(rnd2==1){
						   Sleep(2000);
						   system("cls");
						   printMainMenu();
						   srand(time(NULL));
				           rnd=rand()%99+1;
                           cout<<" adad jadid= "<<rnd<<endl;
				           save2+=rnd;
				           cout<<"\n jaam adad  = "<<save2<<endl;
					   }
					   
					   
					     Sleep(1000);
				   rnd2=rand()%2;
				   if (save2<60)
					   if(rnd2==1){
						   Sleep(2000);
						   system("cls");
						   printMainMenu();
						   srand(time(NULL));
				           rnd=rand()%99+1;
                           cout<<" adad jadid= "<<rnd<<endl;
				           save2+=rnd;
				           cout<<"\n jaam adad  = "<<save2<<endl;
					   }
					   
					   
					   
					   
					   if(save2>101){cout<<"adad kharej shode 101 ast  ...shoma barande shodid...";Sleep(3000);goto win;}
                   system("cls");
				   printMainMenu();
				   cout<<" jam adad shoma     = "<<save1<<endl;
				   cout<<" jam adad computer = "<<save2<<endl;
				   Sleep(1000);
				   if(save1>save2){
					   cout<<"\n\n\t emtiyaz shoma > emtiyaz computer\n\n\t ..........shoma barnde shodid........\n";
					   Sleep(4000);
					   goto win;
				   }
                   goto lose;
                  win:

				   system("cls");							
							
							tahera="   kheyli khobi bodi to barande shodi\n";
							cout<<"\n\n\n\n\n\n\n\n\n\n\n                   ";
							for( tt1=0;tt1<40;tt1++){
							cout<<tahera[tt1];
							Sleep(100);}
							cout<<"\n\n\n\n\n\n\n\n\n\n\n                          ";		
							system("pause");						
						 printCredits();
						goto MainMenu;
                   


                   system("pause");

				   goto MainMenu;
                   
                   lose:
				    system("cls");							
							
							
							tahera="   GAME OVER\n    ";
							cout<<"\n\n\n\n\n\n\n\n\n\n\n                               ";
							for( tt1=0;tt1<16;tt1++){
							cout<<tahera[tt1];
							Sleep(100);}
							cout<<"\n\n\n\n\n\n\n\n\n\n\n                          ";		
							system("pause");						
						 printCredits();
						goto MainMenu;
				   
				   break;
//+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++						
				case 3 :
                    printCredits();
                    goto MainMenu;
               default :
                       break;
    }
    welcome("khoda negah dar");
	return 0;
}
