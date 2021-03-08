
.. _Keck-FOBOS: https://github.com/Keck-FOBOS
.. _Kyle Westfall: westfall@ucolick.org
.. _ScienceRequirements: https://github.com/Keck-FOBOS/ScienceRequirements
.. _FOBOS Document Structure: https://uco.atlassian.net/wiki/spaces/FOB/pages/405700609/Document+Structure

FOBOS Documentation Template in LaTex
-------------------------------------

To start a new document:

    1. Checkout the repository into a directory named after the document
       you're writing:

        .. code-block::

            git clone https://github.com/Keck-FOBOS/LaTexDocTemplate.git ${DocName}

    2. Remove the git infrastructure, ensuring that edits you make are
       not pushed to the template doc.  **To create a new repo for this
       document and to link it in Overleaf, see below.**

        .. code-block::

            cd ${DocName}
            rm -fR .git

    3. Change the name of the main document file:

        .. code-block::

            mv FOBOS_Template.tex FOBOS-${DocName}.tex

    4. In ``FOBOS-${DocName}.tex``, edit the document name, numbering,
       and date.  This also contains the main text of the document and
       the revision history.

    5. Edit the author list in ``authors.tex``.

    6. Edit the contact information for the corresponding author in
       ``corresponding.tex``.

    7. Add any (additional) tex aliases you want to ``aliases.tex``.

    8. Include any ``BibTex`` references in ``ref.bib``.


For an example FOBOS design document, see the `ScienceRequirements`_
document.  For the document numbering scheme, see the `FOBOS Document
Structure`_.

To compile:

.. code-block::

    pdflatex FOBOS-${DocName}
    pdflatex FOBOS-${DocName}
    bibtex FOBOS-${DocName}
    pdflatex FOBOS-${DocName}
    pdflatex FOBOS-${DocName}


Adding doc as a new GitHub repository and linking to Overleaf
=============================================================

It is preferred that you add the doc to the main `Keck-FOBOS`_
organization repository.  To get access, e-mail `Kyle Westfall`_.

To create the repository:

 1. Go to: https://github.com/Keck-FOBOS

 2. Click the "New" button to the right.

 3. Give the repository a name relevant to the doc (we haven't
    formalized this yet) and create it.  It is preferred that you create
    a *private* repository for design documents; these can be changed to
    public later.

 4. The above step creates an empty repository.  Follow the GitHub
    instructions for adding the relevant LaTex files for you doc.  Do
    not add ancillary compilation files!  And take care not to add
    excessively large files.



