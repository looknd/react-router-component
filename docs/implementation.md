# Implementation notes

## Routing environments

         +---------------+
         |               |
         |  Environment  +---+
         |               |   |
         +---------------+   | notify
             ^               |
             |               v
    navigate |    +--------------+
             |    |              |+
             +----+    Router    ||+
                  |              |||
                  +--------------+||
                   +--------------+|
                    +--------------+

## Routing context

   +-------------------------------------------------------------------+
   | Global routing context (created by environment)                   |
   |-------------------------------------------------------------------|
   |                                                                   |
   |   +-------------------------------------------+  +------------+   |
   |   | Routing context created by router         |  |    Link    |   |
   |   |-------------------------------------------|  +------------+   |
   |   |                                           |  +------------+   |
   |   |   +------------+                          |  |    Link    |   |
   |   |   |    Link    |                          |  +------------+   |
   |   |   +------------+                          |  +------------+   |
   |   |   +------------+                          |  |    Link    |   |
   |   |   |    Link    |                          |  +------------+   |
   |   |   +------------+                          |  ...              |
   |   |   +------------+                          |                   |
   |   |   |    Link    |                          |                   |
   |   |   +------------+                          |                   |
   |   |   ...                                     |                   |
   |   |                                           |                   |
   |   +-------------------------------------------+                   |
   |                                                                   |
   +-------------------------------------------------------------------+