#include <conio.h>
#include <fstream.h>
#include <string.h>
#include <stdlib.h>
#include <time.h>

char a, b, p[10], xyz[10];
int z, up, sh[10], sk[10], lh[10], lk[10];
int aa=0, bb=0, end, cdec, ca, cb;
char dis[100][3] = {
			"01", "02", "03", "04", "05",
			"06", "07", "08", "09",
			"10", "11", "12", "13", "14", "15",
			"16", "17", "18", "19",
			"20", "21", "22", "23", "24", "25",
			"26", "27", "28", "29",
			"30", "31", "32", "33", "34", "35",
			"36", "37", "38", "39",
			"40", "41", "42", "43", "44", "45",
			"46", "47", "48", "49",
			"50", "51", "52", "53", "54", "55",
			"56", "57", "58", "59",
			"60", "61", "62", "63", "64", "65",
			"66", "67", "68", "69",
			"70", "71", "72", "73", "74", "75",
			"76", "77", "78", "79",
			"80", "81", "82", "83", "84", "85",
			"86", "87", "88", "89",
			"90", "91", "92", "93", "94", "95",
			"96", "97", "98", "99",
			127,127
			};
int pos[100] = {3,0,0,0,0,0,0,0,0,0,
		0,0,0,0,0,0,0,0,0,0,
		0,0,0,0,0,0,0,0,0,0,
		0,0,0,0,0,0,0,0,0,0,
		0,0,0,0,0,0,0,0,0,0,
		0,0,0,0,0,0,0,0,0,0,
		0,0,0,0,0,0,0,0,0,0,
		0,0,0,0,0,0,0,0,0,0,
		0,0,0,0,0,0,0,0,0,0,
		0,0,0,0,0,0,0,0,0,0,
		 };


class snl
{
	public:
	int bno;
	int d[10], e[10], f[10], g[10], cha, chb, dmax, gmax;

	void chsna(int i)
	{       if(i<5)
		{
			cout<<"\nEnter Head of Snake"<<i+1<<" below 50: ";
			cin>>d[i];
		}
		else
		{
			cout<<"\nEnter Head of Snake"<<i+1<<" above 50: ";
			cin>>d[i];
		}
		cout<<"Enter Tail of Snake"<<i+1<<" : ";
		cin>>e[i];
	}

	void chlad(int i)
	{      if(i<5)
		{
			cout<<"\nEnter Base of Ladder"<<i+1<<" below 50: ";
			cin>>f[i];
		}
		else
		{
			cout<<"\nEnter Base of Ladder"<<i+1<<" above 50: ";
			cin>>f[i];
		}
		cout<<"Enter Peak of Ladder"<<i+1<<" : ";
		cin>>g[i];
	}

	void insna(int i)
	{
		chsna(i);
		if(d[i]<2 || d[i]>98 || e[i]<2 || e[i]>98)
		{
			cout<<"Wrong Input. All positions must lie ";
			cout<<"between 2 & 98. Try Again.\n";
			insna(i);
		}
		else if(d[i] - e[i] <1)
		{
			cout<<"Wrong Input. Head must be above the Tail. ";
			cout<<"Try Again.\n";
			insna(i);
		}
		else if(d[i] - e[i] <10)
		{
			cout<<"Wrong Input. Minimum length of snake must ";
			cout<<"be 10. Try Again.\n";
			insna(i);
		}
		else if(i<5 && d[i]>50)
		{
			cout<<"Wrong Input. Please enter head below 50. ";
			cout<<"Try Again.\n";
			insna(i);
		}
		else if(i>4 && d[i]<=50)
		{
			cout<<"Wrong Input. Please enter head above 50. ";
			cout<<"Try Again.\n";
			insna(i);
		}
	}

	void inlad(int i)
	{
		chlad(i);
		if(f[i]<2 || f[i]>98 || g[i]<2 || g[i]>98)
		{
			cout<<"Wrong Input. All positions must lie between ";
			cout<<"2 & 98. Try Again.\n";
			inlad(i);
		}
		else if(g[i] - f[i] <1)
		{
			cout<<"Wrong Input. Top must be above the Base. ";
			cout<<"Try Again.\n";
			inlad(i);
		}
		else if(g[i] - f[i] >30)
		{
			cout<<"Wrong Input. Maximum length of Ladder can ";
			cout<<"be 30. Try Again.\n";
			inlad(i);
		}
		else if(i<5 && f[i]>50)
		{
			cout<<"Wrong Input. Please enter Base below 50. ";
			cout<<"Try Again.\n";
			inlad(i);
		}
		else if(i>4 && f[i]<=50)
		{
			cout<<"Wrong Input. Please enter Base above 50. ";
			cout<<"Try Again.\n";
			inlad(i);
		}
	}

