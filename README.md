# java-parent-pom

this is project for java parent pom which extends [java-root-parent](https://github.com/mikolajmitura/java-root-parent)

it does the same like java-root-parent + download code rules from from [code-style-rules](https://github.com/mikolajmitura/code-style-rules/tree/develop/src/main/resources) 
and run arch-unit-maven-plugin with rules from code-style-rules.

required to override in child pom/project
```xml
       <!-- required to override -->
        <release.project.name>parent pom with checking code style</release.project.name>
        <release.project.description>parent pom with checking code style based on rules from code-style-rules module</release.project.description>
        <release.project.repository-name>java-parent-pom</release.project.repository-name>
        <archunit.package.to.verify>pl.jalokim</archunit.package.to.verify>
```

can be override in child pom/project
```xml
        <!-- not required to override -->
        <code-style-rules.version>RELEASE</code-style-rules.version> 
        <code-style.base-dir>${project.build.directory}/code-style-rules</code-style.base-dir>
```

+  you can override properties from [java-root-parent pom.xml](https://github.com/mikolajmitura/java-root-parent/blob/develop/pom.xml#L19)
