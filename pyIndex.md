# Python Index
## Basics
data types: String(str), Integer(int), Boolean(bool), List/arrays
	bool: 'True' or 'False' values (no 'true' or 'false')
	type(): prints the datatype of an argument
	Conversion: int(), str(), list(), tuple()
	Slice: x[start:stop:step]. Works for any data type

String: s.lower(), replace(s,ch), s.capitalize, s.upper, s[:], 
		s.strip, s.lstrip, s.rstrip, s.islower, 
		s.isupper, s.split("arg"), max(s)

'()': tuples. Immutable, add comma at the end as convention
	methods: del(tp), tp[index], tp.count(arg) 

'[]' Or list(): List of values
	methods: len(ls), ls.insert(index, arg), ls.remove(arg), 
		ls.pop(), del(arg), ls.clear(), ls.reverse(), 
		ls.sort(), ls.append(), ls.count(arg)

'{}' Or set(): Set of values. No repetition of values
 
'{}': Dictionaries if they have key/value pairs. 
	disclaimer: String keys have to be in quotes
	methods: d[k], d.get(k), d.pop(k), d.clear(), del(d), d.keys(), d.values(), d.items -> prints k,v, d.update(k:v)
		d.update({k: v})

Operators: Typical, single programming operators, while the rest have exceptions
	reassignment: +=, -=, /=, or *= (no ++ or --)
	logical: and, or, not/! (no && or ||)

Overload Operators: 'def __add__(self, other)' 

Functions: Functions start with the word 'def' and are loosely typed
	keyword arg: e.g. 'sum(arg2=3, arg1=10'
	default arg: e.g. 'def sum(arg1=10, arg2)' 10 is default until specified
	multi-args: put '*' infront of arg, e.g. 'prints(arg, *arg2)'
	multi-key args: put '**' infront of arg, e.g. 'prints(arg, **arg2)
		disclaimer: Remember to print of key/value pairs for each multi-arg
		
OOP:	Encapsulation, abstraction, polymorphism, inheritance, classes, and instances

Encapsulation: 
	Private: double underscore preceding the name. Can only be called through a self method
	Partially private: single underscore preceeding

Inheritance: e.g. 'class Square(Polygon)' instead of 'extends' keyword
	Child class is derived from parent class. Parent class is the base class

Classes: uses '__init__' method to initialize an instance and self is used in replacement of 'this'
	Standards: Class names should be in Camelcase 'ThisIsExample'

Instances: are objects of a class, e.g. Honda is a car
	Should be all lowercase 'honda'
	Words in an instance var name should be seperated with an underscore
	Non-public inst var should begin with a single underscore
	For private var, two underscores begin the name

Escape characters: Put a back slash before the character to be escaped
	characters: \\, \", \', \n, \t

Concatenation: You can concatenate strings/chars and even multiply them
	Tips: print function automatically adds spaces between arguments

Placeholders: Use numbers in curly brackets or % w/ letter (%d,%s,%2f)
		Examples: print('They are {0} and {1}'.format(x,y))
			  print('They are %d and %d' % (x, y))

Help: help(), dir(__builtins__), help(<fname>), dir(<fname>)

Comments: # for single comments, and """ """ for multiple-line quotes

Error: To try and catch errors
	try: 'try:'
	catch: 'except Exception as e:'

Virtual Environment: Create a seperate virtual environment in Python
	###methods
	'python3 -m venv <environmentname>': creates virtual environment
	'source <envpath>/bin/activate': puts the shell in virtual environment mode which includes env's path
	'deactivate': returns the shell back to normal

## Modules
### Builtin Modules: Module names should always be in lowercase

I/O: 
	###methods
	input()
	open(): open(<filename>, opt) 
	opt: 'w', 'a', 'r', 'x'	

math: 
	###methods
	pow(), e, pi, log, log10, log2

os: 
	###methods
	system("google-chrome google.com"), mkdir, rmdir, rename, 
	getcwd

shutil: 
	###methods
	copy() 

datetime: 
	###methods
	strftime(), today(), strptime()

sys: 
	###methods
	stdout.write()
	exit()
	
argparse:
	###methods
	<var> = argpase.ArgumentParser()
	<var>.add_argument('--foo', help='foo help')
	<var> = parser.parse_args()

### 3rd Party Modules:

glob: returns the list of files with their full path and is more powerful
	than os.listdir. Glob uses wildcards
	###Methods
	glob()

opencv: use 'import cv2' statement and make sure to use xml detector file
	###methods
	cv2.CascadeClassifier(<Haarcascade XML file for faces>)
	cv2.imread(<singleimagefile>)
	cv2.cvtColor(<singleimagevar>, cv2.COLOR_BGR2GRAY)
		^^Converts the image to grayscale
	detect.detectMultiScale(<convertedgrayimage>, 1.20, 5)
	for (x, y, w, h) in face:
        cv2.rectangle(<singleimagevar>, (x, y), (x+w, y+h), (0, 255, 0), 2)

	cv2.imshow("Detect Multiple Images", <singleimagevar>)
	cv2.waitKey(2000)
	cv2.destroyAllWindows()

pyinstaller: Convert python program to exe program
	###methods
	Easy with many files: 'pyinstaller <pyprogram>'
	One file: 'pyinstaller <pyprogram> --onefile --noconsole --icon=<iconname>'
	###options
	--name: give a name to the executable
	--onefile: make a single container file for the executable
	--noconsole: no console output when executable is ran
	--w: (")
	--icon: Add an icon to the program