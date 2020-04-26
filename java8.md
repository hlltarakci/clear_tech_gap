### Javadoc - Java 8
- https://docs.oracle.com/javase/8/docs/api/
- https://docs.oracle.com/javase/8/docs/api/java/lang/String.html
- https://docs.oracle.com/javase/8/docs/api/java/lang/StringBuilder.html
- https://docs.oracle.com/javase/8/docs/api/java/lang/Character.html
- https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html
- https://docs.oracle.com/javase/8/docs/api/java/util/List.html
- https://docs.oracle.com/javase/8/docs/api/java/util/Collection.html
- https://docs.oracle.com/javase/8/docs/api/java/util/Collections.html
- https://docs.oracle.com/javase/8/docs/api/java/util/Arrays.html
- https://docs.oracle.com/javase/8/docs/api/java/util/ArrayList.html
- https://docs.oracle.com/javase/8/docs/api/java/util/LinkedList.html
- https://docs.oracle.com/javase/8/docs/api/java/util/Hashtable.html
- https://docs.oracle.com/javase/8/docs/api/java/util/HashMap.html
- https://docs.oracle.com/javase/8/docs/api/java/util/HashSet.html
- https://docs.oracle.com/javase/8/docs/api/java/util/Map.html
- https://docs.oracle.com/javase/8/docs/api/java/util/Set.html
- https://docs.oracle.com/javase/8/docs/api/java/util/Deque.html
- https://docs.oracle.com/javase/8/docs/api/java/util/ArrayDeque.html
- https://docs.oracle.com/javase/8/docs/api/java/util/Stack.html
- https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html
- https://docs.oracle.com/javase/8/docs/api/java/util/PriorityQueue.html
- https://docs.oracle.com/javase/8/docs/api/java/util/Comparator.html
- https://docs.oracle.com/javase/8/docs/api/java/util/TreeSet.html
- https://docs.oracle.com/javase/8/docs/api/java/util/TreeMap.html
- https://docs.oracle.com/javase/8/docs/api/java/util/LinkedHashMap.html

## [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)
java.lang

char 	charAt(int index)
Returns the char value at the specified index.

int 	compareTo(String anotherString)
Compares two strings lexicographically.

int 	compareToIgnoreCase(String str)
Compares two strings lexicographically, ignoring case differences.

boolean 	endsWith(String suffix)
Tests if this string ends with the specified suffix.

boolean 	equals(Object anObject)
Compares this string to the specified object.

boolean 	equalsIgnoreCase(String anotherString)
Compares this String to another String, ignoring case considerations.

int 	indexOf(int ch)
Returns the index within this string of the first occurrence of the specified character.

int 	indexOf(int ch, int fromIndex)
Returns the index within this string of the first occurrence of the specified character, starting the search at the specified index.

int 	indexOf(String str)
Returns the index within this string of the first occurrence of the specified substring.

int 	indexOf(String str, int fromIndex)
Returns the index within this string of the first occurrence of the specified substring, starting at the specified index.

boolean 	isEmpty()
Returns true if, and only if, length() is 0.

int 	lastIndexOf(int ch)
Returns the index within this string of the last occurrence of the specified character.

int 	lastIndexOf(int ch, int fromIndex)
Returns the index within this string of the last occurrence of the specified character, searching backward starting at the specified index.

int 	lastIndexOf(String str)
Returns the index within this string of the last occurrence of the specified substring.

int 	lastIndexOf(String str, int fromIndex)
Returns the index within this string of the last occurrence of the specified substring, searching backward starting at the specified index.

int 	length()
Returns the length of this string.

String 	replace(char oldChar, char newChar)
Returns a string resulting from replacing all occurrences of oldChar in this string with newChar.

String[] 	split(String regex)
Splits this string around matches of the given regular expression.

boolean 	startsWith(String prefix)
Tests if this string starts with the specified prefix.

String 	substring(int beginIndex)
Returns a string that is a substring of this string.

String 	substring(int beginIndex, int endIndex)
Returns a string that is a substring of this string.

char[] 	toCharArray()
Converts this string to a new character array.

String 	toLowerCase()
Converts all of the characters in this String to lower case using the rules of the default locale.

String 	toUpperCase()
Converts all of the characters in this String to upper case using the rules of the default locale.

String 	trim()
Returns a string whose value is this string, with any leading and trailing whitespace removed.

static String 	valueOf(boolean b)
Returns the string representation of the boolean argument.

## [StringBuilder](https://docs.oracle.com/javase/8/docs/api/java/lang/StringBuilder.html)
java.lang

StringBuilder()
Constructs a string builder with no characters in it and an initial capacity of 16 characters.

StringBuilder(int capacity)
Constructs a string builder with no characters in it and an initial capacity specified by the capacity argument.

StringBuilder(String str)
Constructs a string builder initialized to the contents of the specified string.

StringBuilder 	append(boolean b)
Appends the string representation of the boolean argument to the sequence.

StringBuilder 	append(char[] str)
Appends the string representation of the char array argument to this sequence.

StringBuilder 	append(char[] str, int offset, int len)
Appends the string representation of a subarray of the char array argument to this sequence.

