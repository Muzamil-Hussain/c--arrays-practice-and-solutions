# c--arrays-practice-and-solutions
###### This is for students new with programming. It can be made better by dividing the code in to different functions and making it simpler.


##  C++ code that initializes an array with 4 rows and 5 columns. The program asks user about two row numbers in the range 0 to 4.  After that the program must be able to swap the rows defined by the user in a 2D array.

```
#include <iostream>
#include <iomanip>
using namespace std;
int main()
{
	int arr[4][5]={{1,2,3,4,5},{6,7,8,9,10},{11,12,13,14,15},{16,17,18,19,20}};
	int temp[5];
	int row1,row2;
	cout<<"Enter the rows to be exchanged: ";
	cin>>row1>>row2;
	for (int i=0;i<5;i++)
	{
		temp[i]=arr[row1][i];
	}
	for (int i=0;i<5;i++)
	{
		arr[row1][i]=arr[row2][i];
	}
	for (int i=0;i<5;i++)
	{
		arr[row2][i]=temp[i];
	}
	for (int i=0;i<4;i++)
	{
		for (int j=0;j<5;j++)
		{
			cout<<setw(2)<<arr[i][j]<<" ";
		}
		cout<<"\n";
	}
}

```


##  C++ code that initializes an array with 4 rows and 5 columns. The program asks user about two columns numbers in the range 0 to 5.  After that the program must be able to swap the columns defined by the user in a 2D array. 

```
#include <iostream>
#include <iomanip>
using namespace std;
int main()
{
	int arr[4][5]={{1,2,3,4,5},{6,7,8,9,10},{11,12,13,14,15},{16,17,18,19,20}};
	int temp[4];
	int col1,col2;
	cout<<"Enter the columns to be exchanged: ";
	cin>>col1>>col2;
	for (int i=0;i<4;i++)
	{
		temp[i]=arr[i][col1];
	}
	for (int i=0;i<4;i++)
	{
		arr[i][col1]=arr[i][col2];
	}
	for (int i=0;i<4;i++)
	{
		arr[i][col2]=temp[i];
	}
	for (int i=0;i<4;i++)
	{
		for (int j=0;j<5;j++)
		{
			cout<<setw(2)<<arr[i][j]<<" ";
		}
		cout<<"\n";
	}
}

```


