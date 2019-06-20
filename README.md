# hibernateAnnotations
@AccessType
The @AccessType annotation is deprecated. You should use either the JPA @Access or the Hibernate native @AttributeAccessor annotation.

@Any
The @Any annotation is used to define the any-to-one association, which can point to one of several entity types.

@AnyMetaDef
The @AnyMetaDef annotation is used to provide metadata about an @Any or @ManyToAny mapping.

@AnyMetaDefs
The @AnyMetaDefs annotation is used to group multiple @AnyMetaDef annotations.

@AttributeAccessor
The @AttributeAccessor annotation is used to specify a custom PropertyAccessStrategy. This should only be used to name a custom PropertyAccessStrategy. For property/field access type, the JPA@Access annotation should be preferred.

@BatchSize
The @BatchSize annotation is used to specify the size for batch loading the entries of a lazy collection.

@Cache
The @Cache annotation is used to specify the CacheConcurrencyStrategy of a root entity or a collection.

@Cascade
The @Cascade annotation is used to apply the Hibernate specific CascadeType strategies (e.g. CascadeType.LOCK, CascadeType.SAVE_UPDATE, CascadeType.REPLICATE) on a given association.

For JPA cascading, I prefer using the javax.persistence.CascadeType instead. When combining both JPA and Hibernate CascadeType strategies, Hibernate will merge both sets of cascades.


@Check
The @Check annotation is used to specify an arbitrary SQL CHECK constraint which can be defined at the class level.

@CollectionId
The @CollectionId annotation is used to specify an identifier column for an idbag collection.
You might want to use the JPA@OrderColumn instead.

@CollectionType
The @CollectionType annotation is used to specify a custom collection type.

The collection can also name a @Type, which defines the Hibernate Type of the collection elements.

@ColumnDefault
The @ColumnDefault annotation is used to specify the DEFAULT DDL value to apply when using the automated schema generator.
The same behavior can be achieved using the definition attribute of the JPA @Column annotation.


@Columns
The @Columns annotation is used to group multiple JPA @Column annotations.


@ColumnTransformer
The @ColumnTransformer annotation is used to customize how a given column value is read from or write into the database.


@ColumnTransformers
The @ColumnTransformers annotation is used to group multiple @ColumnTransformer annotations.

@CreationTimestamp
The @CreationTimestamp annotation is used to specify that the currently annotated temporal type must be initialized with the current JVM timestamp value.


@DiscriminatorFormula
The @DiscriminatorFormula annotation is used to specify a Hibernate @Formula to resolve the inheritance discriminator value.


@DiscriminatorOptions
The @DiscriminatorOptions annotation is used to provide the force and insert Discriminator properties.


@DynamicInsert
The @DynamicInsert annotation is used to specify that the INSERT SQL statement should be generated whenever an entity is to be persisted.

By default, Hibernate uses a cached INSERT statement that sets all table columns. When the entity is annotated with the @DynamicInsert annotation, the PreparedStatement is going to include only the non-null columns.


@DynamicUpdate
The @DynamicUpdate annotation is used to specify that the UPDATE SQL statement should be generated whenever an entity is modified.

By default, Hibernate uses a cached UPDATE statement that sets all table columns. When the entity is annotated with the @DynamicUpdate annotation, the PreparedStatement is going to include only the columns whose values have been changed.


@Entity
The @Entity annotation is deprecated. Use the JPA @Entity annotation instead.

@Fetch
The @Fetch annotation is used to specify the Hibernate specific FetchMode (e.g. JOIN, SELECT, SUBSELECT) used for the currently annotated association:

Read more about this annotation at @Fetch mapping official documentation.

@FetchProfile
The @FetchProfile annotation is used to specify a custom fetching profile, similar to a JPA Entity Graph.


@FetchProfile.FetchOverride
The @FetchProfile.FetchOverride annotation is used in conjunction with the @FetchProfile annotation, and it's used for overriding the fetching strategy of a particular entity association.


@FetchProfiles
The @FetchProfiles annotation is used to group multiple @FetchProfile annotations.

@Filter
The @Filter annotation is used to add filters to an entity or the target entity of a collection.


@FilterDef
The @FilterDef annotation is used to specify a @Filter definition (name, default condition and parameter types, if any).


@FilterDefs
The @FilterDefs annotation is used to group multiple @FilterDef annotations.

@FilterJoinTable
The @FilterJoinTable annotation is used to add @Filter capabilities to a join table collection.


@FilterJoinTables
The @FilterJoinTables annotation is used to group multiple @FilterJoinTable annotations.

@Filters
The @Filters annotation is used to group multiple @Filter annotations.

