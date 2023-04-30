Download Link: https://assignmentchef.com/product/solved-ece-210b-homework-6
<br>



This homework deals with digital filters in a low-level sense. You are expected to know a bit about the z-transform, but if you are not in Signals and Systems, please contact me separately for some additional information on this homework if you need it. Read the parts carefully and make sure to complete every part of the homework. This homework requires you to produce a few plots; I want nice plots! Axis labels and titles are a must.

<ol>

 <li>For this question, you will be working with the discrete system described bythe transfer function:

  <ul>

   <li>Store this transfer function as numerator and denominator polynomials. Be <strong>VERY </strong>careful setting this up. Check the documentation for <em>zplane </em>to see how discrete transfer functions are handled in MATLAB.</li>

   <li>Compute the poles and zeros using a specific MATLAB function. (Make sure you use the right one for discrete signals and not the one used mostly for continuous signals!)</li>

   <li>Create a poly zero plot using a different MATLAB function. You may use either the poles and zeros themselves or the numerator and denominator polynomials.</li>

   <li>Use <em>impz </em>to compute the impulse response of this transfer function. Compute only the first 50 points of it (there is a way to do this in the function itself). Make a stem plot of the impulse response.</li>

   <li>Let. Then use <em>filter </em>to apply the transfer function (or filter) to the signal. In subplots, plot the before and after.</li>

   <li>The above is the easiest way to apply a filter, but you also ought to be able to do this analytically, using either convolution in MATLAB or the product of z-transforms. Show me you know how to do this! That is, plot the same answer achieved in another way. You don’t have to take any inverse z-transforms to do this! Note that if you use convolution with the impulse response, you’ll get a longer vector than when you used filter. Therefore, only plot the first n points where n is the length of the vector result from the previous part.</li>

  </ul></li>

 <li>In this question, you will be ”designing” a bandpass filter (probably unrealisticbut it’s what I came up with). A bandpass filter is a system which only allows a certain band of frequencies from a signal to pass.</li>

</ol>

1

ECE-210B Homework 6

<ul>

 <li>Last question you converted a transfer function in tf form to one in zpk form. Now we will do the opposite. Compute numerator and denominator vectors for a transfer function with <em>k </em>= 0<em>.</em>01 and these zeros and poles:</li>

</ul>

<em>zeros </em>: −1<em>, </em>1

<ul>

 <li>Create a pole-zero plot.</li>

 <li>Now compute the frequency response of this filter using <em>freqz</em>. Use <em>n </em>= 1024 points and return an <em>H </em>frequency response vector and a <em>w </em>frequency vector. <strong>DO NOT </strong>use the option to plot the frequency response. You will be manually creating the plots.</li>

 <li>The <em>H </em>vector is a complex vector. That means it has both magnitude gain (via <em>abs</em>) and phase (via <em>angle</em>). Using subplots, plot the magnitude and phase against the <em>w </em>frequency vector. A few things to note (and will be expected in addition to proper plots):

  <ul>

   <li>Plot the magnitude in dB. You can convert a gain <em>x </em>to dB via</li>

  </ul></li>

</ul>

20<em>log</em><sub>10</sub>(<em>x</em>).

<ul>

 <li>Plot the phase in degrees. You will notice if you do that, the plot will have weird sharp edges. Remove them using <em>unwrap before </em>converting to degrees.</li>

 <li>Show units in the axis labels. (Remember the frequency vector, <em>w</em>, has units <em>radians </em>not radians per second.)</li>

 <li>Remember the frequency vector, <em>w</em>, only goes from 0 to <em>π</em>. Make sure to use <em>xlim</em>, <em>xticks </em>and <em>xticklabels</em>.</li>

</ul>


