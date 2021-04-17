---
description: O <url> elemento Especifica uma URL para a miniatura deste conector de pesquisa. Se <imageLink> existir, esse elemento será necessário. Ele não tem nenhum elemento filho e nenhum atributo.
ms.assetid: addb2614-9f4f-4cab-a678-b6020b8c4648
title: Elemento URL imageLink (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97daaafcbf6336dd4d88c3c92315e656d137b1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763210"
---
# <a name="imagelink-url-element-search-connector-schema"></a>Elemento URL imageLink (esquema do conector de pesquisa)

O <url> elemento Especifica uma URL para a miniatura deste conector de pesquisa. Se <imageLink> existir, esse elemento será necessário. Ele não tem nenhum elemento filho e nenhum atributo.

## <a name="syntax"></a>Syntax


```
<!-- url -->
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



| Elemento pai                                                                   | Elementos filho |
|----------------------------------------------------------------------------------|----------------|
| [Elemento imageLink (esquema do conector de pesquisa)](search-schema-sconn-imagelink.md) |                |



 

## <a name="remarks"></a>Comentários

O valor pode ser um caminho do sistema de arquivos local ou uma URL. O arquivo de imagem pode ser qualquer um dos tipos de imagem básicos com suporte do Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelinkurl-element"></a>Exemplo de um elemento imageLinkurl


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



