---
description: O <imageLink> elemento opcional especifica uma miniatura para este conector de pesquisa. Esse elemento tem um elemento filho obrigatório e nenhum atributo.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Elemento imageLink (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007ad8c2500e2739210646c446d9f906d5a83571ea4ac9780ab9136b73805c83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711086"
---
# <a name="imagelink-element-search-connector-schema"></a>Elemento imageLink (esquema do conector de pesquisa)

O <imageLink> elemento opcional especifica uma miniatura para este conector de pesquisa. Esse elemento tem um elemento filho obrigatório e nenhum atributo.

## <a name="syntax"></a>Syntax


```
<!-- imageLink -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="imageLink" minOccurs="0">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="url" type="xs:anyURI"/>
                    </xs:sequence>
                </xs:complexType>
            </xs:element>            
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                                                                   | Elementos filho                                                                           |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)](search-schema-searchconnectordescription.md) | [Elemento URL imageLink (esquema do conector de pesquisa)](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a>Comentários

O valor de imageLink pode ser um caminho de sistema de arquivos local ou uma URL. o arquivo de imagem pode ser qualquer um dos tipos de imagem básicos com suporte do Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelink-element"></a>Exemplo de um elemento imageLink


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



