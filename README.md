# FileEncryption
My simple File Encryption

How it using?

filename - Mayby, I don't to explain..

password - your 8-32bit encryption string 

Read:
                
                byte[] reader = Encoding.Default.GetBytes(File.ReadAllText(filename, Encoding.BigEndianUnicode));
                string str = MWFileEncoder.DecryptTextFromBytes(reader, password);

Save:
Body - string to encryption

                string save = Encoding.Default.GetString(MWFileEncoder.EncryptTextToBytes(Body, password));              
                File.WriteAllText(filename, save, Encoding.BigEndianUnicode);
