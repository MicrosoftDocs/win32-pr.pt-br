---
title: Lendo o esquema abstrato
description: Este tópico fornece um exemplo de código e diretrizes para leitura do esquema abstrato, que fornece um subconjunto dos dados armazenados nos objetos attributeSchema e classSchema no contêiner de esquema.
ms.assetid: f31fc0ae-048f-413c-9370-96367dc68df8
ms.tgt_platform: multiple
keywords:
- Active Directory de esquema, lendo o esquema abstrato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7095dc4fb5ffe5f11f64781ecd423a60b3d434d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881308"
---
# <a name="reading-the-abstract-schema"></a>Lendo o esquema abstrato

Este tópico fornece um exemplo de código e diretrizes para leitura do esquema abstrato, que fornece um subconjunto dos dados armazenados nos objetos **attributeSchema** e **classSchema** no contêiner de esquema. Para recuperar dados que não estão disponíveis no esquema abstrato, leia os dados diretamente do contêiner de esquema, conforme descrito em [lendo objetos attributeSchema e classSchema](reading-attributeschema-and-classschema-objects.md).

Use a cadeia de vinculação "LDAP://schema" para associar a um ponteiro [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) no esquema abstrato. Use esse ponteiro para enumerar as entradas de classe, atributo e sintaxe no esquema abstrato. Você também pode usar o método [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) para recuperar entradas individuais.


```C++
// Bind to the abstract schema.
IADsContainer *pAbsSchema = NULL;
hr = ADsGetObject(L"LDAP://schema",
                  IID_IADsContainer,
                  (void**)&pAbsSchema);
```




```VB
' Bind to the abstract schema.
Dim adschema As IADsContainer
Set adschema = GetObject("LDAP://schema")
```



Use uma cadeia de vinculação semelhante, "LDAP://schema/ &lt; Object &gt; ", para associar diretamente a uma classe ou a uma entrada de atributo no esquema abstrato. Nessa cadeia de caracteres, " &lt; Object &gt; " é o **lDAPDisplayName** de uma classe ou atributo. Para classes, associe-se à interface [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) ; para atributos, associe à interface [**iadsproperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) .


```C++
// Bind to the user class entry in the abstract schema.
IADsClass *pClass;
hr = ADsGetObject(L"LDAP://schema/user",
                  IID_IADsClass,
                  (void**)&pClass);
```




```VB
Bind to the user class entry in the abstract schema.
Dim userclass As IADsClass
Set userclass = GetObject("LDAP://schema/user")
```



Além disso, a interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) fornece a propriedade [**IADs. Schema**](/windows/desktop/ADSI/iads-property-methods) . Essa propriedade retorna o ADsPath para a classe de objeto no formato de cadeia de vinculação de esquema abstrato. Se você tiver um ponteiro **IADs** para um objeto, poderá associar a sua classe no esquema abstrato usando o ADsPath retornado de **IADs. Schema**.

Para classes, a tabela a seguir lista as principais propriedades fornecidas pelo esquema abstrato.



| Propriedade                                                             | Significado                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsClass. Abstract**](/windows/desktop/ADSI/iadsclass-property-methods)            | Indica se esta é uma classe abstrata.                                                                                                                                                                                                                                            |
| [**IADsClass. auxiliar**](/windows/desktop/ADSI/iadsclass-property-methods)           | Indica se esta é uma classe auxiliar.                                                                                                                                                                                                                                           |
| [**IADsClass.AuxDerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)      | Matriz de classes auxiliares da qual essa classe deriva.                                                                                                                                                                                                                                     |
| [**IADsClass. Container**](/windows/desktop/ADSI/iadsclass-property-methods)           | Indica se os objetos dessa classe podem conter outros objetos, o que será verdadeiro se qualquer classe incluir essa classe em sua lista de **possibleSuperiors**.                                                                                                                                 |
| [**IADsClass.DerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)         | Matriz de classes da qual essa classe é derivada.                                                                                                                                                                                                                                       |
| [**IADsClass. Obrigatórioproperties**](/windows/desktop/ADSI/iadsclass-property-methods) | Recupera uma matriz das propriedades obrigatórias que devem ser definidas para uma instância da classe. A lista retornada inclui todos os valores **mustContain** e **systemMustContain** para a classe e as classes das quais ele é derivado, incluindo as superclasses e as classes auxiliares. |
| [**IADsClass. OID**](/windows/desktop/ADSI/iadsclass-property-methods)                 | Recupera o governsID da classe.                                                                                                                                                                                                                                                   |
| [**IADsClass. OptionalProperties**](/windows/desktop/ADSI/iadsclass-property-methods)  | Recupera uma matriz das propriedades opcionais que podem ser definidas para uma instância da classe. A lista retornada inclui todos os valores **mayContain** e **systemMayContain** para a classe e as classes das quais ele é derivado, incluindo as superclasses e as classes auxiliares.   |
| [**IADsClass.PossibleSuperiors**](/windows/desktop/ADSI/iadsclass-property-methods)   | Recupera uma matriz dos valores de **possibleSuperiors** para a classe, que indica as classes de objeto que podem conter objetos dessa classe.                                                                                                                                        |



 

O esquema abstrato é armazenado no objeto de **subesquema** no contêiner de esquema. Para obter o nome distinto do objeto de **subesquema** , associe-o a RootDSE e leia o atributo **subSchemaSubEntry** , conforme descrito em [associação sem servidor e RootDSE](serverless-binding-and-rootdse.md). Lembre-se de que é mais eficiente ler o esquema abstrato ligando-se a "LDAP://schema", do que associando diretamente ao objeto de **subesquema** .

 

 
