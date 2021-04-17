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
# <a name="imagelink-url-element-search-connector-schema"></a><span data-ttu-id="07501-105">Elemento URL imageLink (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="07501-105">imageLink url Element (Search Connector Schema)</span></span>

<span data-ttu-id="07501-106">O <url> elemento Especifica uma URL para a miniatura deste conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="07501-106">The <url> element specifies a URL to the thumbnail for this search connector.</span></span> <span data-ttu-id="07501-107">Se <imageLink> existir, esse elemento será necessário.</span><span class="sxs-lookup"><span data-stu-id="07501-107">If <imageLink> exists, this element is required.</span></span> <span data-ttu-id="07501-108">Ele não tem nenhum elemento filho e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="07501-108">It has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="07501-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="07501-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="07501-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="07501-110">Element Information</span></span>



| <span data-ttu-id="07501-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="07501-111">Parent Element</span></span>                                                                   | <span data-ttu-id="07501-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="07501-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="07501-113">Elemento imageLink (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="07501-113">imageLink Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="07501-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="07501-114">Remarks</span></span>

<span data-ttu-id="07501-115">O valor pode ser um caminho do sistema de arquivos local ou uma URL.</span><span class="sxs-lookup"><span data-stu-id="07501-115">The value can be a local file system path or a URL.</span></span> <span data-ttu-id="07501-116">O arquivo de imagem pode ser qualquer um dos tipos de imagem básicos com suporte do Windows 7 (PNG, BMP, JPG, GIF).</span><span class="sxs-lookup"><span data-stu-id="07501-116">The image file can be any of the basic image types supported by Windows 7 (PNG, BMP, JPG, GIF).</span></span>

## <a name="example-of-an-imagelinkurl-element"></a><span data-ttu-id="07501-117">Exemplo de um elemento imageLinkurl</span><span class="sxs-lookup"><span data-stu-id="07501-117">Example of an imageLinkurl Element</span></span>


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



