# defects4j-one-edit-degree-patches

This repository contains a set of 3250 test-suite adequate patches for the Defects4j benchmark (https://github.com/rjust/defects4j), generated by the extended version of the ARJA framework available at https://github.com/pdziurzanski/arja-manatee.



The patches are in the ARJA format. All of them are one-edit degree patches (i.e., altering one modification point only). For example, Patch_1 for Chart1 bug removes 1798 line in file AbstractCategoryItemRenderer.java

1 Delete ./bugs/chart_1/source/org/jfree/chart/renderer/category/AbstractCategoryItemRenderer.java 1798\
Faulty:\
return result;\
Seed:\
int hash=37;

In case of the Delete operation, the seed is ignored. Another patch of the same bug, Patch_10, removes three lines, from 1789 to 1791, in file AbstractCategoryItemRenderer.java and inserts line "Shape box=null;" at that position instead.

1 Replace ./bugs/chart_1/source/org/jfree/chart/renderer/category/AbstractCategoryItemRenderer.java 1797\
Faulty:\
if (dataset != null) {\
  return result;\
}\
Seed:\
Shape box=null;

As the patches in the ARJA format cannot be applied directly to the source code, they have been converted to the diff format by the Perl script available at https://github.com/pdziurzanski/arja2diff-patch-converter. That repository also includes the converted versions of these patches.

The authors acknowledge the support of the EPSRC-funded MANATEE project. 
