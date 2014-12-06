
public class Resistor {
private double nominalValue;
private double tolerance;
private double actualResistance;

/**
 * 
 * @param nominalResistance
 * @param tolerance
 * @return actual resistance
 */
public double actualResistance(double nominalResistance, double tolerance){
	double error;
	double lower;
	double upper;
	tolerance = tolerance* 0.01;
	error = nominalResistance*tolerance;
	lower = nominalResistance - error;
	upper = nominalResistance + error;
	actualResistance = (int)(upper*Math.random() + lower);
	return actualResistance;
}//end constructor


}
