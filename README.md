Download Link: https://assignmentchef.com/product/solved-cse225l-lab-03-template-class-and-operator-overloading
<br>
<strong> </strong>Recall the class we used in the previous lab to allocate memory dynamically. Modify the header file and the source file given below so that they now work as template class (the array elements in the dynamically allocated memory can be any type as the user defines).

<table width="0">

 <tbody>

  <tr>

   <td width="334"><strong>dynarr.h </strong> #ifndef DYNARR_H_INCLUDED#define DYNARR_H_INCLUDED class dynArr{     private:int *data;         int size;public:dynArr(int);        ~dynArr();void setValue(int, int);        int getValue(int);}; #endif // DYNARR_H_INCLUDED</td>

   <td width="378"><strong>dynarr.cpp </strong> #include “dynarr.h” #include &lt;iostream&gt; using namespace std; dynArr::dynArr(int s){data = new int[s];     size = s;}dynArr::~dynArr(){delete [] data;}int dynArr::getValue(int index){return data[index];}void dynArr::setValue(int index, int value){data[index] = value;}</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong><u>Task 2:</u> </strong>Recall the complex number class we discussed in our lectures. Modify the class and overload the <strong>*</strong> (multiplication) and the <strong>!=</strong> (not equal) operators for the class given below. <strong> </strong>

<table width="0">

 <tbody>

  <tr>

   <td width="334"><strong>complex.h </strong> #ifndef COMPLEX_H_INCLUDED#define COMPLEX_H_INCLUDED class Complex{     public:     Complex();Complex(double, double);     Complex operator+(Complex);     void Print();     private:double Real, Imaginary;}; #endif // COMPLEX_H_INCLUDED</td>

   <td width="378"><strong>complex.cpp </strong> #include “complex.h”#include &lt;iostream&gt; using namespace std; Complex::Complex(){Real = 0;Imaginary = 0;}Complex::Complex(double r, double i){Real = r;Imaginary = i;}Complex Complex::operator+(Complex a){Complex t;t.Real = Real + a.Real;t.Imaginary = Imaginary + a.Imaginary;     return t;}void Complex::Print(){cout &lt;&lt; Real &lt;&lt; endl;     cout &lt;&lt; Imaginary &lt;&lt; endl;} </td>

  </tr>

 </tbody>

</table>


