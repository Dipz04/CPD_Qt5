# CPD_Qt5
Proposal for implementing CPD on Qt5.

Problem- 
The Qt5 Print Support framework should be updated with the CPD support. The goal is to provide the CPD GUI features and D-bus communications with the CPD backend support for printing from Qt5 applications on support platforms.

Proposed Solution Pathway-
To make the Qt5 support framework backend which will connect to the CPD dialog instead of the QPrintDialog using a D-Bus connector.
The implementation will be within the QPrintDialog where the selection of the CPD happens at build time for (.pro/.pri) files by the package maintainers itself.
For example - the cpdb-libs support is only enabled with QT_CONFIG(cups).
We may add another option, QT_CONFIG(cupscpdwidgets), for building time support. 
