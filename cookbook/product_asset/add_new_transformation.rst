How to Add a New Transformation
===============================

Creating a New Transformer
--------------------------

Transformations are classes which allow to transform a media from state A to state B.
For example, in the Product Asset specific case, they transform a Reference (A) to Variations (B).
Each a Variation is a transformation of a Reference.

As Transformations are not specific PIM elements, they are stocked in `\\Akeneo` and not `\\PimEnterprise`.
Then, you can find in `Akeneo\Component\FileTransformer` all business code and in `Akeneo\\Bundle\\FileTransformerBundle` all Symfony2 specific implementation.

Quick view : as Transformation run with the registry pattern, you just have to create your own Transformation implementing `Akeneo\\Component\\FileTransformer\\Transformation\\TransformationInterface` and to register the service in `Akeneo/Bundle/FileTransformerBundle/Resources/config/transformations.yml` with the `akeneo_file_transformer.transformation` tag.

.. note::
    Know more about .. _registry pattern: http://martinfowler.com/eaaCatalog/registry.html

