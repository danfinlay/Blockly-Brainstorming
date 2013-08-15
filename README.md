The current program looks  intimidating even to seasoned programmers, let alone children or novices, our more likely target with such a tool.

Much of this confusion comes from the complexity of representing Javascript's full syntax.  It's an interesting proof of concept, but requires more massaging than I'm likely to want to commit, to make it really smooth and fun for newcomers.

When inventing Node, nobody said we needed to make sure we can import Ruby before we move forward.  Instead, Node was given NPM, an easy and fun way for people to share chunks of logic.

Much like NPM can have modules written entirely in Javascript or simply be Javascript scaffoldings around other programs, what NPM does is define a common syntax for modularizing code, and that's where it gets its power.

Since the blockly to Javascript conversion is already built, and the JS-to-Blockly is the source of all our pain, I have to consider the merits that might be explored by simply building an NPM for Blockly.

So here's what we'd do:

Define a protocol for binding a block-based API to, say, node-style (common.js) javascript modules.  These block-modules (blodules) would be defined by their author, and could exist in an npm-style survival-of-the-fittest-yet-cooperative anarchy.

These blodules would define sets of blocks that could be displayed in a list added to the left sidebar of blockly.

A new titlebar (or something) would give access to adding new blojules to the current project.

One up-side of defining an standard for defining a block-to-Javascript interface would be that calling methods of an object could be an implicit characteristic of a block.  Rather than getting an "attr: name" block to add to your "person" block, a person block could have a drop-down menu of their defined attributes.  Once one is selected, that attribute might also have a drop-down, or if it's a callback function, it could expand the whole block into a callback-scope style block.

By the way, I think blocks should support spillover:

More blockly-specific review:

Is there a way to make spillover blocks?

Is there a way to make variable blocks available within a scope?  Drag-and-drop blocks that are dragged from a block defining variables?  (Stencyl style).