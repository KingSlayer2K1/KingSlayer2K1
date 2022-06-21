- 👋 Hi, I’m @KingSlayer2K1
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
KingSlayer2K1/KingSlayer2K1 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
abstract class Card
{
abstract void check(String s);
}
class MasterCard extends Card
{
public void check(String s)
{
int n=s.length();
if(n==16)
{
if(s.charAt(0)=='5' && s.charAt(1)=='1' || s.charAt(1)=='2' || s.charAt(1)=='3' ||
s.charAt(1)=='4' || s.charAt(1)=='5')
{
System.out.println("This MasterCard is Valid with card number : " + s);
}
}
else
{
System.out.println("This MasterCard is not valid with card number : " + s);
}
}
}
class Visa extends Card
{
public void check(String s)
{
int n=s.length();
if(n==13 || n==16)
{
if(s.charAt(0)=='4')
{
System.out.println("This Visa card is Valid with card number : " + s);
}
}
else
{
System.out.println("This Visa card is not Valid with card number : " + s);
}
}
}
class AmericanExpress extends Card
{
public void check(String s)
{
int n=s.length();
if(n==15)
{
if(s.charAt(0)=='3' && s.charAt(1)=='4' || s.charAt(1)=='7')
{
System.out.println("This American Express is Valid with card number : " + s);
}
}
else
{
System.out.println("This American Express is not Valid with card number : " + s);
}
}
}
public class Program16
{
public static void main(String []args)
{
System.out.println("\t****************************************");
System.out.println("Demonstrating of card problem using runtime polymorphism.");
System.out.println("\t****************************************\n");
Card obj;
obj = new MasterCard();
obj.check("5500000000000004");
obj=new Visa();
obj.check("4111111111111111");
obj=new AmericanExpress();
obj.check("5256667177788");
}
}
