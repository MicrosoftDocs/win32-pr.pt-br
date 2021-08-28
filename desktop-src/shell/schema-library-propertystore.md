---
description: O &lt; &gt; elemento propertyStore especifica um conjunto de uma ou mais propriedades usadas por essa biblioteca. Esse elemento é opcional e não tem atributos.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: Elemento propertyStore (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089e87e6e7bdfa568ffa2e8903f6347cb6dc7b3d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880422"
---
# <a name="propertystore-element-library-schema"></a>Elemento propertyStore (esquema de biblioteca)

O &lt; &gt; elemento propertyStore especifica um conjunto de uma ou mais propriedades usadas por essa biblioteca. Esse elemento é opcional e não tem atributos.

## <a name="syntax"></a>Syntax

``` syntax
<!-- propertyStore -->
<xs:element name="propertyStore" minOccurs="0">
    <xs:complexType>
        <xs:complexContent>
            <!-- properties are extensions of propertyStoreType -->
            <xs:extension base="propertyStoreType"/>        
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                               | Elementos filho                                                   |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) | [Elemento Property (esquema de biblioteca)](schema-library-property.md) |



 

## <a name="remarks"></a>Comentários

O &lt; &gt; elemento propertyStore pode ter um ou mais &lt; &gt; elementos filho de propriedade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Esquema de descrição da biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de descrição do conector de pesquisa](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
