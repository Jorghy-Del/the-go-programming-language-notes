
# Table of Contents

1.  [Program Structure](#org52d920e)
    1.  [2.1 Names](#org5c866c0)



<a id="org52d920e"></a>

# Program Structure

This chapter deals with the basic structural elements like variable, type declarations, packages, files, scope etc.

An entity can be a function, type, variable or constant. The keywords `func`, `type`, `var` and `const` denote these entities.


<a id="org5c866c0"></a>

## 2.1 Names

1.  Naming follows simple rules

    -   a name begins with a letter or an underscore.
    -   after the initial letter/underscore, may have any number of letters, digits, and underscores.
    -   names are case sensitive, `heapSort` and `HeapSort` are different names.
    
    Package names are in lower case.
    There is no limit on name length. Short names preferred.
    
    Camel case convention. No snake case.
    Letters of acronyms like ASCII, HTML are always in same case.
    Preferred - `htmlEscape`, `HTMLEscape`, `escapeHTML`.
    Not preferred - `escapeHtml`.

2.  Go has 25 keywords

    <table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
    
    
    <colgroup>
    <col  class="org-left" />
    
    <col  class="org-left" />
    
    <col  class="org-left" />
    
    <col  class="org-left" />
    
    <col  class="org-left" />
    </colgroup>
    <tbody>
    <tr>
    <td class="org-left">break</td>
    <td class="org-left">case</td>
    <td class="org-left">chan</td>
    <td class="org-left">const</td>
    <td class="org-left">continue</td>
    </tr>
    
    
    <tr>
    <td class="org-left">default</td>
    <td class="org-left">defer</td>
    <td class="org-left">else</td>
    <td class="org-left">fallthrough</td>
    <td class="org-left">for</td>
    </tr>
    
    
    <tr>
    <td class="org-left">func</td>
    <td class="org-left">go</td>
    <td class="org-left">goto</td>
    <td class="org-left">if</td>
    <td class="org-left">import</td>
    </tr>
    
    
    <tr>
    <td class="org-left">interface</td>
    <td class="org-left">map</td>
    <td class="org-left">package</td>
    <td class="org-left">range</td>
    <td class="org-left">return</td>
    </tr>
    
    
    <tr>
    <td class="org-left">select</td>
    <td class="org-left">struct</td>
    <td class="org-left">switch</td>
    <td class="org-left">type</td>
    <td class="org-left">var</td>
    </tr>
    </tbody>
    </table>

3.  Pre-declared names

    Go has the following pre-declared names for built-in constants, types and functions. These names are not reserved. They are usable in declarations.
    
    <table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
    
    
    <colgroup>
    <col  class="org-left" />
    
    <col  class="org-left" />
    </colgroup>
    <thead>
    <tr>
    <th scope="col" class="org-left">Constants</th>
    <th scope="col" class="org-left">true false iota</th>
    </tr>
    </thead>
    
    <tbody>
    <tr>
    <td class="org-left">Types</td>
    <td class="org-left">int int8 int16 int64 uint8 uint16 uint32</td>
    </tr>
    
    
    <tr>
    <td class="org-left">&#xa0;</td>
    <td class="org-left">uint64 uintptr float32 float64 complex128 complex64</td>
    </tr>
    
    
    <tr>
    <td class="org-left">&#xa0;</td>
    <td class="org-left">bool byte rune string error</td>
    </tr>
    </tbody>
    
    <tbody>
    <tr>
    <td class="org-left">Functions</td>
    <td class="org-left">make len cap new append copy close delete</td>
    </tr>
    
    
    <tr>
    <td class="org-left">&#xa0;</td>
    <td class="org-left">complex real imag panic recover</td>
    </tr>
    </tbody>
    </table>

4.  Exported entities

    An entity (function, type, variable or constant) declared outside of a function is visible in all files of the package to which it belongs. An entity declared within a function is local to that function.
    
    When first letter of a name is upper-case, it is *exported* - it is visible and accessible outside its own package. Names with initial letter in lower-case are visible only inside either the function to which it is local to or only the package to which it belongs.

