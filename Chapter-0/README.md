# Chapter 0: Introduction

- When deciding where to put a piece of code, we like to follow the “Fat Models, Utility Modules,
  Thin Views, Stupid Templates” approach.
  We recommend that you err on the side of putting more logic into anything but views and templates.
  The results are pleasing. The code becomes clearer, more self-documenting, less duplicated, and a lot
  more reusable. As for template tags and filters, they should contain the least amount of logic possible
  to function.
