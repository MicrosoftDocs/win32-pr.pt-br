---
description: O <locationProvider> elemento opcional especifica o provedor de pesquisa a ser usado pelo conector de pesquisa do provedor de serviço Web. Esse elemento contém um atributo obrigatório e um elemento filho opcional.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Elemento LocationProvider (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c68732300c190b44b984bbe64ca031a81ced84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797615"
---
# <a name="locationprovider-element-search-connector-schema"></a><span data-ttu-id="75242-104">Elemento LocationProvider (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="75242-104">locationProvider Element (Search Connector Schema)</span></span>

<span data-ttu-id="75242-105">O <locationProvider> elemento opcional especifica o provedor de pesquisa a ser usado pelo conector de pesquisa do provedor de serviço Web.</span><span class="sxs-lookup"><span data-stu-id="75242-105">The optional <locationProvider> element specifies the search provider to be used by the web service provider search connector.</span></span> <span data-ttu-id="75242-106">Esse elemento contém um atributo obrigatório e um elemento filho opcional.</span><span class="sxs-lookup"><span data-stu-id="75242-106">This element contains one mandatory attribute and an optional child element.</span></span>

## <a name="syntax"></a><span data-ttu-id="75242-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="75242-107">Syntax</span></span>


```
<!-- locationProvider -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="75242-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="75242-108">Element Information</span></span>



| <span data-ttu-id="75242-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="75242-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="75242-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="75242-110">Child Elements</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="75242-111">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="75242-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="75242-112">Elemento propertyBag (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="75242-112">propertyBag Element (Search Connector Schema)</span></span>](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a><span data-ttu-id="75242-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="75242-113">Attributes</span></span>



| <span data-ttu-id="75242-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="75242-114">Attribute</span></span> | <span data-ttu-id="75242-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="75242-115">Description</span></span>                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | <span data-ttu-id="75242-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="75242-116">Required.</span></span> <span data-ttu-id="75242-117">O identificador de classe (CLSID) do provedor de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="75242-117">The class identifier (CLSID) of the search provider.</span></span> |
| <span data-ttu-id="75242-118">bases</span><span class="sxs-lookup"><span data-stu-id="75242-118">codebase</span></span>  | <span data-ttu-id="75242-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="75242-119">Optional.</span></span>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="75242-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="75242-120">Remarks</span></span>

<span data-ttu-id="75242-121">O @clsid valor do atributo para o provedor de OpenSearch é {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.</span><span class="sxs-lookup"><span data-stu-id="75242-121">The @clsid attribute value for the OpenSearch provider is {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.</span></span>

<span data-ttu-id="75242-122">Os conectores de pesquisa baseados no sistema de arquivos e no manipulador de protocolo podem usar o [<simpleLocation>](search-schema-sconn-simplelocation.md) elemento em vez disso.</span><span class="sxs-lookup"><span data-stu-id="75242-122">File system and protocol handler based search connectors can use the [<simpleLocation>](search-schema-sconn-simplelocation.md) element instead.</span></span> <span data-ttu-id="75242-123">Se <locationProvider> estiver presente, não deverá haver um <simpleLocation> elemento na descrição do conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="75242-123">If <locationProvider> is present, there MUST NOT be a <simpleLocation> element in the Search Connector description.</span></span>

## <a name="example-of-a-locationprovider-element"></a><span data-ttu-id="75242-124">Exemplo de um elemento LocalProvider</span><span class="sxs-lookup"><span data-stu-id="75242-124">Example of a locationProvider Element</span></span>


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



