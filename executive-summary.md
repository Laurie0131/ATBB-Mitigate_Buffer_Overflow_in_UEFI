<!--- @file
  Executive Summary

  Copyright (c) 2018, Intel Corporation. All rights reserved.<BR>

  Redistribution and use in source (original document form) and 'compiled'
  forms (converted to PDF, epub, HTML and other formats) with or without
  modification, are permitted provided that the following conditions are met:

  1) Redistributions of source code (original document form) must retain the
     above copyright notice, this list of conditions and the following
     disclaimer as the first lines of this file unmodified.

  2) Redistributions in compiled form (transformed to other DTDs, converted to
     PDF, epub, HTML and other formats) must reproduce the above copyright
     notice, this list of conditions and the following disclaimer in the
     documentation and/or other materials provided with the distribution.

  THIS DOCUMENTATION IS PROVIDED BY TIANOCORE PROJECT "AS IS" AND ANY EXPRESS OR
  IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
  MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO
  EVENT SHALL TIANOCORE PROJECT  BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
  SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
  PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
  OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
  WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
  OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS DOCUMENTATION, EVEN IF
  ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

-->
**Introduction**
A buffer overflow is “one of the most important exploitation techniques in the history of computer security.”  [ [Tanenbaum](https://www.amazon.com/s/ref=dp_byline_sr_book_1?ie=UTF8&field-author=Andrew+S.+Tanenbaum&search-alias=books&text=Andrew+S.+Tanenbaum&sort=relevancerank )]<sup>[[1]](#Tanenbaum)</sup> “Buffer overflows are ideally suited for introducing three of the most important protection mechanisms available in most modern systems: stack canaries, data execution protection, and address-space layout randomization.” [[Tanenbaum](https://www.amazon.com/s/ref=dp_byline_sr_book_1?ie=UTF8&field-author=Andrew+S.+Tanenbaum&search-alias=books&text=Andrew+S.+Tanenbaum&sort=relevancerank )] <sup>[[1]](#Tanenbaum)</sup> However, the current UEFI firmware implementation only adopted a few of these mechanisms. This paper will introduce how to enable the protection mechanisms in UEFI firmware to harden the pre-boot phase.
<BR>
<BR>
<BR>
<hr>
<a name="Tanenbaum">[1] </a> [ [Tanenbaum](https://www.amazon.com/s/ref=dp_byline_sr_book_1?ie=UTF8&field-author=Andrew+S.+Tanenbaum&search-alias=books&text=Andrew+S.+Tanenbaum&sort=relevancerank )] Modern Operating Systems, 4th edition, Andrew S. Tanenbaum, Herbert Bos, Pearson, 2014, ISBN: 978-0133591620 
