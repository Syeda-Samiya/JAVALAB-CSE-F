## EXPERIMENT 3
## EXPERIMET 3A
# TITLE: 3A)Implement Constructor Overloading in JAVA
```
class Student {

	String name;
	int age;
	double marks;

	Student() {

	}

	Student(String name, int age, double marks) {

		this.name=name;
		this.age=age;
		this.marks=marks;

	}

	void display() {

		System.out.println("Name: "+name);
		System.out.println("Age: "+age);
		System.out.println("marks: "+marks);

	}

}
```
# Main.java
```
class Main {

	public static void main(String args[]) {

		Student std = new Student();
		std.display();

		Student std1 = new Student("Hari", 40, 67.8);
		std1.display();

	}
}
```

# Output
<img width="1920" height="1020" alt="exp3A" src="https://github.com/user-attachments/assets/6a5b9740-6c52-4fee-a498-3d8e092f6abe" />



## EXPERIMENT 3B
# TITLE:Implementing Binary search Algorithm
```
import java.util.Scanner;
class BinarySearch {

	int list[];
	int key;
	int size;

	BinarySearch(int size) {

		list= new int[size];
		key = -1;
		this.size=size;

 	}
 
 	void setList() {

			Scanner sc = new Scanner(System.in);
			System.out.println("Enter the list items in Ascending Order.");


			for( int i = 0; i < size; i++) {
	
				System.out.print("Enter the value of " + (i + 1) + " item: ");
				list[i] = sc.nextInt();
			}
			sc.close();

	}

	void getList() {

		for(int i = 0; i < size; i++) 
		System.out.print(list[i] + ", "); System.out.println("\b\b.");

	}

	int binarySearch(int key) {

		int low = 0; int high = list.length; int mid = 0;

		while(low < high) {

			mid = (low + high) / 2;

			if(list[mid] == key) {
				break;
			}

			else if(list[mid] < key) {

				low = mid + 1;
			}

			else
				high = mid + 1;

		}

		return list[mid]==key ? mid : -1 ;

	}

}
```
# Main.java
```
import java.util.Scanner;
class Main {

	public static void main(String args[]) {

		
		BinarySearch bs = new BinarySearch(10);
		bs.setList();
		bs.getList();


	int index = bs.binarySearch(10);		
	if(index == -1 )
			System.out.println("Key item does not exit");

		else
			System.out.println("key item exist at index: " + index);

	}

}
```

# Output
<img width="1920" height="1020" alt="exp3b" src="https://github.com/user-attachments/assets/1ab44d27-ac7e-4279-8e91-b89eee3010bf" />


## EXPERIMENT 3C
# TITLE: 3C)Sorting Element using Bubble Sort
```
class BubbleSort {

	void bubbleSort(int arr[]) {

		int n = arr.length;
		int temp = 0;

		for(int i=0 ; i < n-1 ; i++) {

			for(int j=0; j<n-i-1; j++) {

				if(arr[j] > arr[j+1]) {

					temp = arr[j+1];
					arr[j+1] = arr[j];
					arr[j] = temp;

				}
			}
		}

	}

}
```
# Main.java
```
import java.util.Scanner;
 class Main {
	
	public static void main(String args[]) {


		System.out.print("Enter the size of array: ");
		Scanner sc = new Scanner(System.in);
		int size = sc.nextInt();

		int integer[] = new int[size];

		for(int i = 0; i < size; i++) {

			System.out.print("Enter the value of integer at index " + (i+1) + ":"); 
			integer[i] = sc.nextInt();
		}

		BubbleSort bs = new BubbleSort();
		bs.bubbleSort(integer);


		System.out.print("The Sorted integer: ");

		for(int i = 0; i < size; i++)
		System.out.print(integer[i] + ", ");

		System.out.println("\b\b.");

	}

}
```

# Output
<img width="1920" height="1020" alt="exp3c" src="https://github.com/user-attachments/assets/8a74c74a-9fa4-418c-a88e-6331d1b16df7" />