![Image description](https://i.imgur.com/s1cPuE3.png)
 
 
 ```
 #include <iostream>
using namespace std;
int main()
{
	int num,sum=0,sum2,sum3;
	int arr[5][4];
	int arr2[5][5],arr3[5][5];
	cout<<" Enter 1 to input elements into matrix\n Enter 2 to display elements of matrix\n Enter 3 to sum all the elements of matrix\n Enter 4 to display row-wise sum of matrix\n Enter 5 to display column-wise sum of matrix\n Enter 6 to transpose the matrix\n";
	cin>>num;
	switch (num)
	{
		case 1:
			for (int i=0;i<5;i++)
			{
				cout<<"Enter the elements for row "<<i<<":";
				for (int j=0;j<4;j++)
				{
					cin>>arr[i][j];
				}
			}
			break;
		case 2:
			for (int i=0;i<5;i++)
			{
				cout<<"Enter the elements for row "<<i<<":";
				for (int j=0;j<4;j++)
				{
					cin>>arr[i][j];
				}
			}
			for (int i=0;i<5;i++)
			{
				for (int j=0;j<4;j++)
				{
					cout<<arr[i][j]<<" ";
				}
			cout<<"\n";
			}			
			break;
		case 3:
			for (int i=0;i<5;i++)
			{
				cout<<"Enter the elements for row "<<i<<":";
				for (int j=0;j<4;j++)
				{
					cin>>arr[i][j];
				}
			}
			for (int i=0;i<5;i++)
			{
				for (int j=0;j<4;j++)
				{
					cout<<arr[i][j]<<" ";
				}
				cout<<"\n";
			}			
			cout<<"\n";
			for (int i=0;i<5;i++)
			{
				for (int j=0;j<4;j++)
				{
					sum+=arr[i][j];
				}
			}
			cout<<"The sum of all elements of given matrix is "<<sum<<endl;
			break;
		case 4:
			for (int i=0;i<5;i++)
			{
				cout<<"Enter the elements for row "<<i<<":";
				for (int j=0;j<4;j++)
				{
					cin>>arr[i][j];
				}
			}
			for (int i=0;i<5;i++)
			{
				for (int j=0;j<4;j++)
				{
					cout<<arr[i][j]<<" ";
				}
				cout<<"\n";
			}			
			cout<<"\n";
			for (int i=0;i<5;i++)
			{
				sum2=0;
				for (int j=0;j<4;j++)
				{
					sum2+=arr[i][j];
				}
			cout<<"The sum of all elements of row "<<i<<" is "<<sum2<<endl;
			}
			break;
		case 5:
			for (int i=0;i<5;i++)
			{
				cout<<"Enter the elements for row "<<i<<":";
				for (int j=0;j<4;j++)
				{
					cin>>arr[i][j];
				}
			}
			for (int i=0;i<5;i++)
			{
				for (int j=0;j<4;j++)
				{
					cout<<arr[i][j]<<" ";
				}
				cout<<"\n";
			}			
			cout<<"\n";
			for (int i=0;i<4;i++)
			{
				sum3=0;
				for (int j=0;j<5;j++)
				{
					sum3+=arr[j][i];
				}
			cout<<"The sum of all elements of column "<<i<<" is "<<sum3<<endl;
			}
			break;
		case 6:
			for (int i=0;i<5;i++)
			{
				cout<<"Enter the elements for row "<<i<<":";
				for (int j=0;j<5;j++)
				{
					cin>>arr2[i][j];
				}
			}
			for (int i=0;i<5;i++)
			{
				for (int j=0;j<5;j++)
				{
					cout<<arr2[i][j]<<" ";
				}
			cout<<"\n";
			}			
			for (int i=0;i<5;i++)
			{
				for (int j=0;j<5;j++)
				{
					arr3[i][j]=arr2[j][i];
				}
			}
			cout<<"\n";
			for (int i=0;i<5;i++)
			{
				for (int j=0;j<5;j++)
				{
					cout<<arr3[i][j]<<" ";
				}
			cout<<"\n";
		    }
		    break;
		default:
			cout<<"Invalid option.";
			break;
	}
	return 0;
	
}

 ```
 
 ![Image description](https://i.imgur.com/2L8Ajtp.png)
 
 ```
 #include <iostream>
using namespace std;
int main()
{
	int arr[5][5]={{2,3,1,5,0},{7,1,5,3,1},{2,5,7,8,1},{0,1,5,0,1},{3,4,9,1,5}},k=0;
	for (int i=0;i<5;i++)
	{
		for (int l=1;l<=k;l++)
			{
				cout<<" ";
			}
		for (int j=k;j<5;j++)
		{

			cout<<arr[i][j];
		}
		k+=1;
		cout<<"\n";
	}
	return 0;
}

 ```
 
 ##  The Lo Shu Magic Square is a grid with 3 rows and 3 columns. The Lo Shu Magic Square has the following properties;  The grid contains the numbers 1 through 9 exactly.  The sum of each row, each column, and each diagonal all add up to the same number. 
## In a program, you have to simulate a magic square using a two-dimensional array and determines, whether the array is a Lo Shu Magic Square? 

![Image description](https://i.imgur.com/wkddRJb.png)

```
#include <iostream>
using namespace std;
int main()
{
	int sum1=0,sum2=0,sum3=0,sum4=0,sum5=0,sum6=0,sum7=0,sum8=0;
	int square[3][3];
	for (int i=0;i<3;i++)
	{
		cout <<"Enter row "<<i<<endl;
		for (int j=0;j<3;j++)
		{
			cin>>square[i][j];
		}
	}
	cout<<"\nThe square becomes.\n";
	for (int i=0;i<3;i++)
	{
		for (int j=0;j<3;j++)
		{
			cout<<square[i][j]<<"\t";
		}
		cout<<"\n";
	}
	for (int i=0;i<3;i++)
	{
		for (int j=0;j<3;j++)
		{
			if (i==0)
			{
				sum1+=square[i][j];
			}
			if (i==1)
			{
				sum2+=square[i][j];
			}
			if (i==2)
			{
				sum3+=square[i][j];
			}
		}
	}
	for (int i=0;i<3;i++)
	{
		for (int j=0;j<3;j++)
		{
			if (i==0)
			{
				sum4+=square[j][i];
			}
			if (i==1)
			{
				sum5+=square[j][i];
			}
			if (i==2)
			{
				sum6+=square[j][i];
			}
		}
	}
	for (int i=0;i<3;i++)
	{
		for (int j=0;j<3;j++)
		{
			if (i==j)
			{
				sum7+=square[i][j];
			}
		}
	}
	for (int i=0;i<3;i++)
	{
		for (int j=2;j>=0;j--)
		{
			if (i==j)
			{
				sum8+=square[i][j];
			}
		}
	}
	
	if (sum1==sum2 && sum2==sum3 && sum3==sum4 && sum4==sum5 && sum5==sum6 && sum6==sum7 && sum7==sum8)
	{
		cout<<"\nGiven square is Lo Shu Magic Square.";
	}
	else
	{
	     cout<<"\nGiven square is not Lo Shu Magic Square.";
	}
	
	return 0;
}

```

 ##  Write a program to take sum of adjacent indexes of an integer array with 100 cells and copy the result into another integer array. 
 
 ![Image description](https://i.imgur.com/TnBUoUj.png)
 
 ```
 #include <iostream>
using namespace std;
int main()
{
	int list1[100]={1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10};
	int list2[50];
	int sum=0;
	for (int i=0;i<50;i+=1)
	{
		sum=0;
		sum+=(list1[2*i]+list1[(2*i)+1]);
		list2[i]=sum;
	}
	for (int i=0;i<50;i++)
	{
		cout<<list2[i]<<" ";
	}
	return 0;
}
 ```
 
 ## C++ program that initializes an array of size 4 X 4 and check whether matrix is an Identity matrix or not. Identity matrix is a special square matrix whose main diagonal elements is equal to 1 and other elements are 0.  
 
 ```
 #include<iostream>
using namespace std;
int main()
{
    int imatrix[4][4]={{1,0,0,0},{0,1,0,0},{0,0,1,0},{0,0,0,1}};
    int x=0;
    for (int i=0;i<4;i++)
	{
    	for (int j=0;j<4;j++)
		{
    		if (i==j)
			{
    			if (imatrix[i][j]!=1)
				{
    				x++;
				}
			}
			else 
			{
				if (imatrix[i][j]!=0)
				{
					x++;
				}
			}
		}
	}
	if (x>0)
	{
		cout<<"matrix is not identity matrix."<<endl;
	}else 
	{
		cout<<"matrix is identity matrix."<<endl;
	}
	return 0;
}
 ```
 
 ## program that determines if the number of positive and negative values in an integer array is the same. The program should print true if the list contains -5, 1, -3, 2 (two positives and two negatives), but it should print false for the list containing -5, -1, 3, 2, 11 (too many positive).  The code should print true if the list is empty, since an empty list contains the same number of positive and negatives (0 for both). The program must not affect the contents of the list and 0 must not be included in array values. 
 
 ```
 #include <iostream>
using namespace std;
int main()
{
	int list[6]={1,2,-3,-4,5,-6};
	int count1=0,count2=0,count3=0,k=0;
	for (int i=0;i<6;i++)
	{
		if (list[i]==0)
		{
			k+=1;
			count3+=1;
		}
	}
	if (k>0 && k<6 )
	{
		cout<<"list can't contain the element 0, please enter valid list.";
	}
	else 
	{
		for (int i=0;i<6;i++)
		{
			if (list[i]<0)
			{
				count1+=1;
			}
			else if (list[i]>0)
			{
				count2+=1;
			}
		
		}
	if (count1==count2 || count3==6)
	{
	    cout<<"True";
	}
	else
	{
		cout<<"False";
	}
	}

	return 0;
}

 ```
 
 
 ## Write a code that sum top-bottom pair of an integer array of size 100 and place it into another array. 
 
 ![Image description](https://i.imgur.com/TXhO4PU.png)
 
 ```
 #include <iostream>
using namespace std;
int main()
{
	int list1[100]={1,2,3,4,7,8,9,10,5,6,1,2,3,4,7,8,9,10,7,8,1,2,3,4,7,8,9,10,5,6,1,2,3,4,7,8,9,10,7,8,1,2,3,4,7,8,9,10,7,8,1,2,3,4,7,8,9,10,5,6,1,2,3,4,7,8,9,10,7,8,1,2,3,4,7,8,9,10,5,6,1,2,3,4,7,8,9,10,7,8,1,2,3,4,7,8,9,10,7,8};
	int list2[50];
	int sum=0;
	for (int i=0,j=99;i<50,j>=50;i++,j--)
	{
		sum=0;
		sum+=(list1[i]+list1[j]);
		list2[i]=sum;
	}
	for (int i=0;i<50;i++)
	{
		cout<<list2[i]<<" ";
	}
	return 0;
}

 ```
 
 
 ##  C++ program that determines whether a 2-dimensional arrays have the same corresponding elements. For example: 
![Image description](https://i.imgur.com/EM3f2KU.png)

```
#include <iostream>
using namespace std;
int main()
{
	int arr1[3][2]={{2,1},{3,4},{5,6}};
	int n_arr1[6];
	int arr2[3][2]={{1,2},{3,4},{5,6}};
	int n_arr2[6];
	int temp=0,temp1=0,k=0,l=0,count=0;
	for (int i=0;i<3;i++)
	{
		for (int j=0;j<2;j++)
		{
			n_arr1[k++]=arr1[i][j];
			n_arr2[l++]=arr2[i][j];
		}
	}
	for (int i=0;i<6;i++)
	{
		
		for (int j=0;j<6;j++)
		{
			temp=0;
			if (n_arr1[i]<n_arr1[j])
			{
				temp=n_arr1[i];
				n_arr1[i]=n_arr1[j];
				n_arr1[j]=temp;
			}
		}
	}
		for (int i=0;i<6;i++)
	{
		
		for (int j=0;j<6;j++)
		{
			temp1=0;
			if (n_arr2[i]<n_arr2[j])
			{
				temp1=n_arr2[i];
				n_arr2[i]=n_arr2[j];
				n_arr2[j]=temp1;
			}
		}
	}
	for (int i=0;i<6;i++)
	{
		if(n_arr1[i]!=n_arr2[i])
		{
			count+=1;
		}
	}
	if (count>0)
	{
		cout<<"The elements of given elements are not equal";
	}
	else
	{
		cout<<"The elements of given array are equal";
	}
	return 0;
}

```


##  C++ program that changes a 2-Dimensional array into a 1-dimensional array with all the elements of the two-dimensional array. For example: int arr[3][2]={{3,4},{1,6},{7,8}} should be converted into: int n_arr[6]={3,4,1,6,7,8} 
 
 
```
#include <iostream>
using namespace std;
int main()
{
	int arr[3][2]={{3,4},{1,6},{7,8}};
	int n_arr[6];
	cout<<"{";
	for (int i=0;i<3;i++)
	{
		for (int j=0;j<2;j++)
		{
			n_arr[i]=arr[i][j];
			cout<<n_arr[i];
			if (not(i==2 && j==1))
			{
				cout<<",";
			}
		}
	}
	cout<<"}";
	return 0;
}

```

##  Given a two dimensional array, write a C++ program that prints the array in column major order. For example: int arr[3][2]={{3,4},{1,6},{7,8}} should be printed as: 3, 1, 7,4, 6, 8 
 
 
```
#include <iostream>
using namespace std;
int main()
{
	int arr[3][2]={{3,4},{1,6},{7,8}};
	int n_arr[6];
	cout<<"{";
	for (int i=0;i<2;i++)
	{
		for (int j=0;j<3;j++)
		{
			n_arr[i]=arr[j][i];
			cout<<n_arr[i];
			if (not(i==2 && j==1))
			{
				cout<<",";
			}
		}
	}
	cout<<"}";
	return 0;
}

```
