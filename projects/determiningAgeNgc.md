---
layout: project
type: project
image: img/
title: "Determining the Age of NGC 6791 Through BVI Data"
date: 2022-2023
published: true
labels:
  - Fortran
summary: "Utilizing MESA Star 1D modeling (modeling with graphs) to study the age of NGC 6791"
---

<div class="text-center p-4">
  <img width="200px" src="../img/" class="img-thumbnail" >
</div>

Paragraph here

```cpp
byte ADCRead(byte ch)
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```

