---
description: O <depth> elemento especifica se o escopo do conector de pesquisa deve incluir URLs filho. Os valores permitidos são Deep e superficial. Este elemento não tem elementos filho e nenhum atributo.
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: Elemento Depth (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf68bcbc96b6d1beb2c381f0a17532272b8d397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920761"
---
# <a name="depth-element-search-connector-schema"></a><span data-ttu-id="98cca-105">Elemento Depth (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="98cca-105">depth Element (Search Connector Schema)</span></span>

<span data-ttu-id="98cca-106">O <depth> elemento especifica se o escopo do conector de pesquisa deve incluir URLs filho.</span><span class="sxs-lookup"><span data-stu-id="98cca-106">The <depth> element specifies whether the search connector's scope should include child URLs.</span></span> <span data-ttu-id="98cca-107">Os valores permitidos são `Deep` e `Shallow` .</span><span class="sxs-lookup"><span data-stu-id="98cca-107">The allowed values are `Deep` and `Shallow`.</span></span> <span data-ttu-id="98cca-108">Este elemento não tem elementos filho e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="98cca-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="98cca-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="98cca-109">Syntax</span></span>


```
<!-- depth -->
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
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
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



## <a name="element-information"></a><span data-ttu-id="98cca-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="98cca-110">Element Information</span></span>



| <span data-ttu-id="98cca-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="98cca-111">Parent Element</span></span>                                                                   | <span data-ttu-id="98cca-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="98cca-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="98cca-113">Elemento scopeItem (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="98cca-113">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="98cca-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="98cca-114">Remarks</span></span>

<span data-ttu-id="98cca-115">Se a profundidade for profunda, os usuários poderão procurar ou pesquisar itens no nível da URL do scopeItem ou em quaisquer URLs filho.</span><span class="sxs-lookup"><span data-stu-id="98cca-115">If the depth is deep, users can browse or search items in the scopeItem's URL level or within any child URLs.</span></span>

## <a name="example"></a><span data-ttu-id="98cca-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="98cca-116">Example</span></span>

<span data-ttu-id="98cca-117">O exemplo a seguir mostra um escopo de pesquisa que inclui C: \\ FolderA e todas as suas pastas filho e C: \\ FolderB, mas nenhuma de suas pastas filhas.</span><span class="sxs-lookup"><span data-stu-id="98cca-117">The following example shows a search scope that includes C:\\FolderA and all its child folders and C:\\FolderB but none of its child folders.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



