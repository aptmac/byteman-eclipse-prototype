This is a prototype eclipse for Byteman based on MSc project work
performed by Rebecca Simmonds at Newcastle University. It is not a
completed work. However, it does provide some important elements which
are needed to produce a full working plugin, in particular

  a complete grammar for the Byteman rule language

  a validator class which spots the few errors not caught by the syntax

  byteman rule template generator

  syntax highlighting

  content assistance including auto completion for CLASS and METHOD
  clauses and for various rule expression elements

  prototype Byteman properties configuration sheet


Eclipse Configuration

In order to build and use the plugin you will need to ensure that your
eclipse environment includes JDT, EMF, PLugin Development and XText
support. n.b. the easiest way to install XText is to install the
Eclipse marketplace client and then pull XText in form the marketplace
dialogue.

Building the Plugin

The plugin uses code autogenerated by XText from the Byteman grammar
in file

  org.jboss.byteman.eclipse.Byteman/src/org/jboss/byteman/eclipse/Byteman.xtext

The plugin should be able to build as is using the current
auto-generated sources. To run it select the
org.jboss.byteman.eclipse.Byteman component and then Run As Eclipse
Application

If you need to tweak the Byteman grammar then you will have to
regenerate the auto-generated sources before rebuilding. To do this
select file

org.jboss.byteman.eclipse.Byteman/src/org/jboss/byteman/eclipse/GenerateByteman.mwe2

and then Run As MWE2 Workflow

After the workflow has regenerated the sources using the new grammar
build and run the plugin as described above.
