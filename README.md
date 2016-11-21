This script is a modified version of the relinkDarkEntities.py script found in [https://github.com/cltl/entity-link-postprocess] The only modification is that it is made to work in the pipeline mode (reading the input from stdin) 

What it does:
-------------

This script takes a NAF file, and for every entity without a link, it checks whether there are entity mentions that show a high overlap with entity mentions that do have a link, after which that link is added to the previously unlinked entity. For example if the entity "David Cameron" has a link, but "Cameron" mentioned in another part of the article doesn't, then the link from "David Cameron" is added to the "Cameron" mention. It also adds links for "Mr. So and so" and "Mrs. So and so" if there is an entity mention "So and so" that has a link.

