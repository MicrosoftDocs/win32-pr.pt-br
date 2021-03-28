---
description: Esse <searchConnectorDescriptionList> elemento contém uma lista de conectores de pesquisa que são mapeados para locais incluídos nesta biblioteca. Cada conector de pesquisa é definido por um <searchConnectorDescription> elemento. Esse elemento é opcional e não tem atributos.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Elemento searchConnectorDescriptionList (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d7295796f205ca0d20f220ba827abfd5470bdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968128"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a>Elemento searchConnectorDescriptionList (esquema de biblioteca)

Esse <searchConnectorDescriptionList> elemento contém uma lista de conectores de pesquisa que são mapeados para locais incluídos nesta biblioteca. Cada conector de pesquisa é definido por um <searchConnectorDescription> elemento. Esse elemento é opcional e não tem atributos.

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

Os conectores de pesquisa para a pesquisa federada do Windows e os escopos do manipulador de protocolo não podem ser incluídos em uma biblioteca.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Esquema de descrição da biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de descrição do conector de pesquisa](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
