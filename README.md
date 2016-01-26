# Font_Chooser
Your program is an Applet that lets you choose:

font family
font style
foreground colour
background colour
then it displays the following test pangrams in the selected font family, style and colour.

The quick brown fox jumped over the lazy dog’s back.
Pack my box with five dozen liquor jugs.
Jackdaws love my big sphinx of quartz.
Mr. Jock, TV quiz PhD, bags few lynx.
abcdefghijklmnopqrstuvwxyz
ABCDEFGHIJKLMNOPQRSTUVWXYZ
01234567890
€†™´¸¢©¤°÷½¼¾>¡¿«‘’<¯µ ·¬ªº¶±£"»®§­¹²³ß×™¨¥
ÀÁÂÃÄÅÆÇÈÉ ÊËÌÍÎÏÐÑÒÓÔ ÕÖØÙÚÛÜÝÞÿ
àáâãäåæçèé êëìíîïðñòóô õöøùúûüýþÿ
!"#$%&'()*+,-./:;<=>?@[\^_z{|}~
uvw wW gq9 2z 5s il17|!j oO08 `'" ;:,. m nn rn {[()]}u

Hints

First you get a dynamically generate a list of all possible java fonts installed on the machine with code similar to this.
import java.awt.GraphicsEnvironment;

public class ShowFonts
{
   public static void main ( String [] args )
      {
      GraphicsEnvironment ge = GraphicsEnvironment.getLocalGraphicsEnvironment();
      String[] names = ge.getAvailableFontFamilyNames();
      for ( int i=0; i<names.length; i++ )
         {
             System.out.println( names[i] );
         }
      }
}

You can use a JColorChooser to select the foreground and background colour and a JComboBox to select the family, style, and size and use a JTextArea for the test message, Or do it with AWT (Links to an external site.) (Advanced WindowingToolkit) using ColorChooser, Choice and TextArea.
You need to set up listeners so that if anything changes, you recompute the display.
Bonus

 Display the font family menu using a font sample, but be careful, some fonts don’t work that way, like dingbats.

By Instructure
User Research
Privacy policy
Terms of service
Facebook
Twitter
