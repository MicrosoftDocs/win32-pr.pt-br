---
description: Esse &lt; elemento searchConnectorDescriptionList contém uma lista de conectores de pesquisa que mapeiam para &gt; locais incluídos nesta biblioteca. Cada conector de pesquisa é definido por um &lt; elemento searchConnectorDescription. &gt; Esse elemento é opcional e não tem atributos.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Elemento searchConnectorDescriptionList (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04edc3a3cb7353529dccca66ffa15e1604bdd1c0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885602"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a>Elemento searchConnectorDescriptionList (esquema de biblioteca)

Esse &lt; elemento searchConnectorDescriptionList contém uma lista de conectores de pesquisa que mapeiam para &gt; locais incluídos nesta biblioteca. Cada conector de pesquisa é definido por um &lt; elemento searchConnectorDescription. &gt; Esse elemento é opcional e não tem atributos.

## <a name="syntax"></a>Syntax

``` syntax
<!-- searchConnectorDescriptionList -->
    <xs:element name="searchConnectorDescriptionList" minOccurs="0">
          <xs:complexType>
            <xs:sequence minOccurs="0">
              <xs:element name="searchConnectorDescription" type="searchConnectorDescriptionType" minOccurs="0" maxOccurs="unbounded"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
```

## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                               | Elementos filho                                                                                       |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) | [Elemento searchConnectorDescription (esquema de biblioteca)](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a>Comentários

Conectores de pesquisa para Windows escopos de manipulador de protocolo e pesquisa federada não podem ser incluídos em uma biblioteca.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Esquema de descrição da biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de descrição do conector de pesquisa](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