	void chall()
	{
		cha=0;
		chb=0;
		dmax=0;
		gmax=0;
		for(int i=0; i<10; i++)
		{
			insna(i);
		}
		for(int j=0; j<10; j++)
		{
			inlad(j);
		}
		for(int q=0; q<10; q++)
		{
			for(int r=q+1; r<10; r++)
			{
				if(d[q] == d[r])
				{
					cha = 1;
				}
				else if(f[q] == f[r])
				{
					cha = 1;
				}
			}
		}
		for(int qq=0; qq<10; qq++)
		{
			for(int rr=0; rr<10; rr++)
			{
				if(d[qq] == f[rr])
				{
					cha = 1;
				}
				else if(e[qq] == f[rr])
				{
					cha = 1;
				}
				else if(d[qq] == g[rr])
				{
					cha = 1;
				}
			}
		}
		for(int sl=0; sl<10; sl++)
		{
			if(d[sl] > dmax)
			{
				dmax = d[sl];
			}
			if(g[sl] > gmax)
			{
				gmax = g[sl];
			}
		}
		if(gmax > dmax)
		{
			chb=1;
		}
		if(cha==1)
		{
			clrscr();
			cout<<"\n Wrong Input. No 2 positions (Base, Head).";
			cout<<"\n Or Ladder and Snake make Loop. ";
			cout<<"Try Again. \n";
			chall();
		}
		else if(chb==1)
		{
			clrscr();
			cout<<"\n Wrong Input. There must be atleast ";
			cout<<"1 Snake after";
			cout<<"\n the last Ladder. Try Again. \n";
			chall();
		}
	}

	void getsnl()
	{
		char o[10];
		cout<<"\nEnter Board Number.\n";
		cin>>o;
		if(strcmp(o,"0") == 0)
		{
			bno=0;
			chall();
		}
		else if(strcmp(o,"1") == 0)
		{
			bno=1;
			chall();
		}
		else if(strcmp(o,"2") == 0)
		{
			bno=2;
			chall();
		}
		else if(strcmp(o,"3") == 0)
		{
			bno=3;
			chall();
		}
		else if(strcmp(o,"4") == 0)
		{
			bno=4;
			chall();
		}
		else if(strcmp(o,"5") == 0)
		{
			bno=5;
			chall();
		}
		else if(strcmp(o,"6") == 0)
		{
			bno=6;
			chall();
		}
		else if(strcmp(o,"7") == 0)
		{
			bno=7;
			chall();
		}
		else if(strcmp(o,"8") == 0)
		{
			bno=8;
			chall();
		}
		else if(strcmp(o,"9") == 0)
		{
			bno=9;
			chall();
		}
		else
		{
			clrscr();
			cout<<"Please Enter a Valid Board Number.(1-9)";
			cout<<"\n\n";
			getsnl();
		}
	}

	int getbno()
	{
		return bno;
	}

	int gethead(int i)
	{
		return d[i]-1;
	}

	int gettail(int i)
	{
		return e[i]-1;
	}

	int getbase(int i)
	{
		return f[i]-1;
	}

	int gettop(int i)
	{
		return g[i]-1;
	}
};


void mainmenu();
void credits();
void initialize();
void newgame();
void createboard();
void chz();
void snldo();
void convert();
void diplay();
void dice(int x);
void roll();
void cmove();
void achance();
void bchance();
void chancedec();
void playgame();
void zyx();


void mainmenu()
{
	clrscr();
	cout<<"\n\n\t\t\t   SNAKES AND LADDERS\n\n";
	cout<<"\n\t\t\t         MENU\n\n";
	cout<<"\t\t\t   1. NEW GAME\n";
	cout<<"\t\t\t   2. INITIALIZE\n";
	cout<<"\t\t\t   3. CREDITS\n\n";
	cout<<"\t\t\t   Press 9 to EXIT.\n\n\t\t\t   ";
	cin>>a;
	switch(a)
	{
		case 49:
		newgame();
		break;

		case 50:
		initialize();
		mainmenu();
		break;

		case 51:
		credits();
		mainmenu();
		break;

		case 57:
		exit(0);
		break;

		default:
		mainmenu();
		break;
	}
}


