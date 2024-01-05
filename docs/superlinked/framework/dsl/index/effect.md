Module superlinked.framework.dsl.index.effect
=============================================

Classes
-------

`Effect(space: superlinked.framework.dsl.space.space.Space, affected_schema_reference: superlinked.framework.common.schema.schema_reference.SchemaReference, affecting_schema_reference: superlinked.framework.common.schema.schema_reference.SchemaReference | superlinked.framework.common.schema.schema_reference.MultipliedSchemaReference, filter_: superlinked.framework.common.interface.comparison_operand.ComparisonOperation[superlinked.framework.common.schema.schema_object.SchemaField])`
:   An effect represents a conditional interaction within a `Space` where the
    `affecting_schema_reference` interacted with the `affected_schema_reference`.
    
    It allows you to real-time adjust embeddings based on interaction.
    e.g.: A `User` schema interacts with a `Post` schema, if `event.type == 'like'.

    ### Class variables

    `affected_schema_reference: superlinked.framework.common.schema.schema_reference.SchemaReference`
    :

    `affecting_schema_reference: superlinked.framework.common.schema.schema_reference.SchemaReference | superlinked.framework.common.schema.schema_reference.MultipliedSchemaReference`
    :

    `filter_: superlinked.framework.common.interface.comparison_operand.ComparisonOperation[superlinked.framework.common.schema.schema_object.SchemaField]`
    :

    `space: superlinked.framework.dsl.space.space.Space`
    :