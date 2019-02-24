# Test of Git Config core.autocrlf

This is to test various effects of Git's config core.autocrlf.

My conclusion:
* It's OK to leave core.autocrlf unset(false by default) so Git won't care EOL and you can commit text files with CRLF and/or LF as you want.
* If you want to unify/normalize EOL to LF, set core.autocrlf to "input", so Git won't do conversion for EOL on checkout, but will do it on checkin to normalize EOL to LF. 

References:
* https://stackoverflow.com/questions/3206843/how-line-ending-conversions-work-with-git-core-autocrlf-between-different-operat
* https://git-scm.com/docs/gitattributes
* https://help.github.com/en/articles/dealing-with-line-endings
