Virtual Field Descriptions
==========================

Some fields including in the various Mappers don't rely on any actual field in
the Model (e.g., ``ListMapper::NAME_ACTIONS`` or ``ListMapper::NAME_BATCH``).

In order to prevent any side-effects when trying to retrieve the value of this
field (which doesn't exist), the option ``virtual_field`` is specified for these
fields.

When the template is instantiated, or whenever the value of the field is
required, ``null`` will be returned without prying on the Model itself.
