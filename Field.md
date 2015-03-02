import java.util.Scanner;
public class Field {

	public static void main(String[] args) {
		Scanner input=new Scanner(System.in);
	    char a[][]=new char[15][50];
	    for(int i=0;i<15;i++)
	    {
	        for(int j=0;j<50;j++)
	        {
	            a[i][j]='.';
	            a[0][0]='C';
	            a[14][0]='Q';
	            a[0][49]='E';
	            a[14][49]='T';
	            for(int k=1;k<49;k++)
	            {
	            	a[0][k]='W';
	            }
	            for(int k1=1;k1<14;k1++)
	            {
	            	a[k1][0]='B';
	            }
	            for(int k2=1;k2<49;k2++)
	            {
	            	a[14][k2]='G';
	            }
	            for(int k3=1;k3<14;k3++)
	            {
	            	a[k3][49]='L';
	            }
	            
	            
	        }
	    }
	    int xx;
	    int xy;
	    double ex;
	    double ey;
	    ex=Math.random()*14;
	    ey=Math.random()*49;
	    double ex1;
	    double ey1;
	    ex1=Math.random()*14;
	    ey1=Math.random()*49;
	    double ex2;
	    double ey2;
	    ex2=Math.random()*13;
	    ey2=Math.random()*48;
	    xx=13;
	    xy=25;
	    a[xx][xy]='X';
	    a[(int) ex][(int) ey]='E';
	    a[(int) ex1][(int) ey1]='E';
	    a[(int) ex2][(int) ey2]='E';
	    int g=1;
	    for(int i=0;i<15;i++)
	    {
	        for(int j=0;j<50;j++)
	        {
	            System.out.print(a[i][j]);
	        }
	        System.out.println();
	    }
	    do
	    {
	        boolean XIsOnTheField=false;
	        if(xx>-1 && xx<15 && xy>-1 && xy<50)
	        {
	            XIsOnTheField=true;
	        }
	        do
	        {
	            System.out.print("Enter the direction(W,A,S,D): ");
	            String dir;
	            dir=input.nextLine();
	            a[xx][xy]='.';
	            switch(dir)
	            {
	            case "W":  xx=xx-1; xy=xy+0; break;
	            case "A":  xx=xx+0; xy=xy-1; break;
	            case "S":  xx=xx+1; xy=xy+0; break;
	            case "D":  xx=xx+0; xy=xy+1; break;
	            default: System.out.println("Wrong Direction");
	            }
	            a[xx][xy]='X';
	            double rand=Math.random()*4;
	            a[(int) ex][(int) ey]='.';
	            switch((int)rand)
	            {
	            case 1: ex=ex+1; ey=ey+0; break;
	            case 2: ex=ex-1; ey=ey+0; break;
	            case 3: ex=ex+0; ey=ey+1; break;
	            case 4: ex=ex+0; ey=ey-1; break;
	            }
	            a[(int) ex][(int) ey]='E';
	            if(ex=='W' || ey=='W')
	            {
	            	
	            }
	            double rand1=Math.random()*4;
	            a[(int) ex1][(int) ey1]='.';
	            switch((int)rand1)
	            {
	            case 1: ex1=ex1+1; ey1=ey1+0; break;
	            case 2: ex1=ex1-1; ey1=ey1+0; break;
	            case 3: ex1=ex1+0; ey1=ey1+1; break;
	            case 4: ex1=ex1+0; ey1=ey1-1; break;
	            }
	            a[(int) ex1][(int) ey1]='E';
	      
	            double rand2=Math.random()*4;
	            a[(int) ex2][(int) ey2]='.';
	            switch((int)rand2)
	            {
	            case 1: ex2=ex2+1; ey2=ey2+0; break;
	            case 2: ex2=ex2-1; ey2=ey2+0; break;
	            case 3: ex2=ex2+0; ey2=ey2+1; break;
	            case 4: ex2=ex2+0; ey2=ey2-1; break;
	            }
	            a[(int) ex2][(int) ey2]='E';
	            for(int i=0;i<15;i++)
	            {
	                for(int j=0;j<50;j++)
	                {
	                    System.out.print(a[i][j]);
	                }
	                System.out.println();
	            }


	        }
	        while(XIsOnTheField=true);

	    }
	    while(g!=2);


	    for(int i=0;i<15;i++)
	    {
	        for(int j=0;j<50;j++)
	        {
	            System.out.print(a[i][j]);
	        }
	        System.out.println();
	    }


	}
	

	}



