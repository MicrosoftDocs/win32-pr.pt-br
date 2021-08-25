---
description: O <templateInfo> elemento é um contêiner para o elemento FolderType, que especifica um tipo de pasta para exibir os resultados de uma consulta nessa biblioteca. Esse elemento é opcional e não tem atributos.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Elemento templateInfo (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda0c42e71db2e47335371b51d9dc819620e6b28dfac63ee9c0e2a640ccab0b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942086"
---
# <a name="templateinfo-element-library-schema"></a>Elemento templateInfo (esquema de biblioteca)

O <templateInfo> elemento é um contêiner para o elemento [FolderType](schema-library-foldertype.md) , que especifica um tipo de pasta para exibir os resultados de uma consulta nessa biblioteca. Esse elemento é opcional e não tem atributos.

## <a name="syntax"></a>Syntax

``` syntax
<!-- templateInfo -->
<xs:element name="templateInfo" minOccurs="0">
    <xs:complexType>
        <xs:all>
            <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                               | Elementos filho                                                             |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) | [Elemento FolderType (esquema de biblioteca)](schema-library-foldertype.md)       |
|                                                                              | [Elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Esquema de descrição da biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de descrição do conector de pesquisa](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
