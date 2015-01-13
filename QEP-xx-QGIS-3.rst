.. _qep#[.#]:

========================================================================
QGIS Enhancement #: QGIS Major Version Increment
========================================================================

:Date: 2015/01/13
:Author: Matthias Kuhn
:Contact: matthias at opengis dot ch
:Author: Denis Rouzaud
:Contact: denis dot rouzaud at gmail dot com
:Last Edited: 2015/01/13
:Status:  Draft
:Version: QGIS X+1

.. note::

    See :ref:`QEP 1 <qep1>` for description of QEP process.

#. Summary
----------

This QEP describes the process of a major version increment in QGIS.

#. Reasoning
-------------

The QGIS major version is increased to allow breaking the API.
This has the effect of requiring a considerable amount of plugins to be
updated and obsoleting education material (digital and print).
Some changes require a major version increment because they require to
restructure the API in a way where it is not possible to provide a legacy layer
on top of the old API to maintain backwards compatibility.

Such a process may be driven by internal changes (a previous example is
multithreaded rendering or currently QEP#7 Rename Composer) or by external
dependencies (most notably python related parts like python itself or PyQt).

#. Timeline
-----------

Instead of the normal 3 months implementation and 1 month feature-freeze
period, an additional 2 months of implementation time and an additional 1 month
of feature-freeze/bug-fixing time should be given in order to have enough
time to implement everything that is required and to carefuly check that the
big changes confirm to the expected quality standards.

Two weeks before the feature freeze, an extension of the period should be
reconsidered. If must-have features that will require yet another major version
increment have not been implemented the implementation period should be
extended in order to include this change in the current release.

The first release of the subsequent versoin (X.2) shall be done after 2 months
in order to revert to the previous release dates and to quickly have a new
version available that irons out any bigger issues introduced and discovered
soon after release.

This period is not carved into stone and should be adapted to the amount of
work that is required for a certain release.

#. Additional Cleanup
-------------------------

Throughout the previous version of QGIS certain code pieces have been marked
with deprecated or been annotated with what is going to happen to them with the
next major release.

Anything deprecated shall be removed.

Anything scheduled for the next major release shall be changed.

#.# Python Bindings
...................

Deprecated python bindings should be removed.

#. Further Considerations/Improvements
--------------------------------------

A major version change is being communicated more than a regular release. It
should therefore be considered if the project can take additional advantages
from this process.

It can be a good possibility to launch corporate identity projects like a new
logo, webpage, t-shirts, documentation...

#. Backwards Compatibility
--------------------------

When a major version increment is done, backwards compatibility is of minor
interest.

While it is also desirable to avoid unnecessary breaks with previous versions
in terms of API and user interface, changes should be grouped as much as
possible. Any change that is going to happen in middle-term, is going to change
QGIS API or interface-wise in a major way and where there is no strong reason
against doing it now should be included. Postponing such a change leads to the
need for yet another major version increment sooner and for the sake of users,
authors and developers, such changes should happen as rarely as possible.

#. Issue Tracking ID(s)
-----------------------

(required)

#. Voting History
-----------------

(required)
