This colab notebook implements several 3x3 kernels:  
Horizontal Edge Detector   
45 Degree Angle Detector  
Blur Kernel  
Sharpen Kernel  
Identity function   
  
  
Channels and Kernels:  
Kernels are feature extractors, which start with detecting simple features like edges.  
Channels are similar feature bags. Each channel can be a layer, which extracts a particular type of feature.  
  
Why use 3x3 kernels only?
Easy to apply several times to get any global receptive field. You can apply 3x3 filter twice to get equivalent effect of a 5x5 filter. 

How many times should 3x3 convolution be carried out to go from 199x199 to 1x1?
We would need to convolve 20*5 = 100 times
199x199 | 3x3 > 197x197
197x197 | 3x3 > 195x195
195x195 | 3x3 > 193x193
193x193 | 3x3 > 191x191
191x191 | 3x3 > 189x189

189x189 | 3x3 > 187x187
187x187 | 3x3 > 185x185
185x185 | 3x3 > 183x183
183x183 | 3x3 > 181x181
181x181 | 3x3 > 179x179


179x179 | 3x3 > 177x177
177x177 | 3x3 > 175x175
175x175 | 3x3 > 173x173
173x173 | 3x3 > 171x171
171x171 | 3x3 > 169x169
..
..
..

