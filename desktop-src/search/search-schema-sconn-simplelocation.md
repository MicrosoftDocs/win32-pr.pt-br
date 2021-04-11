---
description: O <simpleLocation> elemento Especifica o local para os conectores de pesquisa que são baseados em sistema de arquivos ou baseado em manipulador de protocolo. Esse elemento tem dois elementos filho e nenhum atributo.
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: Elemento simpleLocation (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12c17ace36314ceb180f14b6de0eb7a890a385b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296229"
---
# <a name="simplelocation-element-search-connector-schema"></a>Elemento simpleLocation (esquema do conector de pesquisa)

O <simpleLocation> elemento Especifica o local para os conectores de pesquisa que são baseados em sistema de arquivos ou baseado em manipulador de protocolo. Esse elemento tem dois elementos filho e nenhum atributo.

## <a name="syntax"></a>Syntax


```
<!-- simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                                                                   | Elementos filho                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)](search-schema-searchconnectordescription.md) | [Elemento URL simpleLocation (esquema do conector de pesquisa)](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | serializado: esse elemento contém o ShellLink codificado na base64 apontando para o local definido no <url> elemento. O Windows 7 cria o ShellLink a partir do valor do <url> elemento e atualiza corretamente esse campo na primeira carga dessa biblioteca, portanto, deve ser deixado vazio pelo autor. |



 

## <a name="remarks"></a>Comentários

Esse elemento pode ser usado em vez de <locationProvider> quando o local está no sistema de arquivos ou o conector é um manipulador de protocolo conhecido (como MAPI:). Se <simpleLocation> estiver presente, não deverá haver um <locationProvider> elemento. Para os conectores de pesquisa do provedor de serviço Web, use o [<locationProvider>](search-schema-sconn-locationprovider.md) elemento em vez disso.

## <a name="examples"></a>Exemplos


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



 

 



