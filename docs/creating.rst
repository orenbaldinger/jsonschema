.. currentmodule:: jsonschemanlplab.validators

.. _creating-validators:

=======================================
Creating or Extending Validator Classes
=======================================

.. autofunction:: create

.. autofunction:: extend

.. autofunction:: validator_for

.. autofunction:: validates


Creating Validation Errors
--------------------------

Any validating function that validates against a subschema should call
``descend``, rather than ``iter_errors``. If it recurses into the
instance, or schema, it should pass one or both of the ``path`` or
``schema_path`` arguments to ``descend`` in order to properly maintain
where in the instance or schema respectively the error occurred.
