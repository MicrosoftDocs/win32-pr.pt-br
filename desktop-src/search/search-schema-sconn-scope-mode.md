---
description: O <mode> elemento especifica se a URL deve ser incluída ou excluída do escopo do conector de pesquisa. Os valores permitidos são include e exclude. Este elemento não tem elementos filho e nenhum atributo.
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: Elemento Mode (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8c09b4c6de138e6e390d2c31a82fe5d1f56566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646856"
---
# <a name="mode-element-search-connector-schema"></a><span data-ttu-id="df137-105">Elemento Mode (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="df137-105">mode Element (Search Connector Schema)</span></span>

<span data-ttu-id="df137-106">O <mode> elemento especifica se a URL deve ser incluída ou excluída do escopo do conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="df137-106">The <mode> element specifies whether the URL should be included or excluded from the scope of the search connector.</span></span> <span data-ttu-id="df137-107">Os valores permitidos são `Include` e `Exclude` .</span><span class="sxs-lookup"><span data-stu-id="df137-107">The allowed values are `Include` and `Exclude`.</span></span> <span data-ttu-id="df137-108">Este elemento não tem elementos filho e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="df137-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="df137-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df137-109">Syntax</span></span>


```
<!-- mode -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="mode" default="Include">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Include"/>
                                            <xs:enumeration value="Exclude"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="df137-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="df137-110">Element Information</span></span>



| <span data-ttu-id="df137-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="df137-111">Parent Element</span></span>                                                                   | <span data-ttu-id="df137-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="df137-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="df137-113">Elemento scopeItem (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="df137-113">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="df137-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="df137-114">Remarks</span></span>

<span data-ttu-id="df137-115">Um escopo excluído não pode ser pesquisado ou procurado.</span><span class="sxs-lookup"><span data-stu-id="df137-115">An excluded scope cannot be searched or browsed.</span></span> <span data-ttu-id="df137-116">Você pode aninhar URLs scopeItem.</span><span class="sxs-lookup"><span data-stu-id="df137-116">You can nest scopeItem URLs.</span></span> <span data-ttu-id="df137-117">Por exemplo, você pode incluir um escopo pai e todos os seus filhos, exceto um adicionando a URL pai como incluído, com um valor de profundidade profundo e excluindo a URL filho.</span><span class="sxs-lookup"><span data-stu-id="df137-117">For example, you can include a parent scope and all its children except one by adding the parent URL as included, with depth value of Deep, and excluding the child URL.</span></span>

## <a name="example"></a><span data-ttu-id="df137-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="df137-118">Example</span></span>

<span data-ttu-id="df137-119">O exemplo a seguir mostra um escopo de pesquisa que inclui C: \\ ExampleFolder e todas as suas pastas filho, exceto c: \\ ExampleFolder \\ ExcludeMe.</span><span class="sxs-lookup"><span data-stu-id="df137-119">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



