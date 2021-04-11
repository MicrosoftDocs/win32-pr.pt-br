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
# <a name="simplelocation-element-search-connector-schema"></a><span data-ttu-id="5670a-104">Elemento simpleLocation (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="5670a-104">simpleLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="5670a-105">O <simpleLocation> elemento Especifica o local para os conectores de pesquisa que são baseados em sistema de arquivos ou baseado em manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="5670a-105">The <simpleLocation> element specifies the location for search connectors that are file-system based or protocol-handler based.</span></span> <span data-ttu-id="5670a-106">Esse elemento tem dois elementos filho e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="5670a-106">This element has two child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5670a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5670a-107">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="5670a-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5670a-108">Element Information</span></span>



| <span data-ttu-id="5670a-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="5670a-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="5670a-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5670a-110">Child Elements</span></span>                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5670a-111">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="5670a-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="5670a-112">Elemento URL simpleLocation (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="5670a-112">simpleLocation url Element (Search Connector Schema)</span></span>](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | <span data-ttu-id="5670a-113">serializado: esse elemento contém o ShellLink codificado na base64 apontando para o local definido no <url> elemento.</span><span class="sxs-lookup"><span data-stu-id="5670a-113">serialized: This element contains the base64-encoded ShellLink pointing to the location defined in the <url> element.</span></span> <span data-ttu-id="5670a-114">O Windows 7 cria o ShellLink a partir do valor do <url> elemento e atualiza corretamente esse campo na primeira carga dessa biblioteca, portanto, deve ser deixado vazio pelo autor.</span><span class="sxs-lookup"><span data-stu-id="5670a-114">Windows 7 creates the ShellLink from the value of the <url> element and properly updates this field on the first load of this library, so it should be left empty by the author.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5670a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5670a-115">Remarks</span></span>

<span data-ttu-id="5670a-116">Esse elemento pode ser usado em vez de <locationProvider> quando o local está no sistema de arquivos ou o conector é um manipulador de protocolo conhecido (como MAPI:).</span><span class="sxs-lookup"><span data-stu-id="5670a-116">This element can be used instead of <locationProvider> when the location is on the file system or the connector is a known protocol handler (like mapi:).</span></span> <span data-ttu-id="5670a-117">Se <simpleLocation> estiver presente, não deverá haver um <locationProvider> elemento.</span><span class="sxs-lookup"><span data-stu-id="5670a-117">If <simpleLocation> is present, there MUST NOT be a <locationProvider> element.</span></span> <span data-ttu-id="5670a-118">Para os conectores de pesquisa do provedor de serviço Web, use o [<locationProvider>](search-schema-sconn-locationprovider.md) elemento em vez disso.</span><span class="sxs-lookup"><span data-stu-id="5670a-118">For web service provider search connectors, use the [<locationProvider>](search-schema-sconn-locationprovider.md) element instead.</span></span>

## <a name="examples"></a><span data-ttu-id="5670a-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5670a-119">Examples</span></span>


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



 

 