@ForeignKey
The @ForeignKey annotation is deprecated. Use the JPA 2.1 @ForeignKey annotation instead.

@Formula
The @Formula annotation is used to specify an SQL fragment that is executed in order to populate a given entity attribute.


@Generated
The @Generated annotation is used to specify that the currently annotated entity attribute is generated by the database.


@GeneratorType
The @GeneratorType annotation is used to provide a ValueGenerator and a GenerationTime for the currently annotated generated attribute.


@GenericGenerator
The @GenericGenerator annotation can be used to configure any Hibernate identifier generator.


@GenericGenerators
The @GenericGenerators annotation is used to group multiple @GenericGenerator annotations.

@Immutable
The@Immutable annotation is used to specify that the annotated entity, attribute, or collection is immutable.

Read more about this annotation at @Immutable mapping official documentation. 

@Index
The @Index annotation is deprecated. Use the JPA @Index annotation instead.

@IndexColumn
The @IndexColumn annotation is deprecated. Use the JPA @OrderColumn annotation instead.

@JoinColumnOrFormula
The @JoinColumnOrFormula annotation is used to specify that the entity association is resolved either through a FOREIGN KEY join (e.g. @JoinColumn) or using the result of a given SQL formula (e.g. @JoinFormula).

@JoinColumnsOrFormulas
The @JoinColumnsOrFormulas annotation is used to group multiple @JoinColumnOrFormula annotations.

@JoinFormula
The @JoinFormula annotation is used as a replacement for @JoinColumn when the association does not have a dedicated FOREIGN KEY column.

@LazyCollection
The @LazyCollection annotation is used to specify the lazy fetching behavior of a given collection.

The TRUE and FALSE values are deprecated since you should be using the JPA FetchType attribute of the @ElementCollection, @OneToMany, or @ManyToMany collection.

@LazyGroup
The @LazyGroup annotation is used to specify that an entity attribute should be fetched along with all the other attributes belonging to the same group.

To load entity attributes lazily, bytecode enhancement is needed. By default, all non-collection attributes are loaded in one group named "DEFAULT."

This annotation allows defining different groups of attributes to be initialized together when access one attribute in the group.

Read more about this annotation at @LazyGroup mapping official documentation.

@LazyToOne
The @LazyToOne annotation is used to specify the laziness options, represented by LazyToOneOption, available for a @OneToOne or @ManyToOne association.

@ListIndexBase
The @ListIndexBase annotation is used to specify the start value for a list index, as stored in the database.

By default, List indexes are stored starting at zero. This is generally used in conjunction with @OrderColumn.

@Loader
The @Loader annotation is used to override the default SELECT query used for loading an entity loading.

Read more about this annotation at Custom CRUD mapping official documentation. 

@ManyToAny
The @ManyToAny annotation is used to specify a many-to-one association when the target type is dynamically resolved.

@MapKeyType
The @MapKeyType annotation is used to specify the map key type.

@MetaValue
The @MetaValue annotation is used by the @AnyMetaDef annotation to specify the association between a given discriminator value and an entity type.

@NamedNativeQueries
The @NamedNativeQuery annotation extends the JPA @NamedNativeQuery with Hibernate specific features.

Read more about this annotation at Hibernate @NamedNativeQuery section for more info.

@NamedQueries
The @NamedQueries annotation is used to group multiple @NamedQuery annotations.

@NamedQuery
The @NamedQuery annotation extends the JPA @NamedQuery with Hibernate specific features.

Read more about this annotation at @NamedQuery  official documentation.

@Nationalized
The @Nationalized annotation is used to specify that the currently annotated attribute is a character type (e.g. String, Character, Clob) that is stored in a nationalized column type (NVARCHAR, NCHAR, NCLOB).

@NaturalId
The @NaturalId annotation is used to specify that the currently annotated attribute is part of the natural id of the entity.

@NaturalIdCache
The @NaturalIdCache annotation is used to specify that the natural id values associated with the annotated entity should be stored in the second-level cache.

@NotFound
The @NotFound annotation is used to specify the NotFoundAction strategy for when an element is not found in a given association.

Read more about this annotation at @NotFound mapping official documentation.

@OnDelete
The @OnDelete annotation is used to specify the delete strategy employed by the currently annotated collection, array, or joined subclasses. This annotation is used by the automated schema generation tool to generate the appropriate FOREIGN KEY DDL cascade directive.

Read more about this annotation at @OnDelete cascade official documentation.

@OptimisticLock
The @OptimisticLock annotation is used to specify if the currently annotated attribute will trigger an entity version increment upon being modified.

Read more about this annotation at Excluding attributes official documentation.

