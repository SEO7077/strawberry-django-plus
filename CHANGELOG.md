# Changelog

## [1.0.0](https://github.com/STAR7077/strawberry-django-plus/compare/v0.1.0...v1.0.0) (2025-04-14)


### ⚠ BREAKING CHANGES

* remove debug toolbar integration
* migrate relay to strawberry's implementation ([#235](https://github.com/STAR7077/strawberry-django-plus/issues/235))
* **relay:** use Connection class from the field annotation and also allow a Connection to be returned by the base_resolver
* Do not make total_count mandatory anymore
* Use print_schema from strawberry as it can now print schema directives correctly
* Fix schema directive usage after latest changes from strawberry
* Remove monkey patches from django debug toolbar as it was released in its latest version

### Features

* add description to enums from django choices ([#217](https://github.com/STAR7077/strawberry-django-plus/issues/217)) ([be53c08](https://github.com/STAR7077/strawberry-django-plus/commit/be53c0811a6c85859e0640a25cc009de4fcee696))
* add semgrep to pre-commit-hooks ([b9e7a8d](https://github.com/STAR7077/strawberry-django-plus/commit/b9e7a8d4b3c46473e4f5401d538e7706d62e69e7))
* Add support for newest way of declaring info for resolvers in strawberry 0.115.0 ([dbfdf87](https://github.com/STAR7077/strawberry-django-plus/commit/dbfdf877445a4350a687eb47337ac9267b80da7b))
* add support for passing graphql_type to Field instances ([55a906e](https://github.com/STAR7077/strawberry-django-plus/commit/55a906e99c0fffe5d5c5643bd676eee472df78e7))
* add support for resolving `auto` fields for properties and cached_properties ([7b2ab43](https://github.com/STAR7077/strawberry-django-plus/commit/7b2ab43cffe7b852a4b805f65632192074c656ed)), closes [#198](https://github.com/STAR7077/strawberry-django-plus/issues/198)
* Add support for running debug_toolbar with ASGI ([8468c6f](https://github.com/STAR7077/strawberry-django-plus/commit/8468c6fec40cef61fc33d413b74eca77b117c002))
* Add support for strawberry-django-graphql &gt;= 0.4 ([de9a031](https://github.com/STAR7077/strawberry-django-plus/commit/de9a031d907a7570d44d59e81fd1a81e944ef32e))
* Add support for strawberry-graphql-django 0.5 ([62c2995](https://github.com/STAR7077/strawberry-django-plus/commit/62c2995c5bf42ee6fda59ca32d1abd42e7bc2109))
* Add support to optimize GenericRelation fields ([40db760](https://github.com/STAR7077/strawberry-django-plus/commit/40db760f8fbbf4620c6e61d401f803b564c32d57))
* Allow to change Connection class for Nodes and Edge class for Connections ([1003702](https://github.com/STAR7077/strawberry-django-plus/commit/10037021218792fbafcda67b1ce470e159a0bf90))
* Allow to pass handle_django_errors=False to CRUD mutations ([a8fb3f6](https://github.com/STAR7077/strawberry-django-plus/commit/a8fb3f69bf86e1ab1686dd442aad5d03b86db598)), closes [#79](https://github.com/STAR7077/strawberry-django-plus/issues/79)
* Allow to specify optimizer params directly to django's type ([34c80b2](https://github.com/STAR7077/strawberry-django-plus/commit/34c80b23c985de9667eca681dc756fee0aa92bb9)), closes [#44](https://github.com/STAR7077/strawberry-django-plus/issues/44)
* Allow to use lambdas for Prefetch optimization ([45e5355](https://github.com/STAR7077/strawberry-django-plus/commit/45e53557419f0a9f480d56f9c94f4df2891d1445)), closes [#83](https://github.com/STAR7077/strawberry-django-plus/issues/83)
* Apply get_queryset when resolving Django relay.Node types ([c3468e4](https://github.com/STAR7077/strawberry-django-plus/commit/c3468e4ef3cf63f4278f6ce14c8b0746e28d563a))
* Customizable typename for Node; Fix: GlobalID parse_literal vars, UNSET as default_value ([477acdf](https://github.com/STAR7077/strawberry-django-plus/commit/477acdf922df3b0880c8504e241a9a36b468eff5))
* enum type for standard django choices ([c3d3a7e](https://github.com/STAR7077/strawberry-django-plus/commit/c3d3a7e995145d7034888b74ad66ca8076a208ef))
* expose `__version__` on the package ([5d2fe07](https://github.com/STAR7077/strawberry-django-plus/commit/5d2fe07e1551fc7b0aff7c8efacc49ffec075580))
* Expose mutation through gql.django.mutation ([a91c3fb](https://github.com/STAR7077/strawberry-django-plus/commit/a91c3fb096633d0ec00747cff7d28f709ba29f2a))
* Expose UNSET to gql so it can be used with gql.UNSET ([af18e41](https://github.com/STAR7077/strawberry-django-plus/commit/af18e41f5f2993c493f8fd6df9e1ec99bcbce716))
* Improve input mutations to better handle m2m with intermediate values ([53d479b](https://github.com/STAR7077/strawberry-django-plus/commit/53d479b903297bbf9cea9eae8ce2973fe2b7eb0b))
* Make defined types comparable and hashable ([3cd100d](https://github.com/STAR7077/strawberry-django-plus/commit/3cd100d89afc333db8da22dfd2df3e42fea407f3)), closes [#158](https://github.com/STAR7077/strawberry-django-plus/issues/158)
* mark this lib as deprecated and add a documentation on how to migrate to strawberry_django ([472f2a2](https://github.com/STAR7077/strawberry-django-plus/commit/472f2a2723607379bab88999adbf29e166ad48b2))
* new GlobalID.aresolve_node to help resolving asynchronous nodes ([9d34f1a](https://github.com/STAR7077/strawberry-django-plus/commit/9d34f1a09ce284ab2380bf44307e375617df0277))
* New mutation that acts like input_mutation, but without converting arguments to an input type ([94805ca](https://github.com/STAR7077/strawberry-django-plus/commit/94805cafe878c2f5bc94c9e729f55d19b2f6dbe9))
* Optimize fields that return an interface (e.g. relay.Node) ([6ec51ce](https://github.com/STAR7077/strawberry-django-plus/commit/6ec51cefebe07a8f94f473c913732b6362297046)), closes [#28](https://github.com/STAR7077/strawberry-django-plus/issues/28)
* Optimize GenericForeignKey by prefetch_related them ([49a30f5](https://github.com/STAR7077/strawberry-django-plus/commit/49a30f5f00406483c1852e88030abd1822d0b7d3))
* **optimizer:** support custom QS for prefetches ([7bc6c30](https://github.com/STAR7077/strawberry-django-plus/commit/7bc6c30f9de1d22cb23bc1bb217b73cedaaf3d74))
* remove debug toolbar integration ([d445154](https://github.com/STAR7077/strawberry-django-plus/commit/d44515441a638331c37c9908fd7fbf8ccb18598e))
* Separate the logic for generating the Q filter for filter_for_user function so that it can be reused elsewhere ([c77014b](https://github.com/STAR7077/strawberry-django-plus/commit/c77014bbcbf107bc6052213684b248ace0e21e0d))
* start testing on Django 4.2 ([c277162](https://github.com/STAR7077/strawberry-django-plus/commit/c27716258bbbdcccdfc5548c9680a1f9d4ff65ce))
* Support field metadata from upstream strawberry ([a49d6f5](https://github.com/STAR7077/strawberry-django-plus/commit/a49d6f5c571b18cf741b1155e3fab602265a9256))
* Support for django 4.1 ([4656403](https://github.com/STAR7077/strawberry-django-plus/commit/4656403b10326bf60f9e7b0bc1626c4145b7dd75))
* Support full_clean when directly invoking resolver ([5e05a20](https://github.com/STAR7077/strawberry-django-plus/commit/5e05a202fd93be4687698d2865b703e92f14f02a))
* Support mutation resolvers that return unions ([4847059](https://github.com/STAR7077/strawberry-django-plus/commit/4847059a246555dc03bc835341405dff95c66800))
* Support nested foreignkey creation for mutations ([a9fe762](https://github.com/STAR7077/strawberry-django-plus/commit/a9fe76206515ec53c7cbcc8ce17c4e6230294b58)), closes [#82](https://github.com/STAR7077/strawberry-django-plus/issues/82)
* Support only/select_related hints for many relations ([5a6ae3f](https://github.com/STAR7077/strawberry-django-plus/commit/5a6ae3fc77b7de7d83f5298d869c683eb00c390b))
* Support strawberry 0.109+ ([395547a](https://github.com/STAR7077/strawberry-django-plus/commit/395547ac2769b422871043aaf3ad39904146f3a8)), closes [#40](https://github.com/STAR7077/strawberry-django-plus/issues/40)
* Support Strawberry 0.139 ([699c3f0](https://github.com/STAR7077/strawberry-django-plus/commit/699c3f0f9dff56424e575d55990d3c07129795ce)), closes [#142](https://github.com/STAR7077/strawberry-django-plus/issues/142)
* Support Unions for ensure_type in resolvers ([6c08d8f](https://github.com/STAR7077/strawberry-django-plus/commit/6c08d8f00fcdc39d2e0e714ce93e55f8da3d24f0))
* update dev requirements and enable more ruff rules ([301c475](https://github.com/STAR7077/strawberry-django-plus/commit/301c47589caba4556058ba4e7c49e0b4526d257c))
* use a type's get_queryset for Relay connections if it defines one ([#215](https://github.com/STAR7077/strawberry-django-plus/issues/215)) ([0b7c122](https://github.com/STAR7077/strawberry-django-plus/commit/0b7c1225b6f65c6ceb3a34328e88898110f0c951))
* Use the CONNECTION_CLASS defined on node when creating a connection field ([cd2926d](https://github.com/STAR7077/strawberry-django-plus/commit/cd2926dc6abfc139a98b6ce05da7bbed268e360d))


### Bug Fixes

* Abort only optimization when manually prefetching something ([758661e](https://github.com/STAR7077/strawberry-django-plus/commit/758661eebb311214878d13b62800de1eb04b2ab4))
* add settings to disable auto-enum generation + unique class name ([4343a72](https://github.com/STAR7077/strawberry-django-plus/commit/4343a723cc9a15db0b94ab9bf0a40aec1402ea17))
* allow `field_name` to be passed for node and connections ([7093e42](https://github.com/STAR7077/strawberry-django-plus/commit/7093e42e8188a658b49477d4439cce5054b21334))
* allow connections to be typed as unions ([9268869](https://github.com/STAR7077/strawberry-django-plus/commit/926886918d0c869fec9cd628938fea5a8f4cc95a)), closes [#223](https://github.com/STAR7077/strawberry-django-plus/issues/223)
* allow mutation full clean with kwargs ([341c4c6](https://github.com/STAR7077/strawberry-django-plus/commit/341c4c6a67215e4e232db4048266c7d6260c9bb0))
* allow update of nested input fields on foreign key relationships ([ad437cc](https://github.com/STAR7077/strawberry-django-plus/commit/ad437ccd39c5f203478cc0f81d8af14bb3567d86))
* also support `auto` when checking for auto annotations ([92dc46b](https://github.com/STAR7077/strawberry-django-plus/commit/92dc46bcd7fe0f7fedb7c21ae426811bb7e9fc8e))
* avoid "lookup was already seen with a different queryset" by merging existing prefetches together with hints ([2aced82](https://github.com/STAR7077/strawberry-django-plus/commit/2aced8201485c0ccc5dad71f5484f535ce6e62ae))
* Avoid AttributeError when retrieving django type's attributes at creation time ([0783742](https://github.com/STAR7077/strawberry-django-plus/commit/078374299fd0fd0643f85a50d77402da2a483b20)), closes [#58](https://github.com/STAR7077/strawberry-django-plus/issues/58)
* broken django-guardian link ([28c91a1](https://github.com/STAR7077/strawberry-django-plus/commit/28c91a19233e59772b77333e5652c1d510408eed))
* build won't break when a generic relation is used ([28c5ea2](https://github.com/STAR7077/strawberry-django-plus/commit/28c5ea23598d73a1002765633f56868140e8a44c))
* Cast object_pk to model pk type ([c793cf1](https://github.com/STAR7077/strawberry-django-plus/commit/c793cf1a5cbb2181c477fac59934387b7246846f))
* Check for Awaitable the correct way ([e663f95](https://github.com/STAR7077/strawberry-django-plus/commit/e663f95a361f3079d896c8cae880570c93782af9))
* Check for coroutrine instead of awaitable ([62145e4](https://github.com/STAR7077/strawberry-django-plus/commit/62145e413a37f6d0158040762155ab4827b70ddb))
* Choices field must be installed in dev ([f7bf59a](https://github.com/STAR7077/strawberry-django-plus/commit/f7bf59a78a16c4d7df5966b4fb533cf0e4e8e224))
* correct when to use model_field.field ([cd68f99](https://github.com/STAR7077/strawberry-django-plus/commit/cd68f9910f546d4cbfcd7272707d36b8e8e27776))
* dataclass to typeddict ([f40490d](https://github.com/STAR7077/strawberry-django-plus/commit/f40490d36a2052ef008bf28e70bb415bd79113c8))
* De morgan law fix from last merged PR ([d7e98ee](https://github.com/STAR7077/strawberry-django-plus/commit/d7e98ee8dfea573350c4c8a607a163598ab4340a))
* delete instead of remove non-nullable foreign key set objects ([cf2344e](https://github.com/STAR7077/strawberry-django-plus/commit/cf2344ebc077ea7edf99e6e2b10b645d19b78d8a))
* django connection field remove kwargs not in default_args ([d197440](https://github.com/STAR7077/strawberry-django-plus/commit/d1974400a5e1f79c69446784f06927e1fd09ee3f))
* **django-relay:** fix filter/order not being applied to django relay connections ([5ed102d](https://github.com/STAR7077/strawberry-django-plus/commit/5ed102d307b2d2fc3a75a93ada8fbe4a2a6e633c)), closes [#170](https://github.com/STAR7077/strawberry-django-plus/issues/170)
* DjangoMutation should not receive an `input_type` ([7450e1e](https://github.com/STAR7077/strawberry-django-plus/commit/7450e1eab67a5619f40ebfe4ea279c45deccebfe)), closes [#80](https://github.com/STAR7077/strawberry-django-plus/issues/80)
* Do not check permissions for OperationInfo ([216e12b](https://github.com/STAR7077/strawberry-django-plus/commit/216e12be230c4001b2c3d104b11877a3dc02b975))
* Do not keep "is_type_of" from parents ([8b1ba26](https://github.com/STAR7077/strawberry-django-plus/commit/8b1ba261ab4eee9d6b5a1ecaab7bd97b443685ae))
* do not try to merge fragments, they have no name ([0dec3de](https://github.com/STAR7077/strawberry-django-plus/commit/0dec3debba7e29b52fb0cee4ab83e16174ad712d))
* Do not use Iterable/Mapping to avoid iterating over wrong types (e.g. strings) ([6db7f42](https://github.com/STAR7077/strawberry-django-plus/commit/6db7f423b982d0a01f0c946ae1c4020cd788d44c))
* don't make full_clean positional ([0925c86](https://github.com/STAR7077/strawberry-django-plus/commit/0925c86ee4feb3de13630874a4044afa8748a857))
* Fix `gql.django.connection` ignoring its source ([f60eb89](https://github.com/STAR7077/strawberry-django-plus/commit/f60eb892557dcb32d50c34204c5027eb4ead1c22))
* fix a nit in factory faker ([3edb8d9](https://github.com/STAR7077/strawberry-django-plus/commit/3edb8d96fe5b12c262087ac3ef9fce21ab115854))
* Fix a typing issue with the latest version of pyright ([f91adf3](https://github.com/STAR7077/strawberry-django-plus/commit/f91adf3332b59e647a84950f5f262f7737166c64))
* Fix a typo that was preventing Django types from defining their own resolve_connection if they wanted ([c7d7e36](https://github.com/STAR7077/strawberry-django-plus/commit/c7d7e364a73c23f7b29235992338676848e7ec71)), closes [#49](https://github.com/STAR7077/strawberry-django-plus/issues/49)
* fix a wrongly refactored code from previous commit ([5b7553c](https://github.com/STAR7077/strawberry-django-plus/commit/5b7553c05baf864a3a4f2965ca6fc6a444af487a))
* fix class inherited fields not being evaluated correctly ([2491cb3](https://github.com/STAR7077/strawberry-django-plus/commit/2491cb3cf086ced0a686eb4e742de30d5c9aa5fb)), closes [#247](https://github.com/STAR7077/strawberry-django-plus/issues/247)
* fix django versioning on test actions ([b313cd9](https://github.com/STAR7077/strawberry-django-plus/commit/b313cd9d33dffbb1e5f0ee0174b605f1cb898af6))
* fix edge case where pk is unset ([4fe52b5](https://github.com/STAR7077/strawberry-django-plus/commit/4fe52b59bccb13b1cf1c8a23798763cbe503b5d6))
* Fix filters breaking relay connections ([222231b](https://github.com/STAR7077/strawberry-django-plus/commit/222231b7f5662e586ca24fd35784e7407019100f)), closes [#47](https://github.com/STAR7077/strawberry-django-plus/issues/47)
* Fix github actions badge ([7a87d6c](https://github.com/STAR7077/strawberry-django-plus/commit/7a87d6c6739608181243e3b3865704f373db721e))
* Fix issues with python 3.9 and lower ([06bfe41](https://github.com/STAR7077/strawberry-django-plus/commit/06bfe41a4e38abf8e197c64c619847c9ed47060b))
* fix LICENSE author ([cdc9b56](https://github.com/STAR7077/strawberry-django-plus/commit/cdc9b56994454dd33af4d0d5fb9ab6373a6b50bc))
* fix missing checkout version ([2993223](https://github.com/STAR7077/strawberry-django-plus/commit/299322385cff41b3241cebe7688aa7e5a5b2d7f1))
* fix missing export of django_resolver ([bcea6a4](https://github.com/STAR7077/strawberry-django-plus/commit/bcea6a464f18a74241a2d0d736a0a9b8dfd3e70c))
* fix optimizer not working on some cases with fragment spreading ([4b3d18e](https://github.com/STAR7077/strawberry-django-plus/commit/4b3d18e3a425eb0fe817a6ccd87de329810b680a)), closes [#144](https://github.com/STAR7077/strawberry-django-plus/issues/144)
* Fix poetry.lock requirements ([ddf0b0b](https://github.com/STAR7077/strawberry-django-plus/commit/ddf0b0b386d3d48b6c7727ed8af9f70daac8004c))
* Fix possibly unbound values and other typing issues ([9fe1a75](https://github.com/STAR7077/strawberry-django-plus/commit/9fe1a756dff74e0f50c6e5cadd3f596f3c153d6e))
* Fix prefetch optimization ([e16ab9d](https://github.com/STAR7077/strawberry-django-plus/commit/e16ab9dd00df95a6c7f87a13b9a145856f03dcc6))
* Fix pyright issues ([ca0a6fc](https://github.com/STAR7077/strawberry-django-plus/commit/ca0a6fc91aa8f65ac1f156c30fc072a53b0314a5))
* fix relay connections not being optimized ([931a6ce](https://github.com/STAR7077/strawberry-django-plus/commit/931a6ce4d990ab188c727979dcce1d8addd1a2c8))
* Fix remaining issues with many to many inputs ([f909063](https://github.com/STAR7077/strawberry-django-plus/commit/f9090637e2388e98670ffffd0a51485e7dbfd365))
* Fix resolving issues with latest changes from strawberry-graphql ([03a7040](https://github.com/STAR7077/strawberry-django-plus/commit/03a7040e2c8f8e4c3b4c970e4ec058e39016e147))
* fix resolving model ids, implement suggested code improvements ([a23dfbf](https://github.com/STAR7077/strawberry-django-plus/commit/a23dfbfe70352e8f53cc6579993a908c405bd819))
* Fix schema printing tests ([5ec137c](https://github.com/STAR7077/strawberry-django-plus/commit/5ec137cf628a5d75512bf0ed0e05c1c8a63ba1a1))
* Fix strange mypy issue introduced in [#137](https://github.com/STAR7077/strawberry-django-plus/issues/137) ([3995e6c](https://github.com/STAR7077/strawberry-django-plus/commit/3995e6c877ec7645eed4f5f8396d425221f04f64)), closes [#145](https://github.com/STAR7077/strawberry-django-plus/issues/145)
* Fix support for the way strawberry checks for auto now ([daab754](https://github.com/STAR7077/strawberry-django-plus/commit/daab7542f35e3d52d1b9d0b88d8a78e036e618ce))
* fix typing for update/delete mutations ([73b4510](https://github.com/STAR7077/strawberry-django-plus/commit/73b451063aa0b57079d2bda86fe61f08448dcb2c))
* Fix typing issues found by latest pyright version ([c02fe9d](https://github.com/STAR7077/strawberry-django-plus/commit/c02fe9d54f328119a97be806ce3d927d227c555a))
* fixes NodeInput parsing to dict ([4fe52b5](https://github.com/STAR7077/strawberry-django-plus/commit/4fe52b59bccb13b1cf1c8a23798763cbe503b5d6))
* Force is_basic_field to return False to fix resolving issues with our custom fields ([27bacae](https://github.com/STAR7077/strawberry-django-plus/commit/27bacae58eb2a5bca6ee9a0ed30c064a6daaa067))
* GENERATE_ENUMS_FROM_CHOICES default to False ([dd5d7dc](https://github.com/STAR7077/strawberry-django-plus/commit/dd5d7dc857837ba309cb60bdc127fac01bcd0c9d))
* inject filters/order at once to avoid one of them missing also removing the other one ([9f4011f](https://github.com/STAR7077/strawberry-django-plus/commit/9f4011f5ad7481308ab20a6b2f28b16025d07ff5)), closes [#243](https://github.com/STAR7077/strawberry-django-plus/issues/243)
* Issue 33 ([6316f8e](https://github.com/STAR7077/strawberry-django-plus/commit/6316f8e4a744b7bda9c3b30eee4de844bea9ad75))
* Keep django_name when it is provided by the user ([1e5cdf8](https://github.com/STAR7077/strawberry-django-plus/commit/1e5cdf88ed392a325f4dd6d51599a192d45e820a))
* Limit relay split to 1 so that the key can contain ":" characters ([1bd0b95](https://github.com/STAR7077/strawberry-django-plus/commit/1bd0b957abaa416f9244b54e686b08e6266bc7ec))
* loosen errors for unions of django types when checking for filters/ordering ([694efa4](https://github.com/STAR7077/strawberry-django-plus/commit/694efa41727e945b8e8525d91c1fbccd056aebdf))
* Make djang-debug-toolbar really an optional dependency by adding it to extras ([2772b8b](https://github.com/STAR7077/strawberry-django-plus/commit/2772b8b1d0aa72d749677a3caaeb3ec43f3d59c9))
* Make relay's input types allow UNSET as the default value ([695610b](https://github.com/STAR7077/strawberry-django-plus/commit/695610b736897660918856a9ecf41d314b3da619))
* Make sure order gets added to the connection when defined on type ([e455054](https://github.com/STAR7077/strawberry-django-plus/commit/e455054c64806da9fffeb8a3b68d6025bf723c98))
* Make sure the class is the same when comparing to other objects ([67d9931](https://github.com/STAR7077/strawberry-django-plus/commit/67d99317f9cf519a4f1ebf97f0b5c0f46863c05d))
* make sure the correct node type is passed on inheritance with other types/interfaces implementing Node ([e03016f](https://github.com/STAR7077/strawberry-django-plus/commit/e03016f5f39e119fbd17283d3ff5746d2f9410bf))
* Make sure to keep original field annotations in the input type ([3cf9d86](https://github.com/STAR7077/strawberry-django-plus/commit/3cf9d8697d9541d179e818d6504ad81a10aee8f5))
* Make sure we keep extra types ordered in the printer ([7235475](https://github.com/STAR7077/strawberry-django-plus/commit/72354757209b6c3080bedd992b16b7a6e720be89))
* missing return for the async resolver ([9894ab8](https://github.com/STAR7077/strawberry-django-plus/commit/9894ab85e48c79f2bf6bff3e9afe699fa61dd6f0))
* **mutations:** ensure that pk is not added by the django base field in create/update/delete mutations ([ef94f9f](https://github.com/STAR7077/strawberry-django-plus/commit/ef94f9f933cbef3393843055bf9067ab395fd861)), closes [#165](https://github.com/STAR7077/strawberry-django-plus/issues/165)
* only format message with params if params is not empty ([ccf5bd5](https://github.com/STAR7077/strawberry-django-plus/commit/ccf5bd511c04cd33dd54a43d23596c8616df6bc2))
* Only map errors if the field is set to handle them ([c11a91c](https://github.com/STAR7077/strawberry-django-plus/commit/c11a91c5ed300dd3ab935ab5e6c3aecc5702c1fa)), closes [#79](https://github.com/STAR7077/strawberry-django-plus/issues/79)
* Only should only be aborted when the whole model is specified (i.e. as a string) ([3bbe8f2](https://github.com/STAR7077/strawberry-django-plus/commit/3bbe8f24b5e84d17929744a413229eaedb1a9f03))
* **optimizer:** avoid double add_prefix calls ([d503218](https://github.com/STAR7077/strawberry-django-plus/commit/d503218f2337809a4fdfacb0d17825c59e8659fe))
* pass headers further on TestClient ([f8a05e8](https://github.com/STAR7077/strawberry-django-plus/commit/f8a05e88ce309b2213171a8460b6f7aedc47763a)), closes [#224](https://github.com/STAR7077/strawberry-django-plus/issues/224)
* pass the correct model to many to many input items ([d22da73](https://github.com/STAR7077/strawberry-django-plus/commit/d22da7377721d5ef7f6d8d68307cc6abe9c1aa87))
* Prevent a circular import issue that might happen in some setups ([eb7392b](https://github.com/STAR7077/strawberry-django-plus/commit/eb7392b2e5569719539b61bfb125dcd49f1e692b))
* properly optimize nested fragments ([d9faa47](https://github.com/STAR7077/strawberry-django-plus/commit/d9faa47a7fa22a7c72fb5689933e87b7491ff224)), closes [#203](https://github.com/STAR7077/strawberry-django-plus/issues/203)
* pyright detected type issues ([e838473](https://github.com/STAR7077/strawberry-django-plus/commit/e8384731665131356f7ecbaaa655c72a9fa9bc40))
* pyright issue ([9a3257e](https://github.com/STAR7077/strawberry-django-plus/commit/9a3257e4f5e17a3d881e88ef8a70a73e62b3d14b))
* pyright tests should also not install debug-toolbar extras ([8edca6d](https://github.com/STAR7077/strawberry-django-plus/commit/8edca6d973b14ca8684e41fd4e42743281f88043))
* **pyright:** solve some issues from the newest pyright version ([df93ada](https://github.com/STAR7077/strawberry-django-plus/commit/df93adae97d31bf189dc79ce610e8a26d1334a0e))
* regenerate whole schema ([85996df](https://github.com/STAR7077/strawberry-django-plus/commit/85996df04686235fe809ba06586f670abf764cf3))
* **relay:** fix support for custom resolvers returning generators ([1aab2ac](https://github.com/STAR7077/strawberry-django-plus/commit/1aab2ac19790b8802c3b7acd5e50a24087eacb35))
* **relay:** use the type's defined resolve_id when it defines one ([710855e](https://github.com/STAR7077/strawberry-django-plus/commit/710855eb03049bc4f1c423af6681e9c6ce684a62))
* Remove print statement left behind ([dd0d71f](https://github.com/STAR7077/strawberry-django-plus/commit/dd0d71f91c29ab13692adbbe6c7158e41fb102f3))
* Resolve `LazyType` when retrieving the node type ([c01678f](https://github.com/STAR7077/strawberry-django-plus/commit/c01678ff0c7715d20dc23d458bd77a8f3ac17c68)), closes [#116](https://github.com/STAR7077/strawberry-django-plus/issues/116)
* run mkdocs with poetry ([92bd473](https://github.com/STAR7077/strawberry-django-plus/commit/92bd47372612dee218e7491129672c84beb6cdab))
* store auto enum in model field hidden attr to avoid duplication in schema ([e8a727c](https://github.com/STAR7077/strawberry-django-plus/commit/e8a727c6ec4cd5495ece4efb8b86b3e1b1013b2f))
* Strawberry 0.133.1+ expects the default factory to be MISSING instead of a lambda that returns UNSET ([b6fdd72](https://github.com/STAR7077/strawberry-django-plus/commit/b6fdd729adb67ffdf50cb645e84ae7a3f7140786))
* strawberry.ID cannot be used on isinstance ([9517fdd](https://github.com/STAR7077/strawberry-django-plus/commit/9517fdd024971681da90ab533ca079b3d7d67331))
* suffix name with Enum instead of AutoEnum ([368567e](https://github.com/STAR7077/strawberry-django-plus/commit/368567e6f8f7653a6517d8ac90acdc2744b254df))
* **type:** Typo in readme.md ([bb4b93d](https://github.com/STAR7077/strawberry-django-plus/commit/bb4b93d57ee9bf37588c5bd0ed12805ca112c9b3))
* typo in docs ([#261](https://github.com/STAR7077/strawberry-django-plus/issues/261)) ([ae625b2](https://github.com/STAR7077/strawberry-django-plus/commit/ae625b29203f39dc5e5192c9391a38a7a48e8be3))
* update build_filter_kwargs to handle Enums ([aec21ce](https://github.com/STAR7077/strawberry-django-plus/commit/aec21cefce3bc486c9dbd8268c57a1fa93b043de))
* update build_filter_kwargs to handle reverse lookups ([8c8c365](https://github.com/STAR7077/strawberry-django-plus/commit/8c8c365c80c755c0e2c0ffca40a20a20cdc288aa))
* WeakKeyDictionary is not subscriptable in python 3.8 ([8c18222](https://github.com/STAR7077/strawberry-django-plus/commit/8c182221d00e0b62109504e45bcc95126a7f3cfa))
* with dataclass validations ([d4b1b7a](https://github.com/STAR7077/strawberry-django-plus/commit/d4b1b7ac274aafb8b75b8f7c7e8ace1a2aea6b34))
* Workaround a pyright false positive ([3e3610f](https://github.com/STAR7077/strawberry-django-plus/commit/3e3610fc97f67d8fcc01d183c429cca16a6a7d58))
* Workaround adding order/filters in django connections in a thread-safe way ([27124bd](https://github.com/STAR7077/strawberry-django-plus/commit/27124bd2dcf02646ee2253de97aee320346eeaaf))


### Performance

* s/ignore/exclude/ for improved pyright performance ([e725b6b](https://github.com/STAR7077/strawberry-django-plus/commit/e725b6b1129e21fd40e2cf676da483df019bfb24))


### Documentation

* add a "Migration guide" section explaning how to migrate from v2 to v3 ([e9ffdf1](https://github.com/STAR7077/strawberry-django-plus/commit/e9ffdf11e2d9dc3a6a98bee4222a8d890027faa4))
* add a note regarding debug-toolbar integration removal ([59bae30](https://github.com/STAR7077/strawberry-django-plus/commit/59bae3019b0c5aa2704a069e3a4e456293dbe9b2))
* Break the docs line in the README ([873af98](https://github.com/STAR7077/strawberry-django-plus/commit/873af98592bda336995ae9d5cf132f1512cd0720))
* document id_attr ([2ce30c0](https://github.com/STAR7077/strawberry-django-plus/commit/2ce30c0d6d53da1cb6682dbf2ce6fdd8ff5be7d6))
* fix a typo in the CHANGELOG ([fedab8e](https://github.com/STAR7077/strawberry-django-plus/commit/fedab8e449d6a926f530e10543d149304c0a5f05))
* Fix a typo in the docs ([2b99571](https://github.com/STAR7077/strawberry-django-plus/commit/2b99571a0a6bbdf830ef617b281c25547c80fdab))
* fix album related name in docs ([#219](https://github.com/STAR7077/strawberry-django-plus/issues/219)) ([8bb4b6b](https://github.com/STAR7077/strawberry-django-plus/commit/8bb4b6b66b74ebdfa77ade6be9233d5ff9c07671))
* fixes 2 typos in docs ([#227](https://github.com/STAR7077/strawberry-django-plus/issues/227)) ([920f5fb](https://github.com/STAR7077/strawberry-django-plus/commit/920f5fbae8e7fe1d6cea9f6e012b0119b83ff5a2))
* Some improvements to docs ([459993e](https://github.com/STAR7077/strawberry-django-plus/commit/459993e0957ec9f9e8a3b0d5ca5906736435e496))
* Update link to mutations documentation ([3a3dc08](https://github.com/STAR7077/strawberry-django-plus/commit/3a3dc08aa1adea4acdefbd66a84021d651712f9d))


### Code Refactoring

* demo mutation cleaning ([8c9f599](https://github.com/STAR7077/strawberry-django-plus/commit/8c9f599d70e6a595a88d2e1696210095439d04a2))
* Disable only optimization on mutations and subscriptions ([dd38b6a](https://github.com/STAR7077/strawberry-django-plus/commit/dd38b6ac75d7a4d2bac84fe0abb74c99dc9ba748))
* Do not make total_count mandatory anymore ([c91bf5e](https://github.com/STAR7077/strawberry-django-plus/commit/c91bf5e669882b9e3079fe713eb8dafe02aab8e3))
* fix assertionerror when registering copied generic types on schema directives ([#238](https://github.com/STAR7077/strawberry-django-plus/issues/238)) ([d56fc20](https://github.com/STAR7077/strawberry-django-plus/commit/d56fc20858a2284ea7331826b2cb9c0e1cddbf76))
* fix lint issues ([2d78a9b](https://github.com/STAR7077/strawberry-django-plus/commit/2d78a9b836393bb70700cfc25166178d648400d9))
* Fix schema directive usage after latest changes from strawberry ([2589944](https://github.com/STAR7077/strawberry-django-plus/commit/2589944e987542c5a9f6dd2f890b1f5e8ac68e66))
* migrate relay to strawberry's implementation ([#235](https://github.com/STAR7077/strawberry-django-plus/issues/235)) ([d854547](https://github.com/STAR7077/strawberry-django-plus/commit/d85454733fe6580fc1f1f8224f0db1fd83a10072))
* **pyright:** fix pyright issues ([1aeae53](https://github.com/STAR7077/strawberry-django-plus/commit/1aeae539c7e6b783e01d19903fd1469de0f71292))
* **relay:** use Connection class from the field annotation and also allow a Connection to be returned by the base_resolver ([85c6b6c](https://github.com/STAR7077/strawberry-django-plus/commit/85c6b6ce276c08549de4cdedfe630f300dcac478))
* remove hard dependencies on contenttypes and auth framework ([#250](https://github.com/STAR7077/strawberry-django-plus/issues/250)) ([c3329de](https://github.com/STAR7077/strawberry-django-plus/commit/c3329de6e2720e26c1455d364626621d432dc710))
* remove model useless transaction and test ([4e678de](https://github.com/STAR7077/strawberry-django-plus/commit/4e678de009d867e371ff38f1b6a5b934ffe3df10))
* Remove monkey patches from django debug toolbar as it was released in its latest version ([2654c4e](https://github.com/STAR7077/strawberry-django-plus/commit/2654c4ec965d47e8737932b645774ca32bab6d19))
* Simplify aio.resolver ([d8f66f0](https://github.com/STAR7077/strawberry-django-plus/commit/d8f66f013871426f53b1b78e43f86a2211e0fd9d))
* simplify Node methods injection code ([2b1b259](https://github.com/STAR7077/strawberry-django-plus/commit/2b1b259da556022af847bf7f16f9d92c817180b0))
* support for strawberry 0.187.5+ ([6ec1de5](https://github.com/STAR7077/strawberry-django-plus/commit/6ec1de51a0094097406cae49c55dda15572a7742))
* use dataclass_transform from typing_extensions ([#236](https://github.com/STAR7077/strawberry-django-plus/issues/236)) ([2ca669c](https://github.com/STAR7077/strawberry-django-plus/commit/2ca669c5fc0b6597f7000f79fd87c6058311f3b9))
* Use print_schema from strawberry as it can now print schema directives correctly ([e751031](https://github.com/STAR7077/strawberry-django-plus/commit/e7510314050faff3f6682ccf03ee564d41f91171))
* use the new extension style using ([c5c521c](https://github.com/STAR7077/strawberry-django-plus/commit/c5c521c2213e324364d22b8b2e93f7cfe54518f3)), closes [#180](https://github.com/STAR7077/strawberry-django-plus/issues/180)


### Tests

* add full_clean kwargs tests ([05ab860](https://github.com/STAR7077/strawberry-django-plus/commit/05ab86096fc2fb5f15f1b45d253d54ffd52e0a29))
* Enable some extra pyright checkings and fix found issues ([af4febf](https://github.com/STAR7077/strawberry-django-plus/commit/af4febf9ccc9331761cacadb979bf2f993539fa2))
* Fix pyright issues ([f5eff94](https://github.com/STAR7077/strawberry-django-plus/commit/f5eff94e97ac4d6f0767723d616cac02efe00ec4))
* Fix pyright issues ([e01c19c](https://github.com/STAR7077/strawberry-django-plus/commit/e01c19c0ee7dd4f1a9b871b61ae21e5441664606))
* Fix pyright issues ([9288494](https://github.com/STAR7077/strawberry-django-plus/commit/92884940af66e81e14283b352f462670e1d42eb7))
* Fix pyright issues ([7153927](https://github.com/STAR7077/strawberry-django-plus/commit/71539274538d3aa06950cf310586d47a43e6e720))
* Workaround some pyright regressions ([a6ce324](https://github.com/STAR7077/strawberry-django-plus/commit/a6ce324a3c20cdbe89cd5f22401b90f5d2265730))


### Build System

* Bump typing-extensions requirement to 4.2.0+ ([4a9d801](https://github.com/STAR7077/strawberry-django-plus/commit/4a9d80123ca9d95d2fd452b16cf17ac05b256e4e))


### Continuous Integration

* add bootstrap-sha for release-please ([2ac69de](https://github.com/STAR7077/strawberry-django-plus/commit/2ac69deb69daca517387633cfcce1efbcaf47527))
* also run release actions for release branches ([6fe03cb](https://github.com/STAR7077/strawberry-django-plus/commit/6fe03cb7f53df0e8f549ad3f4bf74856e0ccab44))
* fix tests breaking due to not having a "debug-toolbar" extra anymore ([c87609f](https://github.com/STAR7077/strawberry-django-plus/commit/c87609f8d53bff28de944a5425cabc91a6046441))
* make sure release-please create release PRs for release branches ([249c28c](https://github.com/STAR7077/strawberry-django-plus/commit/249c28c529d25c87a58fb82d29f5505f4fc22416))


### Miscellaneous

* Add cache for github actions ([de21bd0](https://github.com/STAR7077/strawberry-django-plus/commit/de21bd0ebb7f5549478cf99791898e8e3b74d66f))
* Add python 3.11 to the list of supported python versions ([c75d511](https://github.com/STAR7077/strawberry-django-plus/commit/c75d5111aad59d993a751f646d51168429a91e93))
* Bump strawberry-graphql-django version requirement and remove the not needed anymore auto monkey patch ([906a643](https://github.com/STAR7077/strawberry-django-plus/commit/906a6431d695b45ff3cf7b98bbe78ace689eb919))
* Bump to version 1.10 ([7401040](https://github.com/STAR7077/strawberry-django-plus/commit/74010405bf804276e848bd7aff6d4b85b6f5ebf8))
* Bump to version 1.10.1 ([e3383b2](https://github.com/STAR7077/strawberry-django-plus/commit/e3383b2cbe3408034937686d657bff12407e6330))
* Bump to version 1.10.3 ([f2c74ab](https://github.com/STAR7077/strawberry-django-plus/commit/f2c74abbf63d57ac319968b19971d407760f9e63))
* Bump to version 1.11 ([32e51d6](https://github.com/STAR7077/strawberry-django-plus/commit/32e51d66b6a3838890d0bb7e5fc5c5fe43299093))
* Bump to version 1.11.2 ([a98e176](https://github.com/STAR7077/strawberry-django-plus/commit/a98e176d47e6aba57c38515fb6ee8d8578109d5f))
* Bump to version 1.13 ([5c3cc12](https://github.com/STAR7077/strawberry-django-plus/commit/5c3cc12d5a921e3a94b0037c085d85268edf2062))
* Bump to version 1.13.2 ([118c106](https://github.com/STAR7077/strawberry-django-plus/commit/118c106894b86940f21131661d87628edfe277d2))
* Bump to version 1.14.1 ([2750a3b](https://github.com/STAR7077/strawberry-django-plus/commit/2750a3b358d81439f38f2f8ffcc4ddf5c85ca470))
* Bump to version 1.14.2 ([e58ba50](https://github.com/STAR7077/strawberry-django-plus/commit/e58ba50396c4492acdb3e5ed540e6b79cc5e4dcc))
* Bump to version 1.15 ([b0921dc](https://github.com/STAR7077/strawberry-django-plus/commit/b0921dc94909c6d19c5c1fca259a035c4e2a6e59))
* Bump to version 1.17.0 ([2bf0e47](https://github.com/STAR7077/strawberry-django-plus/commit/2bf0e47c13f3ebfc8838ee2a006681ad97b44ba2))
* Bump to version 1.19 ([d2920a0](https://github.com/STAR7077/strawberry-django-plus/commit/d2920a04bef87372190171d30dbdf1e4cd1398a6))
* Bump to version 1.20 ([f316a45](https://github.com/STAR7077/strawberry-django-plus/commit/f316a45e7d4d0a45740a802a9659b9c86b6cc8fe))
* Bump to version 1.21 ([642927a](https://github.com/STAR7077/strawberry-django-plus/commit/642927ae1db87e0fea599e81f90111c835c7af96))
* Bump to version 1.23 ([15c7d3b](https://github.com/STAR7077/strawberry-django-plus/commit/15c7d3b3315dba5c44316476a310d3bf125bb2e7))
* Bump to version 1.24 ([89e077c](https://github.com/STAR7077/strawberry-django-plus/commit/89e077cb78a50f878a68e307ece50431a5eb098b))
* Bump to version 1.25 ([e3ed18e](https://github.com/STAR7077/strawberry-django-plus/commit/e3ed18e3f3cb62c371087ce7a30867ea17ee08c3))
* Bump to version 1.26.1 ([cf6da1f](https://github.com/STAR7077/strawberry-django-plus/commit/cf6da1f812254a9860fafd6dbc25d039b453feb8))
* Bump to version 1.27 ([85aeab9](https://github.com/STAR7077/strawberry-django-plus/commit/85aeab9688256ef6bc1662a546676167baa20c3d))
* Bump to version 1.28.1 ([4e355f1](https://github.com/STAR7077/strawberry-django-plus/commit/4e355f174618ad0f2b21083bb785ee222b6b2367))
* Bump to version 1.28.2 ([2db7141](https://github.com/STAR7077/strawberry-django-plus/commit/2db71419b1f1f2b6b4f2af020d2a8dacfbac5c5c))
* Bump to version 1.28.3 ([1f1c8d3](https://github.com/STAR7077/strawberry-django-plus/commit/1f1c8d3e5da2891a5d12807499e9828d8d11443b))
* Bump to version 1.28.6 ([0b5a426](https://github.com/STAR7077/strawberry-django-plus/commit/0b5a426b1091244745a94c3eb8259ad75e03e3ad))
* Bump to version 1.9 ([87260b8](https://github.com/STAR7077/strawberry-django-plus/commit/87260b827434e39c8f49867774b0ee9ac6890700))
* Bump to verssion 1.28.4 ([2b12bcc](https://github.com/STAR7077/strawberry-django-plus/commit/2b12bcc1c95c6182779f213e5fb0d859956efaf7))
* Bump version to 1.25.2 ([3356170](https://github.com/STAR7077/strawberry-django-plus/commit/33561703335a8ab3a0b904767bd384f78b658cf1))
* **deps-dev:** bump ipython from 8.9.0 to 8.10.0 ([1f63a09](https://github.com/STAR7077/strawberry-django-plus/commit/1f63a09aa0e386c72779dcd858c99d38a0aa6493))
* **deps-dev:** bump pymdown-extensions from 9.11 to 10.0 ([0d9f62e](https://github.com/STAR7077/strawberry-django-plus/commit/0d9f62ea7003d4232885ce5eb40dd5cfdc21c160))
* **deps:** bump django from 4.2 to 4.2.1 ([52852bd](https://github.com/STAR7077/strawberry-django-plus/commit/52852bdb19c89cf8a0d2943b2b819cbae3233cd1))
* **deps:** bump requests from 2.30.0 to 2.31.0 ([4a3c846](https://github.com/STAR7077/strawberry-django-plus/commit/4a3c8463e085c4b06487a75d3df18056a44a1cc4))
* **deps:** mark strawberry-graphql-django 0.10.0+ as not compatible ([733bfb1](https://github.com/STAR7077/strawberry-django-plus/commit/733bfb1c53706662a5980783456a25bd9b07d948))
* **deps:** update dependencies and fix style issues ([e076bab](https://github.com/STAR7077/strawberry-django-plus/commit/e076bab21829d4f461e526fb38c2d385b0da3bb8))
* **deps:** update dev dependencies ([26b472a](https://github.com/STAR7077/strawberry-django-plus/commit/26b472a2acaa88e5fa8578cb3c6961087f678745))
* **deps:** update dev dependencies ([eb2fa77](https://github.com/STAR7077/strawberry-django-plus/commit/eb2fa7723c4aa645f3b4d02e8903e9d3934b9e24))
* **deps:** update dev dependencies and enable more ruff rules ([3182d99](https://github.com/STAR7077/strawberry-django-plus/commit/3182d991f6e286db3c2b3a131fca6206f659f3ee))
* Disable reportUninitializedInstanceVariable for now as it is bugged in pyright ([2527233](https://github.com/STAR7077/strawberry-django-plus/commit/25272330f899b79f71d8435b2ae5ed3913257413))
* Enable extra pyright check ([2ec0f9a](https://github.com/STAR7077/strawberry-django-plus/commit/2ec0f9a76b14de8c0663cbcf3a5665c1244f3502))
* enable more ruff rules ([d29fa22](https://github.com/STAR7077/strawberry-django-plus/commit/d29fa2269ea834b4bbf5aed4361495901c210257))
* Fix typing issues from latest pyright version ([45108b9](https://github.com/STAR7077/strawberry-django-plus/commit/45108b90be112d3a3c669af0afc8d1a5589b51b2))
* Improve typing ([6dc8e40](https://github.com/STAR7077/strawberry-django-plus/commit/6dc8e40928f6bfa65f184a1c5dc36c61163ae142))
* Install extras when running tests ([1e687cc](https://github.com/STAR7077/strawberry-django-plus/commit/1e687ccaf3b755241c6519db9490a70e514f121a))
* **main:** release 0.1.0 ([70535e4](https://github.com/STAR7077/strawberry-django-plus/commit/70535e4cb6e6c6f61f78e1608ca079e461a48ba0))
* **main:** release 2.5.0 ([2a94283](https://github.com/STAR7077/strawberry-django-plus/commit/2a942839b523bdd72797eb47547a49ff02db43d5))
* **main:** release 2.6.0 ([#218](https://github.com/STAR7077/strawberry-django-plus/issues/218)) ([d12d517](https://github.com/STAR7077/strawberry-django-plus/commit/d12d5173358798075d831cb097676622196975ae))
* **main:** release 2.6.1 ([#220](https://github.com/STAR7077/strawberry-django-plus/issues/220)) ([7623700](https://github.com/STAR7077/strawberry-django-plus/commit/7623700b41a77c29e4a22c1555358d88ff49b024))
* **main:** release 2.6.2 ([#228](https://github.com/STAR7077/strawberry-django-plus/issues/228)) ([7d44d94](https://github.com/STAR7077/strawberry-django-plus/commit/7d44d94f5698edaea8b8c7246679cb54d4eef36b))
* **main:** release 2.6.3 ([#232](https://github.com/STAR7077/strawberry-django-plus/issues/232)) ([56aa27d](https://github.com/STAR7077/strawberry-django-plus/commit/56aa27d71bd99195c07629e4f91a40563d869f8b))
* **main:** release 2.6.4 ([#239](https://github.com/STAR7077/strawberry-django-plus/issues/239)) ([a726e65](https://github.com/STAR7077/strawberry-django-plus/commit/a726e6581dfac569b9e8a798bd83df2103c4033f))
* **main:** release 3.0.0 ([#240](https://github.com/STAR7077/strawberry-django-plus/issues/240)) ([c601398](https://github.com/STAR7077/strawberry-django-plus/commit/c6013985a384db999d085499d8ed08add4895729))
* **main:** release 3.0.1 ([#241](https://github.com/STAR7077/strawberry-django-plus/issues/241)) ([f53bf89](https://github.com/STAR7077/strawberry-django-plus/commit/f53bf894f7de3fcbefdab939b566ef91ff7594c5))
* **main:** release 3.0.2 ([#251](https://github.com/STAR7077/strawberry-django-plus/issues/251)) ([031adb1](https://github.com/STAR7077/strawberry-django-plus/commit/031adb1809e656004f15c3b653b29ef292f29cec))
* **main:** release 3.0.3 ([#253](https://github.com/STAR7077/strawberry-django-plus/issues/253)) ([e9a4b59](https://github.com/STAR7077/strawberry-django-plus/commit/e9a4b5900bea8abf94602f19c717df5984a993c1))
* **main:** release 3.1.0 ([#257](https://github.com/STAR7077/strawberry-django-plus/issues/257)) ([e720dbf](https://github.com/STAR7077/strawberry-django-plus/commit/e720dbf6f184f59575921d90f555dca3f42ea118))
* **main:** release 3.1.1 ([#262](https://github.com/STAR7077/strawberry-django-plus/issues/262)) ([22805b4](https://github.com/STAR7077/strawberry-django-plus/commit/22805b452220b62b3074030f6968af137c9fd1c2))
* migrate to ruff for linting ([5265dea](https://github.com/STAR7077/strawberry-django-plus/commit/5265deae44a510ab3ffee2c03c300f96e374bde3))
* modernize CI/CD scripts and use release-please for releases ([a908625](https://github.com/STAR7077/strawberry-django-plus/commit/a908625ee9da0fcbab2e3ff6eab931ab4ac61cb1))
* **pyright:** fix pyright issues ([b640c21](https://github.com/STAR7077/strawberry-django-plus/commit/b640c211986ccf29219765cafc37fe67f748e3b6))
* Release 1.30 ([84f76e0](https://github.com/STAR7077/strawberry-django-plus/commit/84f76e0ab1c459ad529136b395cb1d23a6c6dc64))
* Release 1.30.1 ([8057d62](https://github.com/STAR7077/strawberry-django-plus/commit/8057d62c38eb33c95fc035454441a961f93034f5))
* Release 1.31 ([5f75385](https://github.com/STAR7077/strawberry-django-plus/commit/5f75385434b3cea7329c91f24f3b8cc9f84d4312))
* Release 1.32 ([4430b8e](https://github.com/STAR7077/strawberry-django-plus/commit/4430b8e1c93381c45d26feb4437c90d95dc33f37))
* Release 1.32.1 ([ad62311](https://github.com/STAR7077/strawberry-django-plus/commit/ad62311151039c4792bdac1bac7b1865f5932d7a))
* Release 1.32.2 ([2ed34a3](https://github.com/STAR7077/strawberry-django-plus/commit/2ed34a3334cfae63e0f7f91b6aa6d065be467bde))
* Release 1.32.3 ([429e7f3](https://github.com/STAR7077/strawberry-django-plus/commit/429e7f3d745d462d68f7036dbfb27306aed8f475))
* Release 1.33.2 ([4c21439](https://github.com/STAR7077/strawberry-django-plus/commit/4c21439ec86459c1ee23183ac07c48b77649b5c8))
* Release 1.34 ([e584a2d](https://github.com/STAR7077/strawberry-django-plus/commit/e584a2d39beafef852990610d4e1369305d73bbd))
* release 2.0.4 ([fc2969a](https://github.com/STAR7077/strawberry-django-plus/commit/fc2969ae51d13d479a7cfa8c49f12674bd778f58))
* release 2.0.5 ([6ce3d50](https://github.com/STAR7077/strawberry-django-plus/commit/6ce3d5047bc486723fa9e081e3ec9cdb5722056c))
* release 2.0.6 ([739783f](https://github.com/STAR7077/strawberry-django-plus/commit/739783f289cb177b0abc05d14cd38fd202aae93a))
* release 2.1.0 ([7601d31](https://github.com/STAR7077/strawberry-django-plus/commit/7601d31306fdd8d6f2814bb0188005b4451ffb20))
* release 2.2.0 ([65403e2](https://github.com/STAR7077/strawberry-django-plus/commit/65403e2d8f2d926172cda1579abd91f81d259d30))
* release 2.3.0 ([6d9115b](https://github.com/STAR7077/strawberry-django-plus/commit/6d9115bb6f3052e1f7b6e1c59b05c52e1b78f952))
* release 2.3.1 ([cb00f0c](https://github.com/STAR7077/strawberry-django-plus/commit/cb00f0cb3f254e5ffa08e1373332b9a7daa1095c))
* **release:** bump to version 2.0.0 ([cd68852](https://github.com/STAR7077/strawberry-django-plus/commit/cd688527884839febe9b93513a6f8352e94c8e62))
* **release:** bump to version 2.0.1 ([9172d3a](https://github.com/STAR7077/strawberry-django-plus/commit/9172d3a6e74fc4c04ac9f1e488a7533da101db28))
* Remove an unnecessary "type:ignore" comment ([4562aff](https://github.com/STAR7077/strawberry-django-plus/commit/4562aff500fe853fb3e843efaa9f38a72f63e8b0))
* remove semgrep (it takes too long to run) ([32ee6d4](https://github.com/STAR7077/strawberry-django-plus/commit/32ee6d4cba938d55624979f41c5a1f6ac5ae7a99))
* Run pyright on CICD ([29d6569](https://github.com/STAR7077/strawberry-django-plus/commit/29d65694595439c9bab4397aa665efc16c036c69))
* Solve some typing issues from latest pyright version ([6048c68](https://github.com/STAR7077/strawberry-django-plus/commit/6048c680cc468491471869c61f3effda2713888e))
* The main branch was renamed to main ([f2e6d1f](https://github.com/STAR7077/strawberry-django-plus/commit/f2e6d1f72d1caed51985d8bebdbeb8731f37d840))
* Update CICD actions ([691b6be](https://github.com/STAR7077/strawberry-django-plus/commit/691b6bed6690e3f5f33a993fa6207fd53d4b89b6))
* Update dependencies and fix typing issues ([4394dc1](https://github.com/STAR7077/strawberry-django-plus/commit/4394dc153ad88a01fe1c51d240cf144b1c82f5b3))
* update dev dependencies ([2b4e010](https://github.com/STAR7077/strawberry-django-plus/commit/2b4e010ba0ae0ce23524343f5c2ccc55ec414d23))
* Update dev dependencies ([00ee42d](https://github.com/STAR7077/strawberry-django-plus/commit/00ee42d43dd80467204d679e913ba649c3427a90))
* Update dev dependencies ([f08326e](https://github.com/STAR7077/strawberry-django-plus/commit/f08326eb42a0f184eb4124413994b8741bb04bc7))
* Update dev dependencies ([1b84237](https://github.com/STAR7077/strawberry-django-plus/commit/1b842370732f821baccf6ba64ae7978816ed6bbe))
* Update dev dependencies ([7c82082](https://github.com/STAR7077/strawberry-django-plus/commit/7c820828eb4b349f53745b86aac526df7ec49bd7))
* Update dev dependencies ([274233e](https://github.com/STAR7077/strawberry-django-plus/commit/274233ec070bd73e0a8ccba89d0b0ffcfbd352d4))
* Update dev dependencies ([aae277e](https://github.com/STAR7077/strawberry-django-plus/commit/aae277e9a88099a5cef273f8868029472933c51d))
* Update dev dependencies ([27287f1](https://github.com/STAR7077/strawberry-django-plus/commit/27287f1aca4efdf07f64cf6a8c8f0f67a50b621c))
* Update dev dependencies ([5be2275](https://github.com/STAR7077/strawberry-django-plus/commit/5be2275c11dd2ce33f1072dec38477142d449297))
* Update dev dependencies ([57fcf45](https://github.com/STAR7077/strawberry-django-plus/commit/57fcf45645ce1a20ec721e5a09a6aab3dcbf7cca))
* Update dev dependencies ([09c1aea](https://github.com/STAR7077/strawberry-django-plus/commit/09c1aeadc2163b420ab316555a4e1b846ec444ee))
* Update dev dependencies ([7fa3369](https://github.com/STAR7077/strawberry-django-plus/commit/7fa33695db9b3ff9f0704e30fd6435a52414bde7))
* Update dev dependencies and fix pyright issues ([d678683](https://github.com/STAR7077/strawberry-django-plus/commit/d678683b93d4498f11e06627a6bd4c2bdf43ba7d))
* Update dev requirements ([631cbf2](https://github.com/STAR7077/strawberry-django-plus/commit/631cbf2d68c57f540503fb6d9a0561a32becf47d))
* Update dev requirements ([e00ccc0](https://github.com/STAR7077/strawberry-django-plus/commit/e00ccc03a4b53cd800456547470f4b9b83398791))
* Update dev requirements ([4dd529b](https://github.com/STAR7077/strawberry-django-plus/commit/4dd529b1bfdf3b1d41700bce271c4378d8958544))
* Update dev requirements ([f52da23](https://github.com/STAR7077/strawberry-django-plus/commit/f52da23367b154d1235b288b272c7441225e6d21))
* Update dev requirements ([d550c20](https://github.com/STAR7077/strawberry-django-plus/commit/d550c20389479738eb42aaf55073327f5c519fda))
* update poetry.lock ([a3f3f1a](https://github.com/STAR7077/strawberry-django-plus/commit/a3f3f1a268c3f5c0ca760e129942e692b440db3a))

## 0.1.0 (2025-03-31)


### ⚠ BREAKING CHANGES

* remove debug toolbar integration
* migrate relay to strawberry's implementation ([#235](https://github.com/SEO7077/strawberry-django-plus/issues/235))
* **relay:** use Connection class from the field annotation and also allow a Connection to be returned by the base_resolver
* Do not make total_count mandatory anymore
* Use print_schema from strawberry as it can now print schema directives correctly
* Fix schema directive usage after latest changes from strawberry
* Remove monkey patches from django debug toolbar as it was released in its latest version

### Features

* add description to enums from django choices ([#217](https://github.com/SEO7077/strawberry-django-plus/issues/217)) ([be53c08](https://github.com/SEO7077/strawberry-django-plus/commit/be53c0811a6c85859e0640a25cc009de4fcee696))
* add semgrep to pre-commit-hooks ([b9e7a8d](https://github.com/SEO7077/strawberry-django-plus/commit/b9e7a8d4b3c46473e4f5401d538e7706d62e69e7))
* Add support for newest way of declaring info for resolvers in strawberry 0.115.0 ([dbfdf87](https://github.com/SEO7077/strawberry-django-plus/commit/dbfdf877445a4350a687eb47337ac9267b80da7b))
* add support for passing graphql_type to Field instances ([55a906e](https://github.com/SEO7077/strawberry-django-plus/commit/55a906e99c0fffe5d5c5643bd676eee472df78e7))
* add support for resolving `auto` fields for properties and cached_properties ([7b2ab43](https://github.com/SEO7077/strawberry-django-plus/commit/7b2ab43cffe7b852a4b805f65632192074c656ed)), closes [#198](https://github.com/SEO7077/strawberry-django-plus/issues/198)
* Add support for running debug_toolbar with ASGI ([8468c6f](https://github.com/SEO7077/strawberry-django-plus/commit/8468c6fec40cef61fc33d413b74eca77b117c002))
* Add support for strawberry-django-graphql &gt;= 0.4 ([de9a031](https://github.com/SEO7077/strawberry-django-plus/commit/de9a031d907a7570d44d59e81fd1a81e944ef32e))
* Add support for strawberry-graphql-django 0.5 ([62c2995](https://github.com/SEO7077/strawberry-django-plus/commit/62c2995c5bf42ee6fda59ca32d1abd42e7bc2109))
* Add support to optimize GenericRelation fields ([40db760](https://github.com/SEO7077/strawberry-django-plus/commit/40db760f8fbbf4620c6e61d401f803b564c32d57))
* Allow to change Connection class for Nodes and Edge class for Connections ([1003702](https://github.com/SEO7077/strawberry-django-plus/commit/10037021218792fbafcda67b1ce470e159a0bf90))
* Allow to pass handle_django_errors=False to CRUD mutations ([a8fb3f6](https://github.com/SEO7077/strawberry-django-plus/commit/a8fb3f69bf86e1ab1686dd442aad5d03b86db598)), closes [#79](https://github.com/SEO7077/strawberry-django-plus/issues/79)
* Allow to specify optimizer params directly to django's type ([34c80b2](https://github.com/SEO7077/strawberry-django-plus/commit/34c80b23c985de9667eca681dc756fee0aa92bb9)), closes [#44](https://github.com/SEO7077/strawberry-django-plus/issues/44)
* Allow to use lambdas for Prefetch optimization ([45e5355](https://github.com/SEO7077/strawberry-django-plus/commit/45e53557419f0a9f480d56f9c94f4df2891d1445)), closes [#83](https://github.com/SEO7077/strawberry-django-plus/issues/83)
* Apply get_queryset when resolving Django relay.Node types ([c3468e4](https://github.com/SEO7077/strawberry-django-plus/commit/c3468e4ef3cf63f4278f6ce14c8b0746e28d563a))
* Customizable typename for Node; Fix: GlobalID parse_literal vars, UNSET as default_value ([477acdf](https://github.com/SEO7077/strawberry-django-plus/commit/477acdf922df3b0880c8504e241a9a36b468eff5))
* enum type for standard django choices ([c3d3a7e](https://github.com/SEO7077/strawberry-django-plus/commit/c3d3a7e995145d7034888b74ad66ca8076a208ef))
* expose `__version__` on the package ([5d2fe07](https://github.com/SEO7077/strawberry-django-plus/commit/5d2fe07e1551fc7b0aff7c8efacc49ffec075580))
* Expose mutation through gql.django.mutation ([a91c3fb](https://github.com/SEO7077/strawberry-django-plus/commit/a91c3fb096633d0ec00747cff7d28f709ba29f2a))
* Expose UNSET to gql so it can be used with gql.UNSET ([af18e41](https://github.com/SEO7077/strawberry-django-plus/commit/af18e41f5f2993c493f8fd6df9e1ec99bcbce716))
* Improve input mutations to better handle m2m with intermediate values ([53d479b](https://github.com/SEO7077/strawberry-django-plus/commit/53d479b903297bbf9cea9eae8ce2973fe2b7eb0b))
* Make defined types comparable and hashable ([3cd100d](https://github.com/SEO7077/strawberry-django-plus/commit/3cd100d89afc333db8da22dfd2df3e42fea407f3)), closes [#158](https://github.com/SEO7077/strawberry-django-plus/issues/158)
* mark this lib as deprecated and add a documentation on how to migrate to strawberry_django ([472f2a2](https://github.com/SEO7077/strawberry-django-plus/commit/472f2a2723607379bab88999adbf29e166ad48b2))
* new GlobalID.aresolve_node to help resolving asynchronous nodes ([9d34f1a](https://github.com/SEO7077/strawberry-django-plus/commit/9d34f1a09ce284ab2380bf44307e375617df0277))
* New mutation that acts like input_mutation, but without converting arguments to an input type ([94805ca](https://github.com/SEO7077/strawberry-django-plus/commit/94805cafe878c2f5bc94c9e729f55d19b2f6dbe9))
* Optimize fields that return an interface (e.g. relay.Node) ([6ec51ce](https://github.com/SEO7077/strawberry-django-plus/commit/6ec51cefebe07a8f94f473c913732b6362297046)), closes [#28](https://github.com/SEO7077/strawberry-django-plus/issues/28)
* Optimize GenericForeignKey by prefetch_related them ([49a30f5](https://github.com/SEO7077/strawberry-django-plus/commit/49a30f5f00406483c1852e88030abd1822d0b7d3))
* **optimizer:** support custom QS for prefetches ([7bc6c30](https://github.com/SEO7077/strawberry-django-plus/commit/7bc6c30f9de1d22cb23bc1bb217b73cedaaf3d74))
* remove debug toolbar integration ([d445154](https://github.com/SEO7077/strawberry-django-plus/commit/d44515441a638331c37c9908fd7fbf8ccb18598e))
* Separate the logic for generating the Q filter for filter_for_user function so that it can be reused elsewhere ([c77014b](https://github.com/SEO7077/strawberry-django-plus/commit/c77014bbcbf107bc6052213684b248ace0e21e0d))
* start testing on Django 4.2 ([c277162](https://github.com/SEO7077/strawberry-django-plus/commit/c27716258bbbdcccdfc5548c9680a1f9d4ff65ce))
* Support field metadata from upstream strawberry ([a49d6f5](https://github.com/SEO7077/strawberry-django-plus/commit/a49d6f5c571b18cf741b1155e3fab602265a9256))
* Support for django 4.1 ([4656403](https://github.com/SEO7077/strawberry-django-plus/commit/4656403b10326bf60f9e7b0bc1626c4145b7dd75))
* Support full_clean when directly invoking resolver ([5e05a20](https://github.com/SEO7077/strawberry-django-plus/commit/5e05a202fd93be4687698d2865b703e92f14f02a))
* Support mutation resolvers that return unions ([4847059](https://github.com/SEO7077/strawberry-django-plus/commit/4847059a246555dc03bc835341405dff95c66800))
* Support nested foreignkey creation for mutations ([a9fe762](https://github.com/SEO7077/strawberry-django-plus/commit/a9fe76206515ec53c7cbcc8ce17c4e6230294b58)), closes [#82](https://github.com/SEO7077/strawberry-django-plus/issues/82)
* Support only/select_related hints for many relations ([5a6ae3f](https://github.com/SEO7077/strawberry-django-plus/commit/5a6ae3fc77b7de7d83f5298d869c683eb00c390b))
* Support strawberry 0.109+ ([395547a](https://github.com/SEO7077/strawberry-django-plus/commit/395547ac2769b422871043aaf3ad39904146f3a8)), closes [#40](https://github.com/SEO7077/strawberry-django-plus/issues/40)
* Support Strawberry 0.139 ([699c3f0](https://github.com/SEO7077/strawberry-django-plus/commit/699c3f0f9dff56424e575d55990d3c07129795ce)), closes [#142](https://github.com/SEO7077/strawberry-django-plus/issues/142)
* Support Unions for ensure_type in resolvers ([6c08d8f](https://github.com/SEO7077/strawberry-django-plus/commit/6c08d8f00fcdc39d2e0e714ce93e55f8da3d24f0))
* update dev requirements and enable more ruff rules ([301c475](https://github.com/SEO7077/strawberry-django-plus/commit/301c47589caba4556058ba4e7c49e0b4526d257c))
* use a type's get_queryset for Relay connections if it defines one ([#215](https://github.com/SEO7077/strawberry-django-plus/issues/215)) ([0b7c122](https://github.com/SEO7077/strawberry-django-plus/commit/0b7c1225b6f65c6ceb3a34328e88898110f0c951))
* Use the CONNECTION_CLASS defined on node when creating a connection field ([cd2926d](https://github.com/SEO7077/strawberry-django-plus/commit/cd2926dc6abfc139a98b6ce05da7bbed268e360d))


### Bug Fixes

* Abort only optimization when manually prefetching something ([758661e](https://github.com/SEO7077/strawberry-django-plus/commit/758661eebb311214878d13b62800de1eb04b2ab4))
* add settings to disable auto-enum generation + unique class name ([4343a72](https://github.com/SEO7077/strawberry-django-plus/commit/4343a723cc9a15db0b94ab9bf0a40aec1402ea17))
* allow `field_name` to be passed for node and connections ([7093e42](https://github.com/SEO7077/strawberry-django-plus/commit/7093e42e8188a658b49477d4439cce5054b21334))
* allow connections to be typed as unions ([9268869](https://github.com/SEO7077/strawberry-django-plus/commit/926886918d0c869fec9cd628938fea5a8f4cc95a)), closes [#223](https://github.com/SEO7077/strawberry-django-plus/issues/223)
* allow mutation full clean with kwargs ([341c4c6](https://github.com/SEO7077/strawberry-django-plus/commit/341c4c6a67215e4e232db4048266c7d6260c9bb0))
* allow update of nested input fields on foreign key relationships ([ad437cc](https://github.com/SEO7077/strawberry-django-plus/commit/ad437ccd39c5f203478cc0f81d8af14bb3567d86))
* also support `auto` when checking for auto annotations ([92dc46b](https://github.com/SEO7077/strawberry-django-plus/commit/92dc46bcd7fe0f7fedb7c21ae426811bb7e9fc8e))
* avoid "lookup was already seen with a different queryset" by merging existing prefetches together with hints ([2aced82](https://github.com/SEO7077/strawberry-django-plus/commit/2aced8201485c0ccc5dad71f5484f535ce6e62ae))
* Avoid AttributeError when retrieving django type's attributes at creation time ([0783742](https://github.com/SEO7077/strawberry-django-plus/commit/078374299fd0fd0643f85a50d77402da2a483b20)), closes [#58](https://github.com/SEO7077/strawberry-django-plus/issues/58)
* broken django-guardian link ([28c91a1](https://github.com/SEO7077/strawberry-django-plus/commit/28c91a19233e59772b77333e5652c1d510408eed))
* build won't break when a generic relation is used ([28c5ea2](https://github.com/SEO7077/strawberry-django-plus/commit/28c5ea23598d73a1002765633f56868140e8a44c))
* Cast object_pk to model pk type ([c793cf1](https://github.com/SEO7077/strawberry-django-plus/commit/c793cf1a5cbb2181c477fac59934387b7246846f))
* Check for Awaitable the correct way ([e663f95](https://github.com/SEO7077/strawberry-django-plus/commit/e663f95a361f3079d896c8cae880570c93782af9))
* Check for coroutrine instead of awaitable ([62145e4](https://github.com/SEO7077/strawberry-django-plus/commit/62145e413a37f6d0158040762155ab4827b70ddb))
* Choices field must be installed in dev ([f7bf59a](https://github.com/SEO7077/strawberry-django-plus/commit/f7bf59a78a16c4d7df5966b4fb533cf0e4e8e224))
* correct when to use model_field.field ([cd68f99](https://github.com/SEO7077/strawberry-django-plus/commit/cd68f9910f546d4cbfcd7272707d36b8e8e27776))
* dataclass to typeddict ([f40490d](https://github.com/SEO7077/strawberry-django-plus/commit/f40490d36a2052ef008bf28e70bb415bd79113c8))
* De morgan law fix from last merged PR ([d7e98ee](https://github.com/SEO7077/strawberry-django-plus/commit/d7e98ee8dfea573350c4c8a607a163598ab4340a))
* delete instead of remove non-nullable foreign key set objects ([cf2344e](https://github.com/SEO7077/strawberry-django-plus/commit/cf2344ebc077ea7edf99e6e2b10b645d19b78d8a))
* django connection field remove kwargs not in default_args ([d197440](https://github.com/SEO7077/strawberry-django-plus/commit/d1974400a5e1f79c69446784f06927e1fd09ee3f))
* **django-relay:** fix filter/order not being applied to django relay connections ([5ed102d](https://github.com/SEO7077/strawberry-django-plus/commit/5ed102d307b2d2fc3a75a93ada8fbe4a2a6e633c)), closes [#170](https://github.com/SEO7077/strawberry-django-plus/issues/170)
* DjangoMutation should not receive an `input_type` ([7450e1e](https://github.com/SEO7077/strawberry-django-plus/commit/7450e1eab67a5619f40ebfe4ea279c45deccebfe)), closes [#80](https://github.com/SEO7077/strawberry-django-plus/issues/80)
* Do not check permissions for OperationInfo ([216e12b](https://github.com/SEO7077/strawberry-django-plus/commit/216e12be230c4001b2c3d104b11877a3dc02b975))
* Do not keep "is_type_of" from parents ([8b1ba26](https://github.com/SEO7077/strawberry-django-plus/commit/8b1ba261ab4eee9d6b5a1ecaab7bd97b443685ae))
* do not try to merge fragments, they have no name ([0dec3de](https://github.com/SEO7077/strawberry-django-plus/commit/0dec3debba7e29b52fb0cee4ab83e16174ad712d))
* Do not use Iterable/Mapping to avoid iterating over wrong types (e.g. strings) ([6db7f42](https://github.com/SEO7077/strawberry-django-plus/commit/6db7f423b982d0a01f0c946ae1c4020cd788d44c))
* don't make full_clean positional ([0925c86](https://github.com/SEO7077/strawberry-django-plus/commit/0925c86ee4feb3de13630874a4044afa8748a857))
* Fix `gql.django.connection` ignoring its source ([f60eb89](https://github.com/SEO7077/strawberry-django-plus/commit/f60eb892557dcb32d50c34204c5027eb4ead1c22))
* fix a nit in factory faker ([3edb8d9](https://github.com/SEO7077/strawberry-django-plus/commit/3edb8d96fe5b12c262087ac3ef9fce21ab115854))
* Fix a typing issue with the latest version of pyright ([f91adf3](https://github.com/SEO7077/strawberry-django-plus/commit/f91adf3332b59e647a84950f5f262f7737166c64))
* Fix a typo that was preventing Django types from defining their own resolve_connection if they wanted ([c7d7e36](https://github.com/SEO7077/strawberry-django-plus/commit/c7d7e364a73c23f7b29235992338676848e7ec71)), closes [#49](https://github.com/SEO7077/strawberry-django-plus/issues/49)
* fix a wrongly refactored code from previous commit ([5b7553c](https://github.com/SEO7077/strawberry-django-plus/commit/5b7553c05baf864a3a4f2965ca6fc6a444af487a))
* fix class inherited fields not being evaluated correctly ([2491cb3](https://github.com/SEO7077/strawberry-django-plus/commit/2491cb3cf086ced0a686eb4e742de30d5c9aa5fb)), closes [#247](https://github.com/SEO7077/strawberry-django-plus/issues/247)
* fix django versioning on test actions ([b313cd9](https://github.com/SEO7077/strawberry-django-plus/commit/b313cd9d33dffbb1e5f0ee0174b605f1cb898af6))
* fix edge case where pk is unset ([4fe52b5](https://github.com/SEO7077/strawberry-django-plus/commit/4fe52b59bccb13b1cf1c8a23798763cbe503b5d6))
* Fix filters breaking relay connections ([222231b](https://github.com/SEO7077/strawberry-django-plus/commit/222231b7f5662e586ca24fd35784e7407019100f)), closes [#47](https://github.com/SEO7077/strawberry-django-plus/issues/47)
* Fix github actions badge ([7a87d6c](https://github.com/SEO7077/strawberry-django-plus/commit/7a87d6c6739608181243e3b3865704f373db721e))
* Fix issues with python 3.9 and lower ([06bfe41](https://github.com/SEO7077/strawberry-django-plus/commit/06bfe41a4e38abf8e197c64c619847c9ed47060b))
* fix LICENSE author ([cdc9b56](https://github.com/SEO7077/strawberry-django-plus/commit/cdc9b56994454dd33af4d0d5fb9ab6373a6b50bc))
* fix missing checkout version ([2993223](https://github.com/SEO7077/strawberry-django-plus/commit/299322385cff41b3241cebe7688aa7e5a5b2d7f1))
* fix missing export of django_resolver ([bcea6a4](https://github.com/SEO7077/strawberry-django-plus/commit/bcea6a464f18a74241a2d0d736a0a9b8dfd3e70c))
* fix optimizer not working on some cases with fragment spreading ([4b3d18e](https://github.com/SEO7077/strawberry-django-plus/commit/4b3d18e3a425eb0fe817a6ccd87de329810b680a)), closes [#144](https://github.com/SEO7077/strawberry-django-plus/issues/144)
* Fix poetry.lock requirements ([ddf0b0b](https://github.com/SEO7077/strawberry-django-plus/commit/ddf0b0b386d3d48b6c7727ed8af9f70daac8004c))
* Fix possibly unbound values and other typing issues ([9fe1a75](https://github.com/SEO7077/strawberry-django-plus/commit/9fe1a756dff74e0f50c6e5cadd3f596f3c153d6e))
* Fix prefetch optimization ([e16ab9d](https://github.com/SEO7077/strawberry-django-plus/commit/e16ab9dd00df95a6c7f87a13b9a145856f03dcc6))
* Fix pyright issues ([ca0a6fc](https://github.com/SEO7077/strawberry-django-plus/commit/ca0a6fc91aa8f65ac1f156c30fc072a53b0314a5))
* fix relay connections not being optimized ([931a6ce](https://github.com/SEO7077/strawberry-django-plus/commit/931a6ce4d990ab188c727979dcce1d8addd1a2c8))
* Fix remaining issues with many to many inputs ([f909063](https://github.com/SEO7077/strawberry-django-plus/commit/f9090637e2388e98670ffffd0a51485e7dbfd365))
* Fix resolving issues with latest changes from strawberry-graphql ([03a7040](https://github.com/SEO7077/strawberry-django-plus/commit/03a7040e2c8f8e4c3b4c970e4ec058e39016e147))
* fix resolving model ids, implement suggested code improvements ([a23dfbf](https://github.com/SEO7077/strawberry-django-plus/commit/a23dfbfe70352e8f53cc6579993a908c405bd819))
* Fix schema printing tests ([5ec137c](https://github.com/SEO7077/strawberry-django-plus/commit/5ec137cf628a5d75512bf0ed0e05c1c8a63ba1a1))
* Fix strange mypy issue introduced in [#137](https://github.com/SEO7077/strawberry-django-plus/issues/137) ([3995e6c](https://github.com/SEO7077/strawberry-django-plus/commit/3995e6c877ec7645eed4f5f8396d425221f04f64)), closes [#145](https://github.com/SEO7077/strawberry-django-plus/issues/145)
* Fix support for the way strawberry checks for auto now ([daab754](https://github.com/SEO7077/strawberry-django-plus/commit/daab7542f35e3d52d1b9d0b88d8a78e036e618ce))
* fix typing for update/delete mutations ([73b4510](https://github.com/SEO7077/strawberry-django-plus/commit/73b451063aa0b57079d2bda86fe61f08448dcb2c))
* Fix typing issues found by latest pyright version ([c02fe9d](https://github.com/SEO7077/strawberry-django-plus/commit/c02fe9d54f328119a97be806ce3d927d227c555a))
* fixes NodeInput parsing to dict ([4fe52b5](https://github.com/SEO7077/strawberry-django-plus/commit/4fe52b59bccb13b1cf1c8a23798763cbe503b5d6))
* Force is_basic_field to return False to fix resolving issues with our custom fields ([27bacae](https://github.com/SEO7077/strawberry-django-plus/commit/27bacae58eb2a5bca6ee9a0ed30c064a6daaa067))
* GENERATE_ENUMS_FROM_CHOICES default to False ([dd5d7dc](https://github.com/SEO7077/strawberry-django-plus/commit/dd5d7dc857837ba309cb60bdc127fac01bcd0c9d))
* inject filters/order at once to avoid one of them missing also removing the other one ([9f4011f](https://github.com/SEO7077/strawberry-django-plus/commit/9f4011f5ad7481308ab20a6b2f28b16025d07ff5)), closes [#243](https://github.com/SEO7077/strawberry-django-plus/issues/243)
* Issue 33 ([6316f8e](https://github.com/SEO7077/strawberry-django-plus/commit/6316f8e4a744b7bda9c3b30eee4de844bea9ad75))
* Keep django_name when it is provided by the user ([1e5cdf8](https://github.com/SEO7077/strawberry-django-plus/commit/1e5cdf88ed392a325f4dd6d51599a192d45e820a))
* Limit relay split to 1 so that the key can contain ":" characters ([1bd0b95](https://github.com/SEO7077/strawberry-django-plus/commit/1bd0b957abaa416f9244b54e686b08e6266bc7ec))
* loosen errors for unions of django types when checking for filters/ordering ([694efa4](https://github.com/SEO7077/strawberry-django-plus/commit/694efa41727e945b8e8525d91c1fbccd056aebdf))
* Make djang-debug-toolbar really an optional dependency by adding it to extras ([2772b8b](https://github.com/SEO7077/strawberry-django-plus/commit/2772b8b1d0aa72d749677a3caaeb3ec43f3d59c9))
* Make relay's input types allow UNSET as the default value ([695610b](https://github.com/SEO7077/strawberry-django-plus/commit/695610b736897660918856a9ecf41d314b3da619))
* Make sure order gets added to the connection when defined on type ([e455054](https://github.com/SEO7077/strawberry-django-plus/commit/e455054c64806da9fffeb8a3b68d6025bf723c98))
* Make sure the class is the same when comparing to other objects ([67d9931](https://github.com/SEO7077/strawberry-django-plus/commit/67d99317f9cf519a4f1ebf97f0b5c0f46863c05d))
* make sure the correct node type is passed on inheritance with other types/interfaces implementing Node ([e03016f](https://github.com/SEO7077/strawberry-django-plus/commit/e03016f5f39e119fbd17283d3ff5746d2f9410bf))
* Make sure to keep original field annotations in the input type ([3cf9d86](https://github.com/SEO7077/strawberry-django-plus/commit/3cf9d8697d9541d179e818d6504ad81a10aee8f5))
* Make sure we keep extra types ordered in the printer ([7235475](https://github.com/SEO7077/strawberry-django-plus/commit/72354757209b6c3080bedd992b16b7a6e720be89))
* missing return for the async resolver ([9894ab8](https://github.com/SEO7077/strawberry-django-plus/commit/9894ab85e48c79f2bf6bff3e9afe699fa61dd6f0))
* **mutations:** ensure that pk is not added by the django base field in create/update/delete mutations ([ef94f9f](https://github.com/SEO7077/strawberry-django-plus/commit/ef94f9f933cbef3393843055bf9067ab395fd861)), closes [#165](https://github.com/SEO7077/strawberry-django-plus/issues/165)
* only format message with params if params is not empty ([ccf5bd5](https://github.com/SEO7077/strawberry-django-plus/commit/ccf5bd511c04cd33dd54a43d23596c8616df6bc2))
* Only map errors if the field is set to handle them ([c11a91c](https://github.com/SEO7077/strawberry-django-plus/commit/c11a91c5ed300dd3ab935ab5e6c3aecc5702c1fa)), closes [#79](https://github.com/SEO7077/strawberry-django-plus/issues/79)
* Only should only be aborted when the whole model is specified (i.e. as a string) ([3bbe8f2](https://github.com/SEO7077/strawberry-django-plus/commit/3bbe8f24b5e84d17929744a413229eaedb1a9f03))
* **optimizer:** avoid double add_prefix calls ([d503218](https://github.com/SEO7077/strawberry-django-plus/commit/d503218f2337809a4fdfacb0d17825c59e8659fe))
* pass headers further on TestClient ([f8a05e8](https://github.com/SEO7077/strawberry-django-plus/commit/f8a05e88ce309b2213171a8460b6f7aedc47763a)), closes [#224](https://github.com/SEO7077/strawberry-django-plus/issues/224)
* pass the correct model to many to many input items ([d22da73](https://github.com/SEO7077/strawberry-django-plus/commit/d22da7377721d5ef7f6d8d68307cc6abe9c1aa87))
* Prevent a circular import issue that might happen in some setups ([eb7392b](https://github.com/SEO7077/strawberry-django-plus/commit/eb7392b2e5569719539b61bfb125dcd49f1e692b))
* properly optimize nested fragments ([d9faa47](https://github.com/SEO7077/strawberry-django-plus/commit/d9faa47a7fa22a7c72fb5689933e87b7491ff224)), closes [#203](https://github.com/SEO7077/strawberry-django-plus/issues/203)
* pyright detected type issues ([e838473](https://github.com/SEO7077/strawberry-django-plus/commit/e8384731665131356f7ecbaaa655c72a9fa9bc40))
* pyright issue ([9a3257e](https://github.com/SEO7077/strawberry-django-plus/commit/9a3257e4f5e17a3d881e88ef8a70a73e62b3d14b))
* pyright tests should also not install debug-toolbar extras ([8edca6d](https://github.com/SEO7077/strawberry-django-plus/commit/8edca6d973b14ca8684e41fd4e42743281f88043))
* **pyright:** solve some issues from the newest pyright version ([df93ada](https://github.com/SEO7077/strawberry-django-plus/commit/df93adae97d31bf189dc79ce610e8a26d1334a0e))
* regenerate whole schema ([85996df](https://github.com/SEO7077/strawberry-django-plus/commit/85996df04686235fe809ba06586f670abf764cf3))
* **relay:** fix support for custom resolvers returning generators ([1aab2ac](https://github.com/SEO7077/strawberry-django-plus/commit/1aab2ac19790b8802c3b7acd5e50a24087eacb35))
* **relay:** use the type's defined resolve_id when it defines one ([710855e](https://github.com/SEO7077/strawberry-django-plus/commit/710855eb03049bc4f1c423af6681e9c6ce684a62))
* Remove print statement left behind ([dd0d71f](https://github.com/SEO7077/strawberry-django-plus/commit/dd0d71f91c29ab13692adbbe6c7158e41fb102f3))
* Resolve `LazyType` when retrieving the node type ([c01678f](https://github.com/SEO7077/strawberry-django-plus/commit/c01678ff0c7715d20dc23d458bd77a8f3ac17c68)), closes [#116](https://github.com/SEO7077/strawberry-django-plus/issues/116)
* run mkdocs with poetry ([92bd473](https://github.com/SEO7077/strawberry-django-plus/commit/92bd47372612dee218e7491129672c84beb6cdab))
* store auto enum in model field hidden attr to avoid duplication in schema ([e8a727c](https://github.com/SEO7077/strawberry-django-plus/commit/e8a727c6ec4cd5495ece4efb8b86b3e1b1013b2f))
* Strawberry 0.133.1+ expects the default factory to be MISSING instead of a lambda that returns UNSET ([b6fdd72](https://github.com/SEO7077/strawberry-django-plus/commit/b6fdd729adb67ffdf50cb645e84ae7a3f7140786))
* strawberry.ID cannot be used on isinstance ([9517fdd](https://github.com/SEO7077/strawberry-django-plus/commit/9517fdd024971681da90ab533ca079b3d7d67331))
* suffix name with Enum instead of AutoEnum ([368567e](https://github.com/SEO7077/strawberry-django-plus/commit/368567e6f8f7653a6517d8ac90acdc2744b254df))
* **type:** Typo in readme.md ([bb4b93d](https://github.com/SEO7077/strawberry-django-plus/commit/bb4b93d57ee9bf37588c5bd0ed12805ca112c9b3))
* typo in docs ([#261](https://github.com/SEO7077/strawberry-django-plus/issues/261)) ([ae625b2](https://github.com/SEO7077/strawberry-django-plus/commit/ae625b29203f39dc5e5192c9391a38a7a48e8be3))
* update build_filter_kwargs to handle Enums ([aec21ce](https://github.com/SEO7077/strawberry-django-plus/commit/aec21cefce3bc486c9dbd8268c57a1fa93b043de))
* update build_filter_kwargs to handle reverse lookups ([8c8c365](https://github.com/SEO7077/strawberry-django-plus/commit/8c8c365c80c755c0e2c0ffca40a20a20cdc288aa))
* WeakKeyDictionary is not subscriptable in python 3.8 ([8c18222](https://github.com/SEO7077/strawberry-django-plus/commit/8c182221d00e0b62109504e45bcc95126a7f3cfa))
* with dataclass validations ([d4b1b7a](https://github.com/SEO7077/strawberry-django-plus/commit/d4b1b7ac274aafb8b75b8f7c7e8ace1a2aea6b34))
* Workaround a pyright false positive ([3e3610f](https://github.com/SEO7077/strawberry-django-plus/commit/3e3610fc97f67d8fcc01d183c429cca16a6a7d58))
* Workaround adding order/filters in django connections in a thread-safe way ([27124bd](https://github.com/SEO7077/strawberry-django-plus/commit/27124bd2dcf02646ee2253de97aee320346eeaaf))


### Performance

* s/ignore/exclude/ for improved pyright performance ([e725b6b](https://github.com/SEO7077/strawberry-django-plus/commit/e725b6b1129e21fd40e2cf676da483df019bfb24))


### Documentation

* add a "Migration guide" section explaning how to migrate from v2 to v3 ([e9ffdf1](https://github.com/SEO7077/strawberry-django-plus/commit/e9ffdf11e2d9dc3a6a98bee4222a8d890027faa4))
* add a note regarding debug-toolbar integration removal ([59bae30](https://github.com/SEO7077/strawberry-django-plus/commit/59bae3019b0c5aa2704a069e3a4e456293dbe9b2))
* Break the docs line in the README ([873af98](https://github.com/SEO7077/strawberry-django-plus/commit/873af98592bda336995ae9d5cf132f1512cd0720))
* document id_attr ([2ce30c0](https://github.com/SEO7077/strawberry-django-plus/commit/2ce30c0d6d53da1cb6682dbf2ce6fdd8ff5be7d6))
* fix a typo in the CHANGELOG ([fedab8e](https://github.com/SEO7077/strawberry-django-plus/commit/fedab8e449d6a926f530e10543d149304c0a5f05))
* Fix a typo in the docs ([2b99571](https://github.com/SEO7077/strawberry-django-plus/commit/2b99571a0a6bbdf830ef617b281c25547c80fdab))
* fix album related name in docs ([#219](https://github.com/SEO7077/strawberry-django-plus/issues/219)) ([8bb4b6b](https://github.com/SEO7077/strawberry-django-plus/commit/8bb4b6b66b74ebdfa77ade6be9233d5ff9c07671))
* fixes 2 typos in docs ([#227](https://github.com/SEO7077/strawberry-django-plus/issues/227)) ([920f5fb](https://github.com/SEO7077/strawberry-django-plus/commit/920f5fbae8e7fe1d6cea9f6e012b0119b83ff5a2))
* Some improvements to docs ([459993e](https://github.com/SEO7077/strawberry-django-plus/commit/459993e0957ec9f9e8a3b0d5ca5906736435e496))
* Update link to mutations documentation ([3a3dc08](https://github.com/SEO7077/strawberry-django-plus/commit/3a3dc08aa1adea4acdefbd66a84021d651712f9d))


### Code Refactoring

* demo mutation cleaning ([8c9f599](https://github.com/SEO7077/strawberry-django-plus/commit/8c9f599d70e6a595a88d2e1696210095439d04a2))
* Disable only optimization on mutations and subscriptions ([dd38b6a](https://github.com/SEO7077/strawberry-django-plus/commit/dd38b6ac75d7a4d2bac84fe0abb74c99dc9ba748))
* Do not make total_count mandatory anymore ([c91bf5e](https://github.com/SEO7077/strawberry-django-plus/commit/c91bf5e669882b9e3079fe713eb8dafe02aab8e3))
* fix assertionerror when registering copied generic types on schema directives ([#238](https://github.com/SEO7077/strawberry-django-plus/issues/238)) ([d56fc20](https://github.com/SEO7077/strawberry-django-plus/commit/d56fc20858a2284ea7331826b2cb9c0e1cddbf76))
* fix lint issues ([2d78a9b](https://github.com/SEO7077/strawberry-django-plus/commit/2d78a9b836393bb70700cfc25166178d648400d9))
* Fix schema directive usage after latest changes from strawberry ([2589944](https://github.com/SEO7077/strawberry-django-plus/commit/2589944e987542c5a9f6dd2f890b1f5e8ac68e66))
* migrate relay to strawberry's implementation ([#235](https://github.com/SEO7077/strawberry-django-plus/issues/235)) ([d854547](https://github.com/SEO7077/strawberry-django-plus/commit/d85454733fe6580fc1f1f8224f0db1fd83a10072))
* **pyright:** fix pyright issues ([1aeae53](https://github.com/SEO7077/strawberry-django-plus/commit/1aeae539c7e6b783e01d19903fd1469de0f71292))
* **relay:** use Connection class from the field annotation and also allow a Connection to be returned by the base_resolver ([85c6b6c](https://github.com/SEO7077/strawberry-django-plus/commit/85c6b6ce276c08549de4cdedfe630f300dcac478))
* remove hard dependencies on contenttypes and auth framework ([#250](https://github.com/SEO7077/strawberry-django-plus/issues/250)) ([c3329de](https://github.com/SEO7077/strawberry-django-plus/commit/c3329de6e2720e26c1455d364626621d432dc710))
* remove model useless transaction and test ([4e678de](https://github.com/SEO7077/strawberry-django-plus/commit/4e678de009d867e371ff38f1b6a5b934ffe3df10))
* Remove monkey patches from django debug toolbar as it was released in its latest version ([2654c4e](https://github.com/SEO7077/strawberry-django-plus/commit/2654c4ec965d47e8737932b645774ca32bab6d19))
* Simplify aio.resolver ([d8f66f0](https://github.com/SEO7077/strawberry-django-plus/commit/d8f66f013871426f53b1b78e43f86a2211e0fd9d))
* simplify Node methods injection code ([2b1b259](https://github.com/SEO7077/strawberry-django-plus/commit/2b1b259da556022af847bf7f16f9d92c817180b0))
* support for strawberry 0.187.5+ ([6ec1de5](https://github.com/SEO7077/strawberry-django-plus/commit/6ec1de51a0094097406cae49c55dda15572a7742))
* use dataclass_transform from typing_extensions ([#236](https://github.com/SEO7077/strawberry-django-plus/issues/236)) ([2ca669c](https://github.com/SEO7077/strawberry-django-plus/commit/2ca669c5fc0b6597f7000f79fd87c6058311f3b9))
* Use print_schema from strawberry as it can now print schema directives correctly ([e751031](https://github.com/SEO7077/strawberry-django-plus/commit/e7510314050faff3f6682ccf03ee564d41f91171))
* use the new extension style using ([c5c521c](https://github.com/SEO7077/strawberry-django-plus/commit/c5c521c2213e324364d22b8b2e93f7cfe54518f3)), closes [#180](https://github.com/SEO7077/strawberry-django-plus/issues/180)


### Tests

* add full_clean kwargs tests ([05ab860](https://github.com/SEO7077/strawberry-django-plus/commit/05ab86096fc2fb5f15f1b45d253d54ffd52e0a29))
* Enable some extra pyright checkings and fix found issues ([af4febf](https://github.com/SEO7077/strawberry-django-plus/commit/af4febf9ccc9331761cacadb979bf2f993539fa2))
* Fix pyright issues ([f5eff94](https://github.com/SEO7077/strawberry-django-plus/commit/f5eff94e97ac4d6f0767723d616cac02efe00ec4))
* Fix pyright issues ([e01c19c](https://github.com/SEO7077/strawberry-django-plus/commit/e01c19c0ee7dd4f1a9b871b61ae21e5441664606))
* Fix pyright issues ([9288494](https://github.com/SEO7077/strawberry-django-plus/commit/92884940af66e81e14283b352f462670e1d42eb7))
* Fix pyright issues ([7153927](https://github.com/SEO7077/strawberry-django-plus/commit/71539274538d3aa06950cf310586d47a43e6e720))
* Workaround some pyright regressions ([a6ce324](https://github.com/SEO7077/strawberry-django-plus/commit/a6ce324a3c20cdbe89cd5f22401b90f5d2265730))


### Build System

* Bump typing-extensions requirement to 4.2.0+ ([4a9d801](https://github.com/SEO7077/strawberry-django-plus/commit/4a9d80123ca9d95d2fd452b16cf17ac05b256e4e))


### Continuous Integration

* add bootstrap-sha for release-please ([2ac69de](https://github.com/SEO7077/strawberry-django-plus/commit/2ac69deb69daca517387633cfcce1efbcaf47527))
* also run release actions for release branches ([6fe03cb](https://github.com/SEO7077/strawberry-django-plus/commit/6fe03cb7f53df0e8f549ad3f4bf74856e0ccab44))
* fix tests breaking due to not having a "debug-toolbar" extra anymore ([c87609f](https://github.com/SEO7077/strawberry-django-plus/commit/c87609f8d53bff28de944a5425cabc91a6046441))
* make sure release-please create release PRs for release branches ([249c28c](https://github.com/SEO7077/strawberry-django-plus/commit/249c28c529d25c87a58fb82d29f5505f4fc22416))


### Miscellaneous

* Add cache for github actions ([de21bd0](https://github.com/SEO7077/strawberry-django-plus/commit/de21bd0ebb7f5549478cf99791898e8e3b74d66f))
* Add python 3.11 to the list of supported python versions ([c75d511](https://github.com/SEO7077/strawberry-django-plus/commit/c75d5111aad59d993a751f646d51168429a91e93))
* Bump strawberry-graphql-django version requirement and remove the not needed anymore auto monkey patch ([906a643](https://github.com/SEO7077/strawberry-django-plus/commit/906a6431d695b45ff3cf7b98bbe78ace689eb919))
* Bump to version 1.10 ([7401040](https://github.com/SEO7077/strawberry-django-plus/commit/74010405bf804276e848bd7aff6d4b85b6f5ebf8))
* Bump to version 1.10.1 ([e3383b2](https://github.com/SEO7077/strawberry-django-plus/commit/e3383b2cbe3408034937686d657bff12407e6330))
* Bump to version 1.10.3 ([f2c74ab](https://github.com/SEO7077/strawberry-django-plus/commit/f2c74abbf63d57ac319968b19971d407760f9e63))
* Bump to version 1.11 ([32e51d6](https://github.com/SEO7077/strawberry-django-plus/commit/32e51d66b6a3838890d0bb7e5fc5c5fe43299093))
* Bump to version 1.11.2 ([a98e176](https://github.com/SEO7077/strawberry-django-plus/commit/a98e176d47e6aba57c38515fb6ee8d8578109d5f))
* Bump to version 1.13 ([5c3cc12](https://github.com/SEO7077/strawberry-django-plus/commit/5c3cc12d5a921e3a94b0037c085d85268edf2062))
* Bump to version 1.13.2 ([118c106](https://github.com/SEO7077/strawberry-django-plus/commit/118c106894b86940f21131661d87628edfe277d2))
* Bump to version 1.14.1 ([2750a3b](https://github.com/SEO7077/strawberry-django-plus/commit/2750a3b358d81439f38f2f8ffcc4ddf5c85ca470))
* Bump to version 1.14.2 ([e58ba50](https://github.com/SEO7077/strawberry-django-plus/commit/e58ba50396c4492acdb3e5ed540e6b79cc5e4dcc))
* Bump to version 1.15 ([b0921dc](https://github.com/SEO7077/strawberry-django-plus/commit/b0921dc94909c6d19c5c1fca259a035c4e2a6e59))
* Bump to version 1.17.0 ([2bf0e47](https://github.com/SEO7077/strawberry-django-plus/commit/2bf0e47c13f3ebfc8838ee2a006681ad97b44ba2))
* Bump to version 1.19 ([d2920a0](https://github.com/SEO7077/strawberry-django-plus/commit/d2920a04bef87372190171d30dbdf1e4cd1398a6))
* Bump to version 1.20 ([f316a45](https://github.com/SEO7077/strawberry-django-plus/commit/f316a45e7d4d0a45740a802a9659b9c86b6cc8fe))
* Bump to version 1.21 ([642927a](https://github.com/SEO7077/strawberry-django-plus/commit/642927ae1db87e0fea599e81f90111c835c7af96))
* Bump to version 1.23 ([15c7d3b](https://github.com/SEO7077/strawberry-django-plus/commit/15c7d3b3315dba5c44316476a310d3bf125bb2e7))
* Bump to version 1.24 ([89e077c](https://github.com/SEO7077/strawberry-django-plus/commit/89e077cb78a50f878a68e307ece50431a5eb098b))
* Bump to version 1.25 ([e3ed18e](https://github.com/SEO7077/strawberry-django-plus/commit/e3ed18e3f3cb62c371087ce7a30867ea17ee08c3))
* Bump to version 1.26.1 ([cf6da1f](https://github.com/SEO7077/strawberry-django-plus/commit/cf6da1f812254a9860fafd6dbc25d039b453feb8))
* Bump to version 1.27 ([85aeab9](https://github.com/SEO7077/strawberry-django-plus/commit/85aeab9688256ef6bc1662a546676167baa20c3d))
* Bump to version 1.28.1 ([4e355f1](https://github.com/SEO7077/strawberry-django-plus/commit/4e355f174618ad0f2b21083bb785ee222b6b2367))
* Bump to version 1.28.2 ([2db7141](https://github.com/SEO7077/strawberry-django-plus/commit/2db71419b1f1f2b6b4f2af020d2a8dacfbac5c5c))
* Bump to version 1.28.3 ([1f1c8d3](https://github.com/SEO7077/strawberry-django-plus/commit/1f1c8d3e5da2891a5d12807499e9828d8d11443b))
* Bump to version 1.28.6 ([0b5a426](https://github.com/SEO7077/strawberry-django-plus/commit/0b5a426b1091244745a94c3eb8259ad75e03e3ad))
* Bump to version 1.9 ([87260b8](https://github.com/SEO7077/strawberry-django-plus/commit/87260b827434e39c8f49867774b0ee9ac6890700))
* Bump to verssion 1.28.4 ([2b12bcc](https://github.com/SEO7077/strawberry-django-plus/commit/2b12bcc1c95c6182779f213e5fb0d859956efaf7))
* Bump version to 1.25.2 ([3356170](https://github.com/SEO7077/strawberry-django-plus/commit/33561703335a8ab3a0b904767bd384f78b658cf1))
* **deps-dev:** bump ipython from 8.9.0 to 8.10.0 ([1f63a09](https://github.com/SEO7077/strawberry-django-plus/commit/1f63a09aa0e386c72779dcd858c99d38a0aa6493))
* **deps-dev:** bump pymdown-extensions from 9.11 to 10.0 ([0d9f62e](https://github.com/SEO7077/strawberry-django-plus/commit/0d9f62ea7003d4232885ce5eb40dd5cfdc21c160))
* **deps:** bump django from 4.2 to 4.2.1 ([52852bd](https://github.com/SEO7077/strawberry-django-plus/commit/52852bdb19c89cf8a0d2943b2b819cbae3233cd1))
* **deps:** bump requests from 2.30.0 to 2.31.0 ([4a3c846](https://github.com/SEO7077/strawberry-django-plus/commit/4a3c8463e085c4b06487a75d3df18056a44a1cc4))
* **deps:** mark strawberry-graphql-django 0.10.0+ as not compatible ([733bfb1](https://github.com/SEO7077/strawberry-django-plus/commit/733bfb1c53706662a5980783456a25bd9b07d948))
* **deps:** update dependencies and fix style issues ([e076bab](https://github.com/SEO7077/strawberry-django-plus/commit/e076bab21829d4f461e526fb38c2d385b0da3bb8))
* **deps:** update dev dependencies ([26b472a](https://github.com/SEO7077/strawberry-django-plus/commit/26b472a2acaa88e5fa8578cb3c6961087f678745))
* **deps:** update dev dependencies ([eb2fa77](https://github.com/SEO7077/strawberry-django-plus/commit/eb2fa7723c4aa645f3b4d02e8903e9d3934b9e24))
* **deps:** update dev dependencies and enable more ruff rules ([3182d99](https://github.com/SEO7077/strawberry-django-plus/commit/3182d991f6e286db3c2b3a131fca6206f659f3ee))
* Disable reportUninitializedInstanceVariable for now as it is bugged in pyright ([2527233](https://github.com/SEO7077/strawberry-django-plus/commit/25272330f899b79f71d8435b2ae5ed3913257413))
* Enable extra pyright check ([2ec0f9a](https://github.com/SEO7077/strawberry-django-plus/commit/2ec0f9a76b14de8c0663cbcf3a5665c1244f3502))
* enable more ruff rules ([d29fa22](https://github.com/SEO7077/strawberry-django-plus/commit/d29fa2269ea834b4bbf5aed4361495901c210257))
* Fix typing issues from latest pyright version ([45108b9](https://github.com/SEO7077/strawberry-django-plus/commit/45108b90be112d3a3c669af0afc8d1a5589b51b2))
* Improve typing ([6dc8e40](https://github.com/SEO7077/strawberry-django-plus/commit/6dc8e40928f6bfa65f184a1c5dc36c61163ae142))
* Install extras when running tests ([1e687cc](https://github.com/SEO7077/strawberry-django-plus/commit/1e687ccaf3b755241c6519db9490a70e514f121a))
* **main:** release 2.5.0 ([2a94283](https://github.com/SEO7077/strawberry-django-plus/commit/2a942839b523bdd72797eb47547a49ff02db43d5))
* **main:** release 2.6.0 ([#218](https://github.com/SEO7077/strawberry-django-plus/issues/218)) ([d12d517](https://github.com/SEO7077/strawberry-django-plus/commit/d12d5173358798075d831cb097676622196975ae))
* **main:** release 2.6.1 ([#220](https://github.com/SEO7077/strawberry-django-plus/issues/220)) ([7623700](https://github.com/SEO7077/strawberry-django-plus/commit/7623700b41a77c29e4a22c1555358d88ff49b024))
* **main:** release 2.6.2 ([#228](https://github.com/SEO7077/strawberry-django-plus/issues/228)) ([7d44d94](https://github.com/SEO7077/strawberry-django-plus/commit/7d44d94f5698edaea8b8c7246679cb54d4eef36b))
* **main:** release 2.6.3 ([#232](https://github.com/SEO7077/strawberry-django-plus/issues/232)) ([56aa27d](https://github.com/SEO7077/strawberry-django-plus/commit/56aa27d71bd99195c07629e4f91a40563d869f8b))
* **main:** release 2.6.4 ([#239](https://github.com/SEO7077/strawberry-django-plus/issues/239)) ([a726e65](https://github.com/SEO7077/strawberry-django-plus/commit/a726e6581dfac569b9e8a798bd83df2103c4033f))
* **main:** release 3.0.0 ([#240](https://github.com/SEO7077/strawberry-django-plus/issues/240)) ([c601398](https://github.com/SEO7077/strawberry-django-plus/commit/c6013985a384db999d085499d8ed08add4895729))
* **main:** release 3.0.1 ([#241](https://github.com/SEO7077/strawberry-django-plus/issues/241)) ([f53bf89](https://github.com/SEO7077/strawberry-django-plus/commit/f53bf894f7de3fcbefdab939b566ef91ff7594c5))
* **main:** release 3.0.2 ([#251](https://github.com/SEO7077/strawberry-django-plus/issues/251)) ([031adb1](https://github.com/SEO7077/strawberry-django-plus/commit/031adb1809e656004f15c3b653b29ef292f29cec))
* **main:** release 3.0.3 ([#253](https://github.com/SEO7077/strawberry-django-plus/issues/253)) ([e9a4b59](https://github.com/SEO7077/strawberry-django-plus/commit/e9a4b5900bea8abf94602f19c717df5984a993c1))
* **main:** release 3.1.0 ([#257](https://github.com/SEO7077/strawberry-django-plus/issues/257)) ([e720dbf](https://github.com/SEO7077/strawberry-django-plus/commit/e720dbf6f184f59575921d90f555dca3f42ea118))
* **main:** release 3.1.1 ([#262](https://github.com/SEO7077/strawberry-django-plus/issues/262)) ([22805b4](https://github.com/SEO7077/strawberry-django-plus/commit/22805b452220b62b3074030f6968af137c9fd1c2))
* migrate to ruff for linting ([5265dea](https://github.com/SEO7077/strawberry-django-plus/commit/5265deae44a510ab3ffee2c03c300f96e374bde3))
* modernize CI/CD scripts and use release-please for releases ([a908625](https://github.com/SEO7077/strawberry-django-plus/commit/a908625ee9da0fcbab2e3ff6eab931ab4ac61cb1))
* **pyright:** fix pyright issues ([b640c21](https://github.com/SEO7077/strawberry-django-plus/commit/b640c211986ccf29219765cafc37fe67f748e3b6))
* Release 1.30 ([84f76e0](https://github.com/SEO7077/strawberry-django-plus/commit/84f76e0ab1c459ad529136b395cb1d23a6c6dc64))
* Release 1.30.1 ([8057d62](https://github.com/SEO7077/strawberry-django-plus/commit/8057d62c38eb33c95fc035454441a961f93034f5))
* Release 1.31 ([5f75385](https://github.com/SEO7077/strawberry-django-plus/commit/5f75385434b3cea7329c91f24f3b8cc9f84d4312))
* Release 1.32 ([4430b8e](https://github.com/SEO7077/strawberry-django-plus/commit/4430b8e1c93381c45d26feb4437c90d95dc33f37))
* Release 1.32.1 ([ad62311](https://github.com/SEO7077/strawberry-django-plus/commit/ad62311151039c4792bdac1bac7b1865f5932d7a))
* Release 1.32.2 ([2ed34a3](https://github.com/SEO7077/strawberry-django-plus/commit/2ed34a3334cfae63e0f7f91b6aa6d065be467bde))
* Release 1.32.3 ([429e7f3](https://github.com/SEO7077/strawberry-django-plus/commit/429e7f3d745d462d68f7036dbfb27306aed8f475))
* Release 1.33.2 ([4c21439](https://github.com/SEO7077/strawberry-django-plus/commit/4c21439ec86459c1ee23183ac07c48b77649b5c8))
* Release 1.34 ([e584a2d](https://github.com/SEO7077/strawberry-django-plus/commit/e584a2d39beafef852990610d4e1369305d73bbd))
* release 2.0.4 ([fc2969a](https://github.com/SEO7077/strawberry-django-plus/commit/fc2969ae51d13d479a7cfa8c49f12674bd778f58))
* release 2.0.5 ([6ce3d50](https://github.com/SEO7077/strawberry-django-plus/commit/6ce3d5047bc486723fa9e081e3ec9cdb5722056c))
* release 2.0.6 ([739783f](https://github.com/SEO7077/strawberry-django-plus/commit/739783f289cb177b0abc05d14cd38fd202aae93a))
* release 2.1.0 ([7601d31](https://github.com/SEO7077/strawberry-django-plus/commit/7601d31306fdd8d6f2814bb0188005b4451ffb20))
* release 2.2.0 ([65403e2](https://github.com/SEO7077/strawberry-django-plus/commit/65403e2d8f2d926172cda1579abd91f81d259d30))
* release 2.3.0 ([6d9115b](https://github.com/SEO7077/strawberry-django-plus/commit/6d9115bb6f3052e1f7b6e1c59b05c52e1b78f952))
* release 2.3.1 ([cb00f0c](https://github.com/SEO7077/strawberry-django-plus/commit/cb00f0cb3f254e5ffa08e1373332b9a7daa1095c))
* **release:** bump to version 2.0.0 ([cd68852](https://github.com/SEO7077/strawberry-django-plus/commit/cd688527884839febe9b93513a6f8352e94c8e62))
* **release:** bump to version 2.0.1 ([9172d3a](https://github.com/SEO7077/strawberry-django-plus/commit/9172d3a6e74fc4c04ac9f1e488a7533da101db28))
* Remove an unnecessary "type:ignore" comment ([4562aff](https://github.com/SEO7077/strawberry-django-plus/commit/4562aff500fe853fb3e843efaa9f38a72f63e8b0))
* remove semgrep (it takes too long to run) ([32ee6d4](https://github.com/SEO7077/strawberry-django-plus/commit/32ee6d4cba938d55624979f41c5a1f6ac5ae7a99))
* Run pyright on CICD ([29d6569](https://github.com/SEO7077/strawberry-django-plus/commit/29d65694595439c9bab4397aa665efc16c036c69))
* Solve some typing issues from latest pyright version ([6048c68](https://github.com/SEO7077/strawberry-django-plus/commit/6048c680cc468491471869c61f3effda2713888e))
* The main branch was renamed to main ([f2e6d1f](https://github.com/SEO7077/strawberry-django-plus/commit/f2e6d1f72d1caed51985d8bebdbeb8731f37d840))
* Update CICD actions ([691b6be](https://github.com/SEO7077/strawberry-django-plus/commit/691b6bed6690e3f5f33a993fa6207fd53d4b89b6))
* Update dependencies and fix typing issues ([4394dc1](https://github.com/SEO7077/strawberry-django-plus/commit/4394dc153ad88a01fe1c51d240cf144b1c82f5b3))
* update dev dependencies ([2b4e010](https://github.com/SEO7077/strawberry-django-plus/commit/2b4e010ba0ae0ce23524343f5c2ccc55ec414d23))
* Update dev dependencies ([00ee42d](https://github.com/SEO7077/strawberry-django-plus/commit/00ee42d43dd80467204d679e913ba649c3427a90))
* Update dev dependencies ([f08326e](https://github.com/SEO7077/strawberry-django-plus/commit/f08326eb42a0f184eb4124413994b8741bb04bc7))
* Update dev dependencies ([1b84237](https://github.com/SEO7077/strawberry-django-plus/commit/1b842370732f821baccf6ba64ae7978816ed6bbe))
* Update dev dependencies ([7c82082](https://github.com/SEO7077/strawberry-django-plus/commit/7c820828eb4b349f53745b86aac526df7ec49bd7))
* Update dev dependencies ([274233e](https://github.com/SEO7077/strawberry-django-plus/commit/274233ec070bd73e0a8ccba89d0b0ffcfbd352d4))
* Update dev dependencies ([aae277e](https://github.com/SEO7077/strawberry-django-plus/commit/aae277e9a88099a5cef273f8868029472933c51d))
* Update dev dependencies ([27287f1](https://github.com/SEO7077/strawberry-django-plus/commit/27287f1aca4efdf07f64cf6a8c8f0f67a50b621c))
* Update dev dependencies ([5be2275](https://github.com/SEO7077/strawberry-django-plus/commit/5be2275c11dd2ce33f1072dec38477142d449297))
* Update dev dependencies ([57fcf45](https://github.com/SEO7077/strawberry-django-plus/commit/57fcf45645ce1a20ec721e5a09a6aab3dcbf7cca))
* Update dev dependencies ([09c1aea](https://github.com/SEO7077/strawberry-django-plus/commit/09c1aeadc2163b420ab316555a4e1b846ec444ee))
* Update dev dependencies ([7fa3369](https://github.com/SEO7077/strawberry-django-plus/commit/7fa33695db9b3ff9f0704e30fd6435a52414bde7))
* Update dev dependencies and fix pyright issues ([d678683](https://github.com/SEO7077/strawberry-django-plus/commit/d678683b93d4498f11e06627a6bd4c2bdf43ba7d))
* Update dev requirements ([631cbf2](https://github.com/SEO7077/strawberry-django-plus/commit/631cbf2d68c57f540503fb6d9a0561a32becf47d))
* Update dev requirements ([e00ccc0](https://github.com/SEO7077/strawberry-django-plus/commit/e00ccc03a4b53cd800456547470f4b9b83398791))
* Update dev requirements ([4dd529b](https://github.com/SEO7077/strawberry-django-plus/commit/4dd529b1bfdf3b1d41700bce271c4378d8958544))
* Update dev requirements ([f52da23](https://github.com/SEO7077/strawberry-django-plus/commit/f52da23367b154d1235b288b272c7441225e6d21))
* Update dev requirements ([d550c20](https://github.com/SEO7077/strawberry-django-plus/commit/d550c20389479738eb42aaf55073327f5c519fda))
* update poetry.lock ([a3f3f1a](https://github.com/SEO7077/strawberry-django-plus/commit/a3f3f1a268c3f5c0ca760e129942e692b440db3a))

## [3.1.1](https://github.com/blb-ventures/strawberry-django-plus/compare/v3.1.0...v3.1.1) (2023-07-07)


### Bug Fixes

* typo in docs ([#261](https://github.com/blb-ventures/strawberry-django-plus/issues/261)) ([72d43e5](https://github.com/blb-ventures/strawberry-django-plus/commit/72d43e5eac9d0bebe07234010745fd19432d9d1c))


### Miscellaneous

* **deps:** mark strawberry-graphql-django 0.10.0+ as not compatible ([2ee73d7](https://github.com/blb-ventures/strawberry-django-plus/commit/2ee73d70d29ecaef58d6420bc7038464704a4b81))

## [3.1.0](https://github.com/blb-ventures/strawberry-django-plus/compare/v3.0.3...v3.1.0) (2023-07-05)


### Features

* mark this lib as deprecated and add a documentation on how to migrate to strawberry_django ([ed52efe](https://github.com/blb-ventures/strawberry-django-plus/commit/ed52efecc7d492d746466119985947e14b837089))


### Bug Fixes

* allow `field_name` to be passed for node and connections ([dc587c7](https://github.com/blb-ventures/strawberry-django-plus/commit/dc587c7face8f9a8bfe943fd1299b73f4dc9d283))
* also support `auto` when checking for auto annotations ([b5b0141](https://github.com/blb-ventures/strawberry-django-plus/commit/b5b01413e7fdb6ea1ee60cc50134a5904ea38775))

## [3.0.3](https://github.com/blb-ventures/strawberry-django-plus/compare/v3.0.2...v3.0.3) (2023-06-25)


### Bug Fixes

* missing return for the async resolver ([f1dacec](https://github.com/blb-ventures/strawberry-django-plus/commit/f1dacece01c8fccf966aabe6eded828ac5d0e1e2))


### Code Refactoring

* remove hard dependencies on contenttypes and auth framework ([#250](https://github.com/blb-ventures/strawberry-django-plus/issues/250)) ([b9428b0](https://github.com/blb-ventures/strawberry-django-plus/commit/b9428b08eeb8172cebd5423aaf1b39add3a47064))
* simplify Node methods injection code ([127124e](https://github.com/blb-ventures/strawberry-django-plus/commit/127124ee8591c023e010e3097411da397cd9dba2))

## [3.0.2](https://github.com/blb-ventures/strawberry-django-plus/compare/v3.0.1...v3.0.2) (2023-06-23)


### Bug Fixes

* fix a wrongly refactored code from previous commit ([fb0de57](https://github.com/blb-ventures/strawberry-django-plus/commit/fb0de5750dc466da9f14e3a5dc4f95eb3e28a1da))
* fix class inherited fields not being evaluated correctly ([15b2dd8](https://github.com/blb-ventures/strawberry-django-plus/commit/15b2dd83a8a8b606d7455d1817966e7e9315c451)), closes [#247](https://github.com/blb-ventures/strawberry-django-plus/issues/247)
* pyright tests should also not install debug-toolbar extras ([1f8600e](https://github.com/blb-ventures/strawberry-django-plus/commit/1f8600e78c6056255214497ad32728ce2a043ef2))


### Code Refactoring

* support for strawberry 0.187.5+ ([493a1ad](https://github.com/blb-ventures/strawberry-django-plus/commit/493a1ad69d1ab12562bf5d35ff34c2b8716ddf01))


### Continuous Integration

* also run release actions for release branches ([6d6c0f7](https://github.com/blb-ventures/strawberry-django-plus/commit/6d6c0f7d21d3ff4796e59b34512a23e1222c2d5e))
* fix tests breaking due to not having a "debug-toolbar" extra anymore ([cd621f5](https://github.com/blb-ventures/strawberry-django-plus/commit/cd621f5bb81f1b6bba7d90e44108d049c2645ff7))
* make sure release-please create release PRs for release branches ([c2d1a78](https://github.com/blb-ventures/strawberry-django-plus/commit/c2d1a78d0358962cdd5a0f6f9f1f01c8a821cb60))

## [3.0.1](https://github.com/blb-ventures/strawberry-django-plus/compare/v3.0.0...v3.0.1) (2023-06-17)


### Bug Fixes

* inject filters/order at once to avoid one of them missing also removing the other one ([84f540e](https://github.com/blb-ventures/strawberry-django-plus/commit/84f540ec8fe608a0bf93efb9ed692421f20e1501)), closes [#243](https://github.com/blb-ventures/strawberry-django-plus/issues/243)
* loosen errors for unions of django types when checking for filters/ordering ([4a97839](https://github.com/blb-ventures/strawberry-django-plus/commit/4a97839e7190a32246cc2ea3d5297cf26a2bea37))


### Documentation

* fix a typo in the CHANGELOG ([f54507e](https://github.com/blb-ventures/strawberry-django-plus/commit/f54507e485d5ad831d71a5a01bd06be09de7300b))

## [3.0.0](https://github.com/blb-ventures/strawberry-django-plus/compare/v2.6.4...v3.0.0) (2023-06-15)


### ⚠ BREAKING CHANGES

* remove debug toolbar integration
* migrate relay to strawberry's implementation ([#235](https://github.com/blb-ventures/strawberry-django-plus/issues/235))

### Features

* remove debug toolbar integration ([463578a](https://github.com/blb-ventures/strawberry-django-plus/commit/463578a119535ec4a3b4df12d2c3d9d1e4c1c53e))


### Code Refactoring

* migrate relay to strawberry's implementation ([#235](https://github.com/blb-ventures/strawberry-django-plus/issues/235)) ([d55f199](https://github.com/blb-ventures/strawberry-django-plus/commit/d55f199de01aaa7c85e7ad12ab2e86ea274ca124))


### Documentation

* add a "Migration guide" section explaining how to migrate from v2 to v3 ([3a1acbb](https://github.com/blb-ventures/strawberry-django-plus/commit/3a1acbbd1c2e8c8cf544ccab05a006ebea330002))
* add a note regarding debug-toolbar integration removal ([051b585](https://github.com/blb-ventures/strawberry-django-plus/commit/051b5854ba0992558492911129ff6fa29b15c9cb))

## [2.6.4](https://github.com/blb-ventures/strawberry-django-plus/compare/v2.6.3...v2.6.4) (2023-06-14)


### Code Refactoring

* fix assertionerror when registering copied generic types on schema directives ([#238](https://github.com/blb-ventures/strawberry-django-plus/issues/238)) ([250da52](https://github.com/blb-ventures/strawberry-django-plus/commit/250da52c48ea17daa756bd12b3babd1b2e050628))

## [2.6.3](https://github.com/blb-ventures/strawberry-django-plus/compare/v2.6.2...v2.6.3) (2023-06-14)


### Miscellaneous

* **pyright:** fix pyright issues ([abacca4](https://github.com/blb-ventures/strawberry-django-plus/commit/abacca48ae17ec33a86dcc948e8d2d4ed62e0fe0))


### Code Refactoring

* use dataclass_transform from typing_extensions ([#236](https://github.com/blb-ventures/strawberry-django-plus/issues/236)) ([47a194e](https://github.com/blb-ventures/strawberry-django-plus/commit/47a194e07a9aa14dad05dcab42557a92c0a860d2))

## [2.6.2](https://github.com/blb-ventures/strawberry-django-plus/compare/v2.6.1...v2.6.2) (2023-06-07)


### Bug Fixes

* do not try to merge fragments, they have no name ([efa0cb4](https://github.com/blb-ventures/strawberry-django-plus/commit/efa0cb4c4cacc24b4cd4091cb5b1cce203bc7a78))


### Documentation

* fixes 2 typos in docs ([#227](https://github.com/blb-ventures/strawberry-django-plus/issues/227)) ([07bb59a](https://github.com/blb-ventures/strawberry-django-plus/commit/07bb59a48586e5737fc7b725e414c7461bdaaebb))


### Miscellaneous

* **deps:** update dev dependencies ([3ab7c91](https://github.com/blb-ventures/strawberry-django-plus/commit/3ab7c91b2431515b00d025cc2d8cf57efd989884))

## [2.6.1](https://github.com/blb-ventures/strawberry-django-plus/compare/v2.6.0...v2.6.1) (2023-06-05)


### Bug Fixes

* allow connections to be typed as unions ([698b854](https://github.com/blb-ventures/strawberry-django-plus/commit/698b854b03ba58eaa3af84074ca6504732bf52d9)), closes [#223](https://github.com/blb-ventures/strawberry-django-plus/issues/223)
* pass headers further on TestClient ([39dc5ac](https://github.com/blb-ventures/strawberry-django-plus/commit/39dc5acb1c64c45bffc07653a0ce5e0ce3f45b13)), closes [#224](https://github.com/blb-ventures/strawberry-django-plus/issues/224)


### Documentation

* fix album related name in docs ([#219](https://github.com/blb-ventures/strawberry-django-plus/issues/219)) ([6d120d3](https://github.com/blb-ventures/strawberry-django-plus/commit/6d120d3eb445d16bd24663c05fdf7471d14e38e2))

## [2.6.0](https://github.com/blb-ventures/strawberry-django-plus/compare/v2.5.0...v2.6.0) (2023-06-01)


### Features

* add description to enums from django choices ([#217](https://github.com/blb-ventures/strawberry-django-plus/issues/217)) ([4d640e7](https://github.com/blb-ventures/strawberry-django-plus/commit/4d640e7d5cb05ed9bac79743e291121d2a9e56fa))
* use a type's get_queryset for Relay connections if it defines one ([#215](https://github.com/blb-ventures/strawberry-django-plus/issues/215)) ([bb3af76](https://github.com/blb-ventures/strawberry-django-plus/commit/bb3af7675a175fc3b85eedef54464198d38613da))

## [2.5.0](https://github.com/blb-ventures/strawberry-django-plus/compare/v2.4.2...v2.5.0) (2023-05-29)


### Features

* expose `__version__` on the package ([de71277](https://github.com/blb-ventures/strawberry-django-plus/commit/de71277624f6537e3ad0a1552f12718cadba2e4d))
* **optimizer:** support custom QS for prefetches ([e7ae685](https://github.com/blb-ventures/strawberry-django-plus/commit/e7ae6855a62f882ce979dcc8368701ebe88f9c80))


### Bug Fixes

* fix django versioning on test actions ([7c59081](https://github.com/blb-ventures/strawberry-django-plus/commit/7c59081c954ecdba72ae1d6b204d710282d8f3ff))
* fix LICENSE author ([b3fa178](https://github.com/blb-ventures/strawberry-django-plus/commit/b3fa178978dfad7004f50f73f59e761dfbf1c100))
* fix missing checkout version ([147e41d](https://github.com/blb-ventures/strawberry-django-plus/commit/147e41d7063fdda01913810f79c51edaada2e868))
* run mkdocs with poetry ([7155e3a](https://github.com/blb-ventures/strawberry-django-plus/commit/7155e3aaa646d13612fc3754c0c1ce5bd8813669))


### Miscellaneous

* **deps:** bump requests from 2.30.0 to 2.31.0 ([f254a3b](https://github.com/blb-ventures/strawberry-django-plus/commit/f254a3b567b8953c5ef9350d77f4fa58e6eefd8c))
* **deps:** update dev dependencies ([cbfd781](https://github.com/blb-ventures/strawberry-django-plus/commit/cbfd78168bfee0966f9e018700b12216be13518f))
* modernize CI/CD scripts and use release-please for releases ([b6ec168](https://github.com/blb-ventures/strawberry-django-plus/commit/b6ec16879078379a88f68a6ec8633cf02e78c296))


### Continuous Integration

* add bootstrap-sha for release-please ([4a1a534](https://github.com/blb-ventures/strawberry-django-plus/commit/4a1a534fa6dbe6a119b2d89c6728f7808c5f78fc))
