# Write-a-Python-program-to-convert-any-integer-N-to-base-B-2-B-32-
Write a Python program to convert any integer N to base B (2 &lt;= B &lt;= 32)
"""
# Convert integer n to base b
#
# @author viettuts.vn
# @param n: so nguyen
# @param b: he co so
# @return he co so b
"""
def convert_number(n, b):
     if (n < 0 or b < 2 or b > 16):
         return "";
  
     sb = "";
     m = 0;
     remainder = n;
  
     while (remainder > 0):
         if (b > 10):
             m = remainder % b;
             if (m >= 10):
                 sb = sb + str(chr(55 + m));
             else:
                 sb = sb + str(m);
         else:
             sb = sb + str(remainder % b);
         remainder = int(remainder / b);
     return "".join(reversed(sb)); # reverse string sb
  
n = int(input("Enter a positive integer n = "));
print("Integer base 2", n, "is:", convert_number(n, 2))
print("Integer base 16", n, "is:", convert_number(n, 16))
