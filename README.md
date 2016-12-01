# phore-annotations
Wrapper for Doctrine Annotaions


## Create a AnnotationPack

```
class AnnotationPack_Application implements GoAnnotationPack {


        /**
         * Return a Array of Annotation Classnames to be loaded
         *
         * @return string[]
         */
        public function getAnnotationClassNames() {
            return [
                Action::class,
                AllowAll::class,
                Api::class,
                Filter::class,
                Mount::class,
                Parameter::class,
                Requires::class,
                Route::class,
                ContextInit::class
            ];
        }
    }


```

## Register the Pack

```
Annotations::Register(AnnotationPack_Application::class);
```

## Access the Annotations

```
Annotations::ForClass(SomeClass::class);
Annotations::ForMethod(SomeClass::class, "methodName");
Annotations::ForProperty(SomeClass::class, "propertyName");
```

The Annotations returned are Doctrine Annotations
[http://doctrine-project.com]