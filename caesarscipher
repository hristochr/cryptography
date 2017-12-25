namespace CaesarsCypher
{

    using System;
    using System.Text;

    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Please input text to ecnrypt:");
            string text = Console.ReadLine();
            int s = 0;
            Console.WriteLine("Please input shift: ");
            try
            {
                s = int.Parse(Console.ReadLine());
            }
            catch (Exception)
            {

                throw new ArgumentException("Error. The number must be an integer.");
            }

            Console.WriteLine($"Text: {text}");
            Console.WriteLine($"Shift: {s.ToString()}");
            Console.WriteLine($"Cipher: {Encrypt(text, s)}");
        }

        private static string Encrypt(string text, int s)
        {
            StringBuilder result = new StringBuilder();
            for (int i = 0; i < text.Length; i++)
            {
                char c = text[i];
                if (char.IsUpper(c))
                {
                    result.Append(Convert.ToChar(((c) + s - 65) % 26 + 65));
                }
                else if (char.IsLower(c))
                {
                    result.Append(Convert.ToChar(((c) + s - 97) % 26 + 97));
                }
            }
            
            return result.ToString();
        }
    }
}
