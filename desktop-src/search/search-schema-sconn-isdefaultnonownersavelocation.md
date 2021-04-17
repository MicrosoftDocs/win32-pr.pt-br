---
description: O elemento booliano opcional <isDefaultNonOwnerSaveLocation> especifica se o local descrito no conector de pesquisa deve ser usado como o local de salvamento padrão quando um usuário de outro computador em um grupo doméstico opta por salvar um item.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: Elemento isDefaultNonOwnerSaveLocation (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edd39ab76ae1b99d6518ca40407d328f5da9778c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790491"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a>Elemento isDefaultNonOwnerSaveLocation (esquema do conector de pesquisa)

O elemento booliano opcional <isDefaultNonOwnerSaveLocation> especifica se o local descrito no conector de pesquisa deve ser usado como o local de salvamento padrão quando um usuário de outro computador em um grupo doméstico opta por salvar um item. Este elemento não tem elementos filho e nenhum atributo.

## <a name="syntax"></a>Syntax


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                                                                   | Elementos filho |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Comentários

Se for true, quando um usuário de outro computador em um grupo doméstico optar por salvar um item, o Windows Explorer salvará o item no local especificado no <simpleLocation> elemento.

## <a name="example"></a>Exemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