@OptimisticLocking
The @OptimisticLocking annotation is used to specify the currently annotated an entity optimistic locking strategy.

@OrderBy
The @OrderBy annotation is used to specify a SQL ordering directive for sorting the currently annotated collection.

It differs from the JPA @OrderBy annotation because the JPA annotation expects a JPQL order-by fragment, not an SQL directive.

@ParamDef
The @ParamDef annotation is used in conjunction with @FilterDef so that the Hibernate Filter can be customized with runtime-provided parameter values.

@Parameter
The @Parameter annotation is a generic parameter (basically a key/value combination) used to parametrize other annotations, like @CollectionType, @GenericGenerator, @Type, and @TypeDef.

@Parent
The @Parent annotation is used to specify that the currently annotated embeddable attribute references back the owning entity.

Read more about this annotation at @Parent mapping official documentation.

@Persister
The @Persister annotation is used to specify a custom entity or collection persister.

For entities, the custom persister must implement the EntityPersister interface.

For collections, the custom persister must implement the CollectionPersister interface.

@Polymorphism
The @Polymorphism annotation is used to define the PolymorphismType Hibernate will apply to entity hierarchies.

@Proxy
The @Proxy annotation is used to specify a custom proxy implementation for the currently annotated entity.

Read more about this annotation at @Proxy mappingofficial documentation.

@RowId
The @RowId annotation is used to specify the database column used as a ROWID pseudocolumn. For instance, Oracle defines the ROWID pseudocolumn as something that provides the address of every table row.

@SelectBeforeUpdate
The @SelectBeforeUpdate annotation is used to specify that the currently annotated entity state be selected from the database when determining whether to perform an update when the detached entity is reattached.

@Sort
The @Sort annotation is deprecated. Use the Hibernate specific @SortComparator or @SortNatural annotations instead.

@SortComparator
The @SortComparator annotation is used to specify a Comparator for sorting the Set/Map in-memory.

@SortNatural
The @SortNatural annotation is used to specify that the Set/Map should be sorted using natural sorting.

@Source
The @Source annotation is used in conjunction with a @Version timestamp entity attribute indicating the SourceType of the timestamp value.

@SQLDelete
The @SQLDelete annotation is used to specify a custom SQL DELETE statement for the currently annotated entity or collection.

See the Custom CRUD mapping official documentation.

@SQLDeleteAll
The @SQLDeleteAll annotation is used to specify a custom SQL DELETE statement when removing all elements of the currently annotated collection.

Read more about this annotation at Custom CRUD mapping official documentation.

@SqlFragmentAlias
The @SqlFragmentAlias annotation is used to specify an alias for a Hibernate @Filter.

The alias (e.g. myAlias) can then be used in the @Filter condition clause using the {alias} (e.g. {myAlias}) placeholder.

@SQLInsert
The @SQLInsert annotation is used to specify a custom SQL INSERT statement for the currently annotated entity or collection.

@SQLUpdate
The @SQLUpdate annotation is used to specify a custom SQL UPDATE statement for the currently annotated entity or collection.

@Subselect
The @Subselect annotation is used to specify an immutable and read-only entity using a custom SQL SELECT statement.

@Synchronize
The @Synchronize annotation is usually used in conjunction with the @Subselect annotation to specify the list of database tables used by the @Subselect SQL query.

@Table
The @Table annotation is used to specify additional information to a JPA @Table annotation, like custom INSERT, UPDATE or DELETE statements or a specific FetchMode.

@Tables
The @Tables annotation is used to group multiple @Table annotations.

@Target
The @Target annotation is used to specify an explicit target implementation when the currently annotated association is using an interface type.

@Tuplizer
The @Tuplizer annotation is used to specify a custom tuplizer for the currently annotated entity or embeddable.

@Tuplizers
The @Tuplizers annotation is used to group multiple @Tuplizer annotations.

@Type
The @Type annotation is used to specify the Hibernate @Type used by the currently annotated basic attribute.

@TypeDef
The @TypeDef annotation is used to specify a @Type definition, which can later be reused for multiple basic attribute mappings.

@TypeDefs
The @TypeDefs annotation is used to group multiple @TypeDef annotations.

@UpdateTimestamp
The @UpdateTimestamp annotation is used to specify that the currently annotated timestamp attribute should be updated with the current JVM timestamp whenever the owning entity gets modified.

@ValueGenerationType
The @ValueGenerationType annotation is used to specify that the current annotation type should be used as a generator annotation type.

@Where
The @Where annotation is used to specify a custom SQL WHERE clause used when fetching an entity or a collection.

@WhereJoinTable
The @WhereJoinTable annotation is used to specify a custom SQL WHERE clause used when fetching a join collection table.
