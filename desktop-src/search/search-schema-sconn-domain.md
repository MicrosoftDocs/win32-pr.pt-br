---
description: O <domain> elemento opcional especifica a URL do serviço de pesquisa usado por este conector de pesquisa. Ele é exibido no painel de detalhes. Este elemento não tem elementos filho e nenhum atributo.
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: Elemento Domain (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b57819cf485bccbe63e7560f3fcb92811d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826903"
---
# <a name="domain-element-search-connector-schema"></a>Elemento Domain (esquema do conector de pesquisa)

O <domain> elemento opcional especifica a URL do serviço de pesquisa usado por este conector de pesquisa. Ele é exibido no painel de detalhes. Este elemento não tem elementos filho e nenhum atributo.

## <a name="syntax"></a>Syntax


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
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

A URL deve ser o domínio de nível superior para o provedor de pesquisa. Por exemplo, https://www.example.com.

## <a name="example"></a>Exemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 



