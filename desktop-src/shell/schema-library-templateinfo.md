---
description: O &lt; &gt; elemento templateInfo é um contêiner para o elemento FolderType, que especifica um tipo de pasta para exibir os resultados de uma consulta nessa biblioteca. Esse elemento é opcional e não tem atributos.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Elemento templateInfo (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f55fec64bf7418eef8e70c4cf8fa1ee47006c5f2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885522"
---
# <a name="templateinfo-element-library-schema"></a>Elemento templateInfo (esquema de biblioteca)

O &lt; &gt; elemento templateInfo é um contêiner para o elemento [FolderType](schema-library-foldertype.md) , que especifica um tipo de pasta para exibir os resultados de uma consulta nessa biblioteca. Esse elemento é opcional e não tem atributos.

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

 

 
