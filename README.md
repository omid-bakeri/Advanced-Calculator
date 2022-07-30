# Advanced-Calculator
This Desktop app is a Advanced Calculator create with c# and SharpDevelop


/*
 * Created by SharpDevelop.
 * Programmer = Omid Bakeri
 * Project = Advanced Calculator
 * User: LaptopYar
 * Date: 15/04/1400
 * Time: 11:52
 * 
 * To change this template use Tools | Options | Coding | Edit Standard Headers.
 */
 
 
using System;
using System.Collections.Generic;
using System.Drawing;
using System.Windows.Forms;
using System.Globalization;

namespace Advanced_Calculator
{
	public partial class MainForm : Form
	{
		double H=0;
		double Division=0;
		double Minus=0;
		double Sum=0;
		double Multiple=0;
		double Equals=0;
		double XY=0;
		double Mod=0;
		
		char corporation;
		
		
		// Div //
		double divMath1;
		double divMath2;
		double divRes;
		string Svdiv1;
		string Svdiv2;
		double eqDiv1;
		double eqDiv2;
		double fiDiv;
		// Div //
		
		
		
		public MainForm()
		{
			
			InitializeComponent();
		}
		
		bool f1=false , f2=false , f3=false , f4=false , f5=false , f6=false , f7=false , f8=false , f9=false , f0=false;
		
		void Button24_Click(object sender, EventArgs e)
		{
			txt_calc.Text = txt_calc.Text + btn_one.Text;
			f1=true;
		}
		
		void Btn_two_Click(object sender, EventArgs e)
		{
			txt_calc.Text = txt_calc.Text + btn_two.Text;
			f2=true;
		}
		
		void Btn_three_Click(object sender, EventArgs e)
		{
			txt_calc.Text = txt_calc.Text + btn_three.Text;
			f3=true;
		}
		
		void Btn_four_Click(object sender, EventArgs e)
		{
			txt_calc.Text = txt_calc.Text +  btn_four.Text;
			f4=true;
		}
		
		void Btn_five_Click(object sender, EventArgs e)
		{
			txt_calc.Text = txt_calc.Text +  btn_five.Text;
			f5=true;
		}
		
		void Btn_six_Click(object sender, EventArgs e)
		{
			txt_calc.Text = txt_calc.Text +  btn_six.Text;
			f6=true;
		}
		
		void Btn_seven_Click(object sender, EventArgs e)
		{
			txt_calc.Text = txt_calc.Text + btn_seven.Text;
			f7=true;
		}
		
		void Btn_eight_Click(object sender, EventArgs e)
		{
			txt_calc.Text = txt_calc.Text +  btn_eight.Text;
			f8=true;
		}
		
		void Btn_nine_Click(object sender, EventArgs e)
		{
			txt_calc.Text = txt_calc.Text +  btn_nine.Text;
			f9=true;
		}
		
		void Btn_ziro_Click(object sender, EventArgs e)
		{
			txt_calc.Text = txt_calc.Text +  btn_ziro.Text;
			f0=true;
		}
		
		void Btn_c_Click(object sender, EventArgs e)
		{
			txt_calc.Clear();
			txt_calc.ForeColor = Color.DarkBlue;
		}
		
		void Btn_back_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				txt_calc.Text = txt_calc.Text.Remove(txt_calc.Text.Length -1);
			}
			
		}
		
		void Btn_xpow2_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			if(txt_calc.Text!="")
			{
				double powx2Math;
			    double powx2Compute;
			    string pxSave;
			    
				powx2Math    =  double.Parse(txt_calc.Text);
				pxSave = txt_calc.Text;
				txt_calc.Clear();
				
				powx2Compute =  Math.Pow(powx2Math , 2);
				string powOperatorXRes;
				powOperatorXRes = powx2Compute.ToString();
				    
				//corporation = "xpow2";
				txt_calc.Text = pxSave + "^" + 2 + "=" + powOperatorXRes;
				txt_calc.ForeColor = Color.DarkGreen;
				
			}
		}
		
