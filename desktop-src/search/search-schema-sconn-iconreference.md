---
description: O <iconReference> elemento opcional especifica um ícone personalizado para esse local. Este elemento não tem atributos nem elementos filho.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: Elemento iconReference (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c181efe3bb8ac04f08d4fa16016d3468af6f10c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501459"
---
# <a name="iconreference-element-search-connector-schema"></a>Elemento iconReference (esquema do conector de pesquisa)

O <iconReference> elemento opcional especifica um ícone personalizado para esse local. Este elemento não tem atributos nem elementos filho.

## <a name="syntax"></a>Syntax


```
<!-- iconReference -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
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

O formato da referência deve ser especificado em um formato adequado para a função [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) : (por exemplo, <dll file name> <icon index> ).

## <a name="example"></a>Exemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 
