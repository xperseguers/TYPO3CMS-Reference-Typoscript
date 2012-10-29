.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. include:: ../../Includes.txt


EDITPANEL
^^^^^^^^^

This content object is inserted only if a backend user is logged in
and if a FE-editing extension is installed and loaded. What gets
displayed exactly may depend on which FE-editing extension is used.
The reference below is related to the "feedit" system extension. In
such a case the EDITPANEL also requires that the Admin Panel be
displayed (config.admPanel = 1) and that the user has checked the
"Display Edit Icons" option. Whenever the edit panel is inserted, page
caching is disabled.

The edit panel inserts icons for moving, editing, deleting, hiding and
creating records.

In conjunction with css\_styled\_content, an EDITPANEL will appear for
each content element on the page. It is also possible to insert an
EDITPANEL as cObject in the template, using TypoScript.


((generated))
"""""""""""""

Example
~~~~~~~

::

   page = PAGE
   page.10 = EDITPANEL
   page.10 {
     ...
   }

In such a case, there's nothing to edit in the FE, but the panel can
be used to create new records, for example.

.. figure:: ../../Images/icon_note.png
   :alt: Note

**Note**

The extension "feedit" needs to be installed for this to work.

.. ### BEGIN~OF~TABLE ###

.. container:: table-row

   Property
         Property:

   Data type
         Data type:

   Description
         Description:

   Default
         Default:


.. container:: table-row

   Property
         label

   Data type
         string /stdWrap

   Description
         Title for the panel. You can insert the record title with %s

         **Example:** ::

            label = Section <b>%s</b>

   Default


.. container:: table-row

   Property
         allow

   Data type
         string

   Description
         Define which functions are accessible. Further this list may be
         reduced, if the BE\_USER does not have permission to perform the
         action

         Values should be listed separated by comma. This is the options you
         can choose between:

         toolbar,edit,new,delete,move,hide

         (toolbar is a general list of icons regarding the page, so use this
         for page records only)

   Default


.. container:: table-row

   Property
         newRecordFromTable

   Data type
         string

   Description
         Will display a panel for creation of new element (in the top of list)
         on the page from that table.

   Default


.. container:: table-row

   Property
         newRecordInPid

   Data type
         int

   Description
         Define a page ID where new records (except new pages) will be created.

   Default


.. container:: table-row

   Property
         line

   Data type
         boolean / int

   Description
         If set, a black line will appear after the panel. This value will
         indicate the distance from the black line to the panel

   Default


.. container:: table-row

   Property
         edit.displayRecord

   Data type
         boolean

   Description
         If set, then the record edited is displayed above the editing form.

   Default


.. container:: table-row

   Property
         onlyCurrentPid

   Data type
         boolean

   Description
         If set, only records with a pid matching the current id (TSFE->id)
         will be shown with the panel.

   Default


.. container:: table-row

   Property
         innerWrap

   Data type
         wrap /stdWrap

   Description
         Wraps the edit panel

   Default


.. container:: table-row

   Property
         outerWrap

   Data type
         wrap /stdWrap

   Description
         Wraps the whole edit panel including the black line (if configured)

   Default


.. container:: table-row

   Property
         printBeforeContent

   Data type
         boolean

   Description
         Normally the edit panel is displayed below the content element it
         belongs to. If this option is set, the panel is printed in front of
         the according element.

         **Example:** ::

            tt_content.stdWrap.editPanel.
            printBeforeContent = 1

         This displays the edit panels in front of the according elements, if
         you use css\_styled\_content.

   Default
         0


.. container:: table-row

   Property
         previewBorder

   Data type
         boolean / int

   Description
         If set, the hidden/starttime/endtime/fe\_user elements which are
         previewed will have a border around.

         The integer value denotes the thickness of the border

   Default


.. container:: table-row

   Property
         previewBorder.innerWrap

         previewBorder.outerWrap

         previewBorder.color

   Data type
         wrap / HTML color

   Description
         **innerWrap** wraps the content elements (including the icons) inside
         the preview border (an HTML table).

         **outerWrap** wraps the whole content element including the border.

         **color** denotes the color of the border.

   Default


.. container:: table-row

   Property
         stdWrap

   Data type
         ->stdWrap

   Description


   Default


.. ###### END~OF~TABLE ######

[tsref:(cObject).EDITPANEL]