StringBuilder 	append(String str)
Appends the specified string to this character sequence.

StringBuilder 	append(StringBuffer sb)
Appends the specified StringBuffer to this sequence.

char 	charAt(int index)
Returns the char value in this sequence at the specified index.

StringBuilder 	delete(int start, int end)
Removes the characters in a substring of this sequence.

StringBuilder 	deleteCharAt(int index)
Removes the char at the specified position in this sequence.

void 	getChars(int srcBegin, int srcEnd, char[] dst, int dstBegin)
Characters are copied from this sequence into the destination character array dst.

int 	indexOf(String str)
Returns the index within this string of the first occurrence of the specified substring.

int 	indexOf(String str, int fromIndex)
Returns the index within this string of the first occurrence of the specified substring, starting at the specified index.

StringBuilder 	insert(int offset, boolean b)
Inserts the string representation of the boolean argument into this sequence.

StringBuilder 	insert(int offset, char[] str)
Inserts the string representation of the char array argument into this sequence.

StringBuilder 	insert(int index, char[] str, int offset, int len)
Inserts the string representation of a subarray of the str array argument into this sequence.

StringBuilder 	insert(int offset, String str)
Inserts the string into this character sequence.

int 	lastIndexOf(String str)
Returns the index within this string of the rightmost occurrence of the specified substring.

int 	lastIndexOf(String str, int fromIndex)
Returns the index within this string of the last occurrence of the specified substring.

int 	length()
Returns the length (character count).

StringBuilder 	replace(int start, int end, String str)
Replaces the characters in a substring of this sequence with characters in the specified String.

StringBuilder 	reverse()
Causes this character sequence to be replaced by the reverse of the sequence.

void 	setCharAt(int index, char ch)
The character at the specified index is set to ch.

void 	setLength(int newLength)
Sets the length of the character sequence.

String 	substring(int start)
Returns a new String that contains a subsequence of characters currently contained in this character sequence.

String 	substring(int start, int end)
Returns a new String that contains a subsequence of characters currently contained in this sequence.

String 	toString()
Returns a string representing the data in this sequence.

## [Character](https://docs.oracle.com/javase/8/docs/api/java/lang/Character.html)
java.lang

char 	charValue()
Returns the value of this Character object.

static int 	compare(char x, char y)
Compares two char values numerically.

int 	compareTo(Character anotherCharacter)
Compares two Character objects numerically.

static int 	getNumericValue(char ch)
Returns the int value that the specified Unicode character represents.

static boolean 	isDigit(char ch)
Determines if the specified character is a digit.

static boolean 	isLetter(char ch)
Determines if the specified character is a letter.

static boolean 	isLetterOrDigit(char ch)
Determines if the specified character is a letter or digit.

static boolean 	isLowerCase(char ch)
Determines if the specified character is a lowercase character.

static boolean 	isSpaceChar(char ch)
Determines if the specified character is a Unicode space character.

static boolean 	isUpperCase(char ch)
Determines if the specified character is an uppercase character.

static boolean 	isWhitespace(char ch)
Determines if the specified character is white space according to Java.

static char 	reverseBytes(char ch)
Returns the value obtained by reversing the order of the bytes in the specified char value.

static char 	toLowerCase(char ch)
Converts the character argument to lowercase using case mapping information from the UnicodeData file.

String 	toString()
Returns a String object representing this Character's value.

static String 	toString(char c)
Returns a String object representing the specified char.

static char 	toUpperCase(char ch)
Converts the character argument to uppercase using case mapping information from the UnicodeData file.

static Character 	valueOf(char c)
Returns a Character instance representing the specified char value.

## [Math](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html)
java.lang

static double 	abs(double a)
Returns the absolute value of a double value.

static float 	abs(float a)
Returns the absolute value of a float value.

static int 	abs(int a)
Returns the absolute value of an int value.

static long 	abs(long a)
Returns the absolute value of a long value.

static double 	ceil(double a)
Returns the smallest (closest to negative infinity) double value that is greater than or equal to the argument and is equal to a mathematical integer.

static double 	floor(double a)
Returns the largest (closest to positive infinity) double value that is less than or equal to the argument and is equal to a mathematical integer.

static double 	max(double a, double b)
Returns the greater of two double values.

static float 	max(float a, float b)
Returns the greater of two float values.

static int 	max(int a, int b)
Returns the greater of two int values.

static long 	max(long a, long b)
Returns the greater of two long values.

static double 	min(double a, double b)
Returns the smaller of two double values.

static float 	min(float a, float b)
Returns the smaller of two float values.

static int 	min(int a, int b)
Returns the smaller of two int values.

static long 	min(long a, long b)
Returns the smaller of two long values.

static double 	pow(double a, double b)
Returns the value of the first argument raised to the power of the second argument.

static double 	random()
Returns a double value with a positive sign, greater than or equal to 0.0 and less than 1.0.

static long 	round(double a)
Returns the closest long to the argument, with ties rounding to positive infinity.

static int 	round(float a)
Returns the closest int to the argument, with ties rounding to positive infinity.

static double 	sqrt(double a)
Returns the correctly rounded positive square root of a double value.
