//		void Btn_xpowy_Click(object sender, EventArgs e)
//		{	
//			if(txt_calc.Text=="")
//			{
//				MessageBox.Show("برای انجام این عملیات دو عدد را وارد نمایید" , "خطا" ,  MessageBoxButtons.OK , MessageBoxIcon.Warning);
//			}
//			
//			if(txt_calc.Text!="")
//			{
//				corporation = "xpy";
//				double powMathx;
//				double powMathy;
//				double powResxy;
//				
//				powMathx = double.Parse(txt_calc.Text);
//				txt_calc.Clear();
//				
//				
//				//powMathy = double.Parse(txt_calc.Text);
//				
//				//powResxy = Math.Pow(powMathx , double.Parse(txt_calc.Text));
//			}
//		}
		
		
		void Btn_sin_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")	
			{
				double sinMath;
				double sinRes;
				string sinSave;
				
				sinMath = double.Parse(txt_calc.Text);
				sinSave= txt_calc.Text;
				
				txt_calc.Clear();
				
				sinRes = Math.Sin(sinMath);
				txt_calc.Text = "sin" + "(" +  sinSave + ")" + "=" +  sinRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;
			}
		}
		
		
		void Btn_cos_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")	
			{
				double cosMath;
				double cosRes;
				string cosSave;
				
				cosMath = double.Parse(txt_calc.Text);
				cosSave = txt_calc.Text;
				txt_calc.Clear();
				
				cosRes = Math.Cos(cosMath);
				txt_calc.Text = "cos" + "(" + cosSave + ")" + "=" + cosRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;
			}
			
		}
		
		void Btn_tan_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")	
			{
				double tanMath;
				double tanRes;
				string tanSave;
				
				tanMath = double.Parse(txt_calc.Text);
				tanSave= txt_calc.Text;
				txt_calc.Clear();
				
				tanRes = Math.Tan(tanMath);
				txt_calc.Text = "tan" + "(" + tanSave + ")" + "=" +   tanRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;
			}
		}
		
		void Btn_rad_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				double radMath;
				double radRes;
				string radSave;
				
				radMath = double.Parse(txt_calc.Text);
				radSave = txt_calc.Text;
				txt_calc.Clear();
				
				radRes  = Math.Sqrt(radMath);
				txt_calc.Text = "√" + "(" + radSave  + ")" + "=" +  radRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;
				
			}
		}
		
		void Btn_10powx_Click(object sender, EventArgs e)
		{
			
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				double powTenMath;
				double powTenRes;
				string TenSave;
				
				
				powTenMath = double.Parse(txt_calc.Text);
				TenSave = txt_calc.Text;
				txt_calc.Clear();
				
				powTenRes = Math.Pow(10 , powTenMath);
				txt_calc.Text = 10 + "^" + TenSave + "=" + powTenRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;

			}
		}
		
		void Btn_log_Click(object sender, EventArgs e)
		{	
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				double mathLog;
				double mathRes;
				
				mathLog = double.Parse(txt_calc.Text);
				mathRes = Math.Log10(mathLog);
				
				txt_calc.Text = "log" + "(" + mathLog.ToString() + ")" + "=" + mathRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;
			}
		}
		
		void Btn_exp_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				double mathExp;
				double mathRes;
				string expSave;
				
				mathExp = double.Parse(txt_calc.Text);
				expSave = txt_calc.Text;
				txt_calc.Clear();
				
				mathRes = Math.Exp(mathExp);
				
				
				txt_calc.Clear();
				
				txt_calc.Text = mathRes.ToString();
				
				txt_calc.Text = "exp" + "(" + expSave + ")" + "=" + mathRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;
			}
		}
		
		
		void Btn_nfactorial_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				 int mathFact;
				 int mathRes=1;
				//int finalRes;
				string mathFinal;
				
				
				mathFact  =  int.Parse(txt_calc.Text);
				mathFinal = txt_calc.Text;
				
				txt_calc.Clear();
				
				 int i;
				
				for(i=mathFact ; i>=1 ; i--)
				{
					mathRes = mathRes * i ;  //5   
				}
				
				txt_calc.Text = "fact" + "(" + mathFinal + ")" + "=" + mathRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;
			}
		}
		
		void Btn_xpow3_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				
				double xThreeMath;
				double xThreeRes;
				string saveNum;
				
				xThreeMath = double.Parse(txt_calc.Text);
				saveNum = txt_calc.Text;
				txt_calc.Clear();
				
				xThreeRes = Math.Pow(xThreeMath , 3);
				
				txt_calc.Text = "cube " + "(" +  saveNum +  ")" + "=" + xThreeRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;
			}
		}
		
		void Btn_xnum_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				txt_calc.ForeColor = Color.DarkRed;
				double xMath;
				double xRes;
				double xNum;
				
				string xSave;
				
				xMath = double.Parse(txt_calc.Text);
				xSave = txt_calc.Text;
				xNum = double.Parse(xSave);
				
				
				txt_calc.Clear();
				
				xRes = (1)/(xNum) ;
				
				txt_calc.Text = 1 + "/" + "("  + xNum.ToString()  + ")" + "=" + xRes;
				txt_calc.ForeColor = Color.DarkGreen;
			}
		}
		
		void Btn_ln_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				double lnMath;
				double lnRes;
				
				lnMath = double.Parse(txt_calc.Text);
				lnRes = 2.303 * Math.Log10(lnMath);
				
				txt_calc.Clear();
				
				txt_calc.Text = "ln" + "(" + lnMath + ")"  + "=" + lnRes.ToString();
				txt_calc.ForeColor =Color.DarkGreen;
				
				
			}
			
		}
		
		void Btn_pi_Click(object sender, EventArgs e)
		{
			txt_calc.Text = "3.1415926535897932384626433832795";
			txt_calc.ForeColor=Color.DarkGreen;
		}
		
		void Btn_epowx_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				double piMath;
				double piRes;
				string piSave;
				
				double pi = 2.71828;
				double piRex;
				
				piMath = double.Parse(txt_calc.Text);
				piSave = txt_calc.Text;
				piRex = double.Parse(piSave);
				
				txt_calc.Clear();
				
				piRes = Math.Pow( pi , piRex);
				
				txt_calc.Text = "e" + "^" + "(" + piSave + ")" + "=" + piRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;
			}
		}
		
		void Btn_pm_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				double pmmathd;
				pmmathd = double.Parse(txt_calc.Text);
				
				txt_calc.Text = (-pmmathd).ToString();
			}
		}
		
		void Btn_aopen_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				txt_calc.Text = btn_aopen.Text + txt_calc.Text;
			}
		}
		
		void Btn_aclose_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				txt_calc.Text = btn_aclose.Text + txt_calc.Text;
			}
		}
		
		void Btn_slash_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				txt_calc.Text = txt_calc.Text + btn_slash.Text ; 
			}
		}
		
		void Btn_div_Click(object sender, EventArgs e)
		{
	
			if(txt_calc.Text=="")
			{
				MessageBox.Show("نامعتبر", "خطا", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				corporation ='/';
				Division += Convert.ToDouble(txt_calc.Text);
				txt_calc.Clear();
			}
		}
		
		void Btn_minus_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("نامعتبر", "خطا", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				corporation ='-';
				Minus +=Convert.ToDouble(txt_calc.Text);
				txt_calc.Clear();
			}
		}
		
		void Btn_plus_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("نامعتبر", "خطا", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				Sum += Convert.ToDouble(txt_calc.Text);
				corporation ='+';
				txt_calc.Clear();
				
			}
		}
		

		void Btn_multiple_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("نامعتبر", "خطا", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				Multiple += Convert.ToDouble(txt_calc.Text);
				corporation = '*';
				
				txt_calc.Clear();
			}
		}
		
		
		void Btn_result_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("نامعتبر", "خطا", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(corporation=='/')
			{
				H+= double.Parse(txt_calc.Text);
				double divRes;
				
				divRes = Division / H;
				
				txt_calc.Clear();
				
				txt_calc.Text = Division + "÷" + H + "=" + divRes.ToString();
                txt_calc.ForeColor = Color.DarkGreen;
                
				Division = '\0';
				H = '\0';
				
				
			}
			
			if(corporation == '-')
			{
				H+= double.Parse(txt_calc.Text);
				double minuRes;
				
				minuRes = Minus - H;
				txt_calc.Clear();
				
				txt_calc.Text = Minus + "-" + H  + "=" + minuRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;
				
				Minus = '\0';
				H = '\0';
			}
			
			if(corporation =='*')
			{
				H += Convert.ToDouble(txt_calc.Text);
				double multRes;
				
				multRes = Multiple * H ; 
				
				txt_calc.Clear();
				
				txt_calc.Text = Multiple + "*" + H + "=" + multRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;
				
				Multiple = '\0';
				H = '\0';
			}
			
			if(corporation == '+')
			{
				H+= Convert.ToDouble(txt_calc.Text);
				double sumRes;
				
				sumRes = Sum + H ;
				
				txt_calc.Clear();
				
				txt_calc.Text = Sum + "+" + H + "=" + sumRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;
				
				Sum = '\0';
				H = '\0';
			}
			
			if(corporation == 'c')
			{
				H += Convert.ToDouble(txt_calc.Text);
				double xyRes;
				xyRes = Math.Pow(XY  , H );
				
				txt_calc.Clear();
				
				txt_calc.Text = XY + "^" + "(" + H + ")" + "=" + xyRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;
				
				
				XY = '\0';
				H = '\0';
				
			}
			
		}
		
		
		void Btn_mod_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				double cotMath;
				double cotRes;
				string absSave;
				
				cotMath = double.Parse(txt_calc.Text);
				absSave = txt_calc.Text;
				txt_calc.Clear();
				
				cotRes = Math.Abs(cotMath);
				
				txt_calc.Clear();
				
				txt_calc.Text = "abs" + "(" + absSave  + ")" + "=" + cotRes.ToString();
				txt_calc.ForeColor = Color.DarkGreen;
			}
		}
		
		void BtnXY_Click(object sender, EventArgs e)
		{
			if(txt_calc.Text=="")
			{
				MessageBox.Show("لطفا یک عدد را وارد نمایید.", "تذکر", MessageBoxButtons.OK, MessageBoxIcon.Warning,
                MessageBoxDefaultButton.Button1, MessageBoxOptions.RightAlign | MessageBoxOptions.RtlReading);
			}
			
			if(txt_calc.Text!="")
			{
				XY += Convert.ToDouble(txt_calc.Text);
				corporation ='c';
				txt_calc.Clear();
				
			}
		}
		
	}
}