void credits()
{
	clrscr();
	cout<<"\n\n\n\n\n\n\t\t\t\tCredits\n\n";
	cout<<"\n\t\t    GAME DESIGNERS : DEVANSH and NITYA";
	cout<<"\n\t\t\tPERSONALIZATION BY DEVANSH\n";
	cout<<"\n\t\t    DEDICATED TO William Higinbotham";
	cout<<"\n\t\t     creater of first videogame ever";
	cout<<"\n\t\t           'TENNIS FOR TWO'\n";
	cout<<"\n\t\t    ";
	getch();
}


void initialize()
{
	clrscr();
	for(int j=0; j<10; j++)
	{
		snl s1;
		fstream out("snl.dat", ios::out | ios::app | ios::binary);
		s1.bno = j;
		s1.d[0]=20;
		s1.d[1]=24;
		s1.d[2]=34;
		s1.d[3]=38;
		s1.d[4]=45;
		s1.d[5]=54;
		s1.d[6]=62;
		s1.d[7]=87;
		s1.d[8]=92;
		s1.d[9]=98;
		s1.e[0]=3;
		s1.e[1]=14;
		s1.e[2]=13;
		s1.e[3]=17;
		s1.e[4]=28;
		s1.e[5]=35;
		s1.e[6]=43;
		s1.e[7]=25;
		s1.e[8]=50;
		s1.e[9]=77;
		s1.f[0]=9;
		s1.f[1]=16;
		s1.f[2]=26;
		s1.f[3]=32;
		s1.f[4]=40;
		s1.f[5]=57;
		s1.f[6]=61;
		s1.f[7]=66;
		s1.f[8]=68;
		s1.f[9]=78;
		s1.g[0]=30;
		s1.g[1]=36;
		s1.g[2]=48;
		s1.g[3]=53;
		s1.g[4]=59;
		s1.g[5]=65;
		s1.g[6]=79;
		s1.g[7]=73;
		s1.g[8]=90;
		s1.g[9]=86;
		out.write((char*)&s1, sizeof(s1));
	}
	cout<<"\n\n\n\n\n\n\n\n\n\t\t\t   Initialisation done.";
	cout<<"\n\n\t\t\t   ";
	getch();
}


void newgame()
{
	clrscr();
	cout<<"\n\n\t\t\t   SNAKES AND LADDERS\n\n";
	cout<<"\n\t\t\t         NEW GAME\n\n";
	cout<<"\t\t\t   1. CREATE BOARD\n";
	cout<<"\t\t\t   2. LOAD BOARD\n";
	cout<<"\t\t\t   3. USE DEFAULT BOARD\n\n";
	cout<<"\t\t\t   Press 9 to Return to MENU.\n\n\t\t\t   ";
	cin>>b;
	switch(b)
	{
		case 49:
		createboard();
		newgame();
		break;

		case 50:
		clrscr();
		chz();
		playgame();
		break;

		case 51:
		z=0;
		playgame();
		break;

		case 57:
		mainmenu();
		break;

		default:
		newgame();
		break;
	}
}


void createboard()
{
	clrscr();
	snl sc;
	ofstream out("snl.dat", ios::out | ios::binary);
	sc.getsnl();
	out.write((char*)&sc, sizeof(sc));
	getch();
}


void chz()
{
	cout<<"\nEnter Board No.\n";
	cin>>p;
	if(strcmp(p,"1") == 0)
	{
		z=1;
	}
	else if(strcmp(p,"2") == 0)
	{
		z=2;
	}
	else if(strcmp(p,"3") == 0)
	{
		z=3;
	}
	else if(strcmp(p,"4") == 0)
	{
		z=4;
	}
	else if(strcmp(p,"5") == 0)
	{
		z=5;
	}
	else if(strcmp(p,"6") == 0)
	{
		z=6;
	}
	else if(strcmp(p,"7") == 0)
	{
		z=7;
	}
	else if(strcmp(p,"8") == 0)
	{
		z=8;
	}
	else if(strcmp(p,"9") == 0)
	{
		z=9;
	}
	else
	{
		clrscr();
		cout<<"Please Enter a Valid Board Number.(1-9) \n\n";
		chz();
	}
}


