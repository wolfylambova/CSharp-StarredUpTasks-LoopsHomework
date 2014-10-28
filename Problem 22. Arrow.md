using System;

    class Arrow
    {
        static void Main()
        {
            int nWidth = int.Parse(Console.ReadLine());

            int height = 2 * nWidth - 1;
            int dotPadding = nWidth / 2;
            int sharpMiddle = nWidth;
            int dotMiddle = nWidth-2;

            for (int i = 0; i < nWidth; i++)
            {
                if (i==0)
                {
                    string pads = new string('.',dotPadding);
                    string sharp = new string('#', sharpMiddle);
                    Console.WriteLine(pads+sharp+pads);
                }
                if (i== (nWidth-1))
                {
                    string pads = new string('#', dotPadding+1);
                    string dot = new string('.', sharpMiddle-2);
                    Console.WriteLine(pads+ dot  + pads);
                }
                else 
                {
                    string pads = new string('.', dotPadding);
                    string sharp = new string('#',1);
                    string dot = new string('.', sharpMiddle-2);
                    Console.WriteLine(pads+sharp + dot + sharp + pads);
                }

            }
            int dotPad = 1;
            int sharp1 = 1;
            
            for (int i = 0; i < nWidth-2; i++)
            {
                int middleDot = (nWidth * 2) - (2 * dotPad + 2 * sharp1)-1;
                
                string dot1 = new string('.',dotPad);
                string dot2 = new string('.',middleDot);
                string sharps = new string('#',sharp1);
                Console.WriteLine(dot1+sharps+dot2+sharps+dot1);
                dotPad++;
                do
                {
                    middleDot-=2;
                } while (i==(nWidth-2));

                //if (i==(nWidth-2))
                //{
                //      string dott = new string('.',(nWidth-1));
                //      string sharpp = new string('#',1); 
                //      Console.WriteLine(dott+sharpp+dott);
                //}
             }
           
                string dott = new string('.', (nWidth - 1));
                string sharpp = new string('#', 1);
                Console.WriteLine(dott + sharpp + dott);
        }
    }

