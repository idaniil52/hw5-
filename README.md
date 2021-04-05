# hw5-
public abstract class PayCalculator{
    private double payRate;
    public PayCalculator(double payRate){
        this.payRate=payRate;
    }
    public double getPay(double hours){
        return payRatehours;
    }
}


public class RegularPay extends PayCalculator{
    public RegularPay(double payRate){
        super(payRate);
    }
    public static void main(String[] args){
        RegularPay rpay= new RegularPay(10.00);
    }
}




public class HazardPay extends PayCalculator{
    public HazardPay(double payRate){
        super(payRate);
    }
    public double getPay(double hours){
       return super.getPay(hours)1.5; 
    }
}



public abstract class DiscountPolicy{
    private double percentOff;
    public double computeDiscount(int count, double itemCost){
        return countitemCostpercentOff/100;
    }
}


public class BulkDiscount extends DiscountPolicy{
    int minimum;
    double percent;
    @Override
    public double computeDiscount(int count, double itemCost){
      double discount;
      if(count>minimum){
          discount=countitemCostpercent/100;
        }
        else{
           discount=0.00; 
        }
      return discount;
    }
}




public interface MessageEncoder{
    public String encode(String password);
}


public class SubsitutionCipher implements MessageEncoder{
    int shift;

    public Character ShiftCharacter(Character x){
        return (char)(x+shift);
    }
    @Override
    public String encode(String password){
        String encoddedPassword;
        for(int i=0;i<password.length();i++){
            Character c= password.charAt(i);
            ShiftCharacter(c);
        }
        return null;
    }
}
