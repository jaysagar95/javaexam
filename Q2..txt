import java.util.*;
class Item{
	int itemId;
	String itemName;
	Item(int itemId,String itemName){
		this.itemName=itemName;
		this.itemId=itemId;
	}
	Item(){
		void setitemId(int itemId){
			this.itemId=itemId;
		}
	}
	void setitemName(String itemName){
		this.itemName=itemName;
	}
	public String toString(){
		return this.itemId+""+this.itemName;
	}
}

class namesort implements Comparator<Item>{
	public int compare(Item i1,Item I2){
		return I1.itemId-(I2.itemId);
	}
}

class Inventory{
	static Item I = new Item();
	static ArrayList<Item>list=new ArrayList<>();
	public static void main(String[] args){
		Scanner sc = new Scanner(System.in);
		int choice;
		Item I1=new Item(1,"A");
		Item I1=new Item(3,"R");
		Item I1=new Item(2,"Z");
		Item I1=new Item(4,"H");
		Item I1=new Item(10,"M");
		list.add(I1);
		list.add(I2);
		list.add(I3);
		list.add(I4);
		list.add(I5);
		do{
			System.out.println("Enter your Choice==");
		System.out.println("1)Add Item.\n2)Display complete inventory in sorted order of item names as well as itemId.\3)Remove Item.\n4)Exit");
			choicesc.nextInt();
			switch(choice){
				case 1:
				System.out.println("enter your details as follows");
				System.out.println("enter item you want to add");
				//int n=sc.nextInt();
				for(int i =1,i<=1,i++){
					System.out.println("enter id of item");
					int d = sc.nextInt();
					l.setitemId(d);
					System.out.println("enter name of item");
					sc.nextLine();
					String ss = sc.nextLine();
					l.setitemName(ss);
					list.add(l);
				}
				System.out.println("add items as follows");
				System.out.println(list);
				break;
				case 2:
				System.out.println("before sorting");
				System.out.println(list);
				System.out.println("sorting by id");
				issort n2 = new idsort();
				Collections.sort(list,n2);
				System.out.println(list);
				System.out.println("sorting by name");
				namesort n1=new namesort();
				Collections.sort(list,n1);
				System.out.println(list);
				break;
			    case 3:	
				System.out.println("Lists as follows");
				System.out.println(list);
				System.out.println("enter index of item which you want to remove index start from 0");
				int re = sc.nextInt();
				list.remove(re);
				System.out.println("list after removal");
				System.out.println(list);
				break;
				case 4:
				System.out.println("Thank you");
				break;
				
			}
			
		}while(choice!=4);
	}
}
