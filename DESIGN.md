# Guiding Principles
- Srict Type-Safety
- Modularity
- Interoperability
- First-class Linux Support
- User-Friendliness

# Roadmap
1. Pre-Development
    - Outline project requirements
        * Outline GIS architecture
    - Determine vision and mission
    - Establish a clear direction
    - Publish a document style guide
    - Publish a coding style guide
    - Answer basic questions (FAQ)
2. Early Development Libraries (Alpha)
    - Write instructions for building and using PureGIS libraries.
    - Lay the groundwork for implementation of GIS concepts.
    - Define core types, including geometries.
    - Integrate georeferencing with Coordinate Reference Systems, Geographic Coordinate Systems, and Datums.
    - Define a sample of Mercator (cylindrical), conic, and azimuth projections.
    - Design a reprojection tool.
    - Implement a minimum set of I/O standards from those set by the Open Geospatial Consortium (OGC).
        1. First priority is GeoJSON
        2. Then, possibly GeoPackage or Shapefiles
    - Program a basic analysis toolset, focusing on returning computations of measurements.
    - Work on simple tests of accuracy to identify errors in georeferencing, projection, or computation.
        * Compare results to other GIS tools' results using statistical analysis such as root mean square error.
    - Start working on a functional data pipeline, implementing more composable functions.
    - Design a rudimentary mapping and visualization module that is capable of rendering a set of georeferenced points, lines, or polygons and exporting to a visual file format, such as PDF.
    - Begin to use CI/CD and prepare for changing priorities as the initial project roadmap starts to show signs of weakness.
    - Begin abstraction of library utilities for a command line interface.
3. Extended I/O and Data Engineering (Beta)
    - Milestone goals:
        * Tabular Data I/O
        * A set of spatial interaction tools (Buffer, Union, Clip, Erase, etc.)
        * Command-line Interface (CLI)
    - Evaluate project dependencies and FFI bindings
        * Determine whether hgdal would be a justified project requirement.
    - Establish CONTRIBUTING guidelines.
    - Expand geospatial types to include raster and multi-feature geometries.
    - Continuously integrate additional coordinate systems and utilities.
    - Prioritize improving computations, especially focusing on concurrence in Haskell.
    - Focus on implementing simpler GDAL operations, progressing to more complex problems.
    - If using hgdal or FFI bindings, phase out redundant operations in favor of Haskell implementations.
    - Always review input/output streams, focusing on data pipelines.
    - Maintain modularity of utilities, ensuring a well-defined I/O for each.
    - Ensure high-level utilities can be used in CLI program.
    - Implement first non-Haskell code for use with Qt.
4. A functional Haskell-based GIS (Release 1)
    - Support a handful of REST APIs for basemaps and data acquisition
    - Supports a multi-use interface:
        * Haskell Libraries
        * Command-line Interface
        * Graphical User Interface
    - Each use case is a modular integration of a subset of GIS components
        * Libraries remain separate by domain and function
        * CLI has access to utilities from installed packages
        * GUI likewise; UI is composed of a modular layout and atomic elements making use of QML for configuration.
    - Features a toolset of fundamental GIS utilities that could be used throughout a GIS Fundamentals course.
    - Work with multidimensional features.
    - A long release cycle that continuously works on these objectives:
        * Foster a team of contributors.
        * Focus on incorporating an increasing number of open standards.
        * Research and develop novel GIS applications.
        * Integrate horizontally.
            - Provide utility for existing GIS users through unique solutions and plugins.
            - Step into other GIS ecosystems with a heavy focus on API integration.
5. Future releases may seek to
    - Fill gaps in desktop GIS ecosystems
    - Shrink gaps between ecosystems
    - Implement complete GIS components
        * Cross-platform support
        * WebGIS
        * Reduce the barrier to hosting geographic data
    - ~~Embrace, Extend, Extinguish~~
    - Reduce vendor lock-in
​
