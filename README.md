#include<stdio.h>

void push ();
void pop ();
void display ();
int top = -1;
int stack[100], x, n, i, n, choice;
int
main ()
{


  printf ("enter the size of stack\t");
  scanf ("%d", &n);
  printf ("stack implementation using array\n");
  printf ("\n 1.PUSH \n 2.POP \n 3.DISPLAY\nv 4.Exit  \n");

  do
    {
      printf ("Enter your choice :\t");
      scanf ("%d", &choice);

      switch (choice)
	{

	case 1:
	  {
	    push ();
	    break;
	  }
	case 2:
	  {
	    pop ();
	    break;
	  }
	case 3:
	  {
	    display ();
	    break;
	  }

	case 4:
	  {
	    printf ("Exit");
	    break;
	  }
	default:
	  {
	    printf ("Enter the valid choice (Between 1/2/3/40");
	  }

	}


    }
  while (choice != 4);
  return 0;
}

void
push ()
{
  if (top >= n - 1)
    {
      printf ("Stack over Flow.");
    }
  else
    {
      printf ("Enert the number\t");
      scanf ("%d", &x);
      top++;
      stack[top] = x;
    }

}

void
pop ()
{
  if (top <= -1)
    {
      printf ("StaCK Underflow");
    }
  else
    {
      printf ("Element deleted from stack\n");
      top--;
    }


}

void
display ()
{

  if (top >= 0)
    {
      printf ("Elements are\n");
      for (i = top; i >= 0; i--)
	{
	  printf ("\n %d", stack[i]);
	}
    }
  else
    {
      printf ("Stack is empty");
    }

}
