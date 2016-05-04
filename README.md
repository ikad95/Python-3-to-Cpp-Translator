Note:
	Use python3 syntax, ie print("hello") instead of print "hello" and while(i<5): instead of while i<5:
	Use tab instead of space to indent. So don't write in IDLE as it uses whitespace. Sublime Text or any other good editor will work
	The C++ code won't print a new line like python! so do double check!

How to use:

	In the directory write your code in toTranslate.py
	run py2cpp.py
	voila! The C++ code should be in Translated.cpp file



In the future :
Dynamic type checking is awesome, but C++ doesn't allow that!!
The process of adding dynamic type checking support has already started! Until then be safe!

So you'll be able to do this 

In Python -

n=4
if(n==4):
	n="FOUR"
print(n)


Translated C++ code will look like this - 

int main()
{
	long long n_ll;
	string n_str;

	n_ll=4;
	if(n_ll==4)
	{
		n_str="FOUR";

	}
	cout<<n_str;
	return 0;
}

Currently as of today the C++ code looks like this -

int main()
{
	string n;

	n=4;
	if(n==4)
	{
		n="FOUR";
	
	}
	cout<<n;
	return 0;
}

Clearly this won't compile! It's initializing n with its last data type!  