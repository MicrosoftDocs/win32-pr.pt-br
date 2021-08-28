---
description: O elemento &lt; imageLink &gt; opcional especifica uma miniatura para esse conector de pesquisa. Esse elemento tem um elemento filho obrigatório e nenhum atributos.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Elemento imageLink (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6030f44e74f8f8441b3a6cd0835df9c5969619
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882396"
---
# <a name="imagelink-element-search-connector-schema"></a>Elemento imageLink (esquema do conector de pesquisa)

O elemento &lt; imageLink &gt; opcional especifica uma miniatura para esse conector de pesquisa. Esse elemento tem um elemento filho obrigatório e nenhum atributos.

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
| [Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)](search-schema-searchconnectordescription.md) | [Elemento imageLink url (Esquema do Conector de Pesquisa)](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a>Comentários

O valor imageLink pode ser um caminho do sistema de arquivos local ou uma URL. O arquivo de imagem pode ser qualquer um dos tipos de imagem básicos com suporte Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelink-element"></a>Exemplo de um elemento imageLink


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



