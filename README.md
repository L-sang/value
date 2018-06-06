# 斗地主

 实现模拟斗地主的功能 
* 组合牌
  * 创建Map集合,键是编号,值是牌
  * 创建List集合,存储编号
  * 定义出13个点数的数组{"2","A","K","Q","J","10","9","8","7","6","5","4","3"};
  * 定义4个花色数组{"♠","♥","♣","♦"};
  * 遍历数组,花色+点数的组合,存储到Map集合
```  for(String number : numbers){
			for(String color : colors){
				pooker.put(index, color+number);
				pookerNumber.add(index);
				index++;
			}
		}
```  
  * 存储大王,和小王
* 洗牌
  * 洗牌,将牌的编号打乱 
```
Collections.shuffle(pookerNumber);
```
* 发牌
  * 发牌功能,将牌编号,发给玩家集合,底牌集合
  
* 看牌
  * 看牌,将玩家手中的编号,到Map集合中查找,根据键找值
    * 定义方法实现
```public static void look(String name,ArrayList<Integer> player,HashMap<Integer,String> pooker){
		//遍历ArrayList集合,获取元素,作为键,到集合Map中找值
		System.out.print(name+" ");
		for(Integer key : player){
			String value = pooker.get(key);
			System.out.print(value+" ");
		}
		System.out.println();
	}
 ```
