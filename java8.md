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








