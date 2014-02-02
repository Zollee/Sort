Sort
====

选择排序&amp;冒泡排序
·written in Java;



	public static void main(String[] args)
	{
		int[] arr = new int[]{2,5,6,8,3};
		System.out.print("排序前：");
		printArr(arr);
		
		selectSort(arr);                              //选择排序
		System.out.print("排序后：");
		printArr(arr);

		bubbleSort(arr);                              //冒泡排序
		System.out.print("排序后：");
		printArr(arr);
	}
	
	public static void selectSort(int[] arr)              //选择排序
	{
		for(int x = 0; x < arr.length -1; x++)
		{
			for(int y = x+1; y < arr.length; y++)
			{
				if(arr[x] > arr[y])
				{
					int temp = arr[x];
					arr[x] = arr[y];
					arr[y] = temp;
				}
			}
		}
	}
	
	
	
	public static void bubbleSort(int[] arr)              //冒泡排序
	{
		for(int x = 0; x < arr.length -1; x++)
		{
			for (int y = 0; y < arr.length-1-x; y++)
			{
				if(arr[y] > arr[y+1])
				{
					int temp = arr[y];
					arr[y] = arr[y+1];
					arr[y+1] = temp;
				}
			}
		}
	}
	
	
	public static void printArr(int[] arr)                //输出数组
	{
		for(int i = 0; i < arr.length; i++)
		{
			System.out.print(arr[i] + "	");
		}
		System.out.println();
	}