void snldo()
{
	for(int da=0 ; da<10 ; da++)
	{
		for(int db=0 ; db<10 ; db++)
		{
			if(pos[ sh[db] ] == 1)
			{
			pos[ sh[db] ] = 0;
				pos[ sk[db] ] = pos[ sk[db] ] + 1;
				aa = sk[db];
			}
			else if(pos[ sh[db] ] == 2)
			{
				pos[ sh[db] ] = 0;
				pos[ sk[db] ] = pos[ sk[db] ] + 2;
				bb = sk[db];
			}
			else if(pos[ sh[db] ] == 3)
			{
				pos[ sh[db] ] = 0;
				pos[ sk[db] ] = pos[ sk[db] ] + 3;
				aa = sk[db];
				bb = sk[db];
			}
			if(pos[ lh[db] ] == 1)
			{
				pos[ lh[db] ] = 0;
				pos[ lk[db] ] = pos[ lk[db] ] + 1;
				aa = lk[db];
			}
			else if(pos[ lh[db] ] == 2)
			{
				pos[ lh[db] ] = 0;
				pos[ lk[db] ] = pos[ lk[db] ] + 2;
				bb = lk[db];
			}
			else if(pos[ lh[db] ] == 3)
			{
				pos[ lh[db] ] = 0;
				pos[ lk[db] ] = pos[ lk[db] ] + 3;
				aa = lk[db];
				bb = lk[db];
			}
		}
	}
}


void convert()
{
  for(int co=0 ; co<99 ; co++)
  {
	switch(pos[co])
	{
		case 0:
		{
			if(co%10 == 9)
			{
				dis[co][0] = (co+1)/10 + 48;
				dis[co][1] = 48;
			}
			else
			{
				dis[co][0]=(co - co%10)/10 + 48;
				dis[co][1]= co%10 + 49;
			}
		break;
		}
		case 1:
		{
		dis[co][0]=65;
		dis[co][1]=65;
		break;
		}
		case 2:
		{
		dis[co][0]=66;
		dis[co][1]=66;
		break;
		}
		case 3:
		{
		dis[co][0]=65;
		dis[co][1]=66;
		break;
		}
	}
  }
}


void display()
{
	cout<<"   ---- ---- ---- ---- ---- ---- ---- ---- ---- ";
	cout<<"----     SNAKES      LADDERS   "<<endl;
	for(int i=0; i<10; i++)
	{
		cout<<"  | ";
		if(i%2==0)
		{
			for(int j=99 - 10*i; j>89 - 10*i; j--)
			{
				cout<<dis[j]<<" | ";
			}
		}
		else
		{
			for(int k=90 - 10*i; k<100 - 10*i; k++)
			{
				cout<<dis[k]<<" | ";
			}
		}
		cout<<endl<<"   ---- ---- ---- ---- ---- ---- ---- ";
		cout<<"---- ---- ----    "<<sh[i]+1<<" to "<<sk[i]+1;
		cout<<"    "<<lh[i]+1<<" to "<<lk[i]+1<<endl;
	}
}


void dice(int x)
{
	char m=4;
	switch(x)
	{
	case 1:
		{
		cout<<"\t"<<"     "<<endl<<"\t"<<"  "<<m<<"  "<<endl;
		cout<<"\t"<<"     "<<endl;
		break;
		}
	case 2:
		{
		cout<<"\t"<<m<<"    "<<endl<<"\t"<<"     "<<endl<<"\t";
		cout<<"    "<<m<<endl;
		break;
		}
	case 3:
		{
		cout<<"\t"<<m<<"    "<<endl<<"\t"<<"  "<<m<<"  "<<endl;
		cout<<"\t"<<"    "<<m<<endl;
		break;
		}
	case 4:
		{
		cout<<"\t"<<m<<"   "<<m<<endl<<"\t"<<"     "<<endl<<"\t";
		cout<<m<<"   "<<m<<endl;
		break;
		}
	case 5:
		{
		cout<<"\t"<<m<<"   "<<m<<endl<<"\t"<<"  "<<m<<"  "<<endl;
		cout<<"\t"<<m<<"   "<<m<<endl;
		break;
		}
	case 6:
		{
		cout<<"\t"<<m<<"  "<<m<<endl<<"\t"<<m<<"  "<<m<<endl<<"\t";
		cout<<m<<"  "<<m<<endl;
		break;
		}

	}
}


void roll()
{
	time_t t;
	unsigned int seedval;
	seedval = (unsigned)time(&t);
	srand(seedval);
	up = 1 + rand()%6;
}


