Module superlinked.framework.dsl.executor.executor
==================================================

Classes
-------

`App(executor: ExecutorT, entity_store: EntityStore, object_store: ObjectStore)`
:   Abstract base class for an App, a running executor that can for example do queries or ingest data.
    
    Initialize the App.
    
    Args:
        executor (TExecutor): The executor instance.
        entity_store (EntityStore): The entity store instance.
        object_store (ObjectStore): The object store instance.

    ### Ancestors (in MRO)

    * abc.ABC
    * typing.Generic

    ### Descendants

    * superlinked.framework.dsl.executor.in_memory.in_memory_executor.InMemoryApp
    * superlinked.framework.dsl.executor.rest.rest_executor.RestApp

    ### Instance variables

    `entity_store_manager: superlinked.framework.storage.entity_store_manager.EntityStoreManager`
    :   Get the entity store manager.
        
        Returns:
            EntityStoreManager: The entity store manager instance.

    `executor: ~ExecutorT`
    :   Get the executor.
        
        Returns:
            ExecutorT: The executor instance.

    `object_store_manager: superlinked.framework.storage.object_store_manager.ObjectStoreManager`
    :   Get the object store manager.
        
        Returns:
            ObjectStoreManager: The object store manager instance.

`Executor(sources: Sequence[SourceT], indices: Sequence[Index], context: ExecutionContext)`
:   Abstract base class for an executor.
    
    Initialize the Executor.
    
    Args:
        sources (list[SourceT]): The list of sources.
        indices (list[Index]): The list of indices.
        context (Mapping[str, Mapping[str, Any]]): The context mapping.

    ### Ancestors (in MRO)

    * abc.ABC
    * typing.Generic

    ### Descendants

    * superlinked.framework.dsl.executor.in_memory.in_memory_executor.InMemoryExecutor
    * superlinked.framework.dsl.executor.rest.rest_executor.RestExecutor

    ### Instance variables

    `context: superlinked.framework.common.dag.context.ExecutionContext`
    :   Get the context.
        
        Returns:
            Mapping[str, Mapping[str, Any]]: The context mapping.

    ### Methods

    `run(self) ‑> superlinked.framework.dsl.executor.executor.App[typing_extensions.Self]`
    :   Abstract method to run the executor.
        
        Returns:
            App[Self]: An instance of App.