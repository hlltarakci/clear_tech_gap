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