void cmove()
{
	gotoxy(23,22);
	cout<<"A : "<<aa+1;
	gotoxy(23,23);
	cout<<"B : "<<bb+1;
	if(cdec == 1)
	{
		gotoxy(29,22);
		cout<<"*";
	}
	else if(cdec == 2)
	{
		gotoxy(29,23);
		cout<<"*";
	}
	gotoxy(23,24);
	cout<<"Press 9 to go to MENU.";
	gotoxy(1,25);
}


void achance()
{
	if(end == 0)
	{
		pos[aa] = pos[aa] - 1;
		roll();
		if(up == 6)
		{
			cdec=1;
		}
		else
		{
			cdec=2;
		}
		if(aa + up <= 98)
		{
			aa= aa + up;
			pos[aa] = pos[aa] + 1;
			snldo();
			convert();
			clrscr();
			display();
			dice(up);
			cmove();
		}
		else if(aa + up > 99)
		{
			pos[aa] = pos[aa] + 1;
			snldo();
			convert();
			clrscr();
			display();
			dice(up);
			cmove();
		}
		else if(aa + up == 99)
		{
			clrscr();
			cout<<"\n A is the WINNER \n";
			pos[aa]=0;
			pos[bb]=0;
			pos[0]=3;
			aa=0;
			bb=0;
			end=1;
			getch();
			mainmenu();
		}
	}
}


void bchance()
{
	if(end == 0)
	{
		pos[bb] = pos[bb] - 2;
		roll();
		if(up == 6)
		{
			cdec=2;
		}
		else
		{
			cdec=1;
		}
		if(bb + up <= 98)
		{
			bb= bb + up;
			pos[bb] = pos[bb] + 2;
			snldo();
			convert();
			clrscr();
			display();
			dice(up);
			cmove();
		}
		else if(bb + up > 99)
		{
			pos[bb] = pos[bb] + 2;
			snldo();
			convert();
			clrscr();
			display();
			dice(up);
			cmove();
		}
		else if(bb + up == 99)
		{
			clrscr();
			cout<<"\n B is the WINNER \n";
			pos[aa]=0;
			pos[bb]=0;
			pos[0]=3;
			aa=0;
			bb=0;
			end=1;
			getch();
			mainmenu();
		}
	}
}


void chancedec()
{
	cout<<"\nA rolls the dice.\n";
	getch();
	roll();
	ca = up;
	dice(up);
	cout<<endl<<"\nB rolls the dice."<<endl;
	getch();
	roll();
	cb = up;
	dice(up);
	cout<<endl;
	getch();
	clrscr();
	if(ca > cb)
	{
	cout<<endl<<"A has First Chance \n";
	cdec=1;
	}
	else if(ca < cb)
	{
	cout<<endl<<"B has First Chance \n";
	cdec=2;
	}
	else if(ca == cb)
	{
	cout<<"Both got equal number. Lets do it Again \n";
	chancedec();
	}
}


void playgame()
{
	clrscr();
	end=0;
	snl so,sn;
	ifstream fin("snl.dat", ios::in | ios::binary);
	while(!fin.eof())
	{
		fin.read((char*)&sn, sizeof(sn));
		if(sn.getbno() == z)
		{
			so = sn;
		}
	}
	for(int i=0; i<10; i++)
	{
		sh[i] = so.gethead(i);
		sk[i] = so.gettail(i);
		lh[i] = so.getbase(i);
		lk[i] = so.gettop(i);
	}
	chancedec();
	getch();
	clrscr();
	convert();
	display();
	while(end == 0)
	{
		gotoxy(1,25);
		zyx();
		if(cdec == 1)
		{
			achance();
			if(end == 0)
			{
				zyx();
				if(cdec == 1)
				{
					achance();
				}
				else if(cdec == 2)
				{
					bchance();
				}
			}
		}
		else if(cdec == 2)
		{
			bchance();
			if(end == 0)
			{
				zyx();
				if(cdec == 1)
				{
					achance();
				}
				else if(cdec == 2)
				{
					bchance();
				}
			}
		}
	}
}


void zyx()
{
	cin>>xyz;
	if(strcmp(xyz,"9") == 0)
	{
		pos[aa]=0;
		pos[bb]=0;
		pos[0]=3;
		aa=0;
		bb=0;
		mainmenu();
	}
}


void main()
{

	clrscr();

	mainmenu();

	getch();

}

