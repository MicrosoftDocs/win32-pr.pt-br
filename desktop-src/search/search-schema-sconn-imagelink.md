---
description: O <imageLink> elemento opcional especifica uma miniatura para este conector de pesquisa. Esse elemento tem um elemento filho obrigatório e nenhum atributo.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Elemento imageLink (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b2e5cbbfc8bbd98557ebd0405a09cf998e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783741"
---
# <a name="imagelink-element-search-connector-schema"></a><span data-ttu-id="a08e3-104">Elemento imageLink (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="a08e3-104">imageLink Element (Search Connector Schema)</span></span>

<span data-ttu-id="a08e3-105">O <imageLink> elemento opcional especifica uma miniatura para este conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a08e3-105">The optional <imageLink> element specifies a thumbnail for this search connector.</span></span> <span data-ttu-id="a08e3-106">Esse elemento tem um elemento filho obrigatório e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="a08e3-106">This element has one mandatory child element and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a08e3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a08e3-107">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="a08e3-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a08e3-108">Element Information</span></span>



| <span data-ttu-id="a08e3-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a08e3-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="a08e3-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a08e3-110">Child Elements</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a08e3-111">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="a08e3-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="a08e3-112">Elemento URL imageLink (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="a08e3-112">imageLink url Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a><span data-ttu-id="a08e3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a08e3-113">Remarks</span></span>

<span data-ttu-id="a08e3-114">O valor de imageLink pode ser um caminho de sistema de arquivos local ou uma URL.</span><span class="sxs-lookup"><span data-stu-id="a08e3-114">The imageLink value can be a local file system path or a URL.</span></span> <span data-ttu-id="a08e3-115">O arquivo de imagem pode ser qualquer um dos tipos de imagem básicos com suporte do Windows 7 (PNG, BMP, JPG, GIF).</span><span class="sxs-lookup"><span data-stu-id="a08e3-115">The image file can be any of the basic image types supported by Windows 7 (PNG, BMP, JPG, GIF).</span></span>

## <a name="example-of-an-imagelink-element"></a><span data-ttu-id="a08e3-116">Exemplo de um elemento imageLink</span><span class="sxs-lookup"><span data-stu-id="a08e3-116">Example of an imageLink Element</span></span>


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



