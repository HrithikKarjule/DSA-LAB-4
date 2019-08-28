# DSA-LAB-4
## DATABASE WITH STRUCTURE
    #include <stdio.h>
    #include <string.h>
    struct product
    { 
        float dis;
      long long int price,id;
      char name[20];

    };
    struct product getdata()
    { 
      struct product f;
      printf("Enter Product Name:");
      scanf("%s",&f.name);
      printf("Enter Product Id:");
      scanf("%llu",&f.id);
      printf("Enter Product Price:");
      scanf("%llu",&f.price);
      printf("Enter Product discount %:");
      scanf("%f",&f.dis);


        return f;
    }

    int putdata(struct product c)
    {
      printf("\nProduct Name: %s",c.name);
      printf("\nProduct Id: %llu",c.id);
      printf("\nProduct Price: %llu",c.price);
      printf("\nProduct Discount : %.3f %",c.dis);
    }

    int main() 
    {
      struct product x[10];
      int i,n;
      printf("Enter the number of products");
      scanf("%d",&n);
      for(i=0;i<n;i++)
      {
      x[i] = getdata();
      }
      for(i=0;i<n;i++)
      {
        putdata(x[i]);
      }
      return 0;
    }

