---
title: Tipo complexo TemplateListType
description: Define uma lista de modelos que especificam os dados a serem incluídos com os eventos. | Tipo complexo TemplateListType
ms.assetid: 7f676746-6773-4ae2-8330-60d432c29e3a
keywords:
- Log de eventos do tipo complexo TemplateListType
topic_type:
- apiref
api_name:
- TemplateListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a60b31fd88d05f00229f27a616a29483a29bd49d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663915"
---
# <a name="templatelisttype-complex-type"></a><span data-ttu-id="25184-105">Tipo complexo TemplateListType</span><span class="sxs-lookup"><span data-stu-id="25184-105">TemplateListType Complex Type</span></span>

<span data-ttu-id="25184-106">Define uma lista de modelos que especificam os dados a serem incluídos com os eventos.</span><span class="sxs-lookup"><span data-stu-id="25184-106">Defines a list of templates that specify the data to include with the events.</span></span>

``` syntax
<xs:complexType name="TemplateListType">
    <xs:sequence>
        <xs:element name="template"
            type="TemplateItemType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="25184-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="25184-107">Child elements</span></span>



| <span data-ttu-id="25184-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="25184-108">Element</span></span>                                                                   | <span data-ttu-id="25184-109">Type</span><span class="sxs-lookup"><span data-stu-id="25184-109">Type</span></span>                                                                         | <span data-ttu-id="25184-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="25184-110">Description</span></span>                                                           |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="25184-111">**modelos**</span><span class="sxs-lookup"><span data-stu-id="25184-111">**template**</span></span>](eventmanifestschema-template-templatelisttype-element.md) | [<span data-ttu-id="25184-112">**TemplateItemType**</span><span class="sxs-lookup"><span data-stu-id="25184-112">**TemplateItemType**</span></span>](eventmanifestschema-templateitemtype-complextype.md) | <span data-ttu-id="25184-113">Um modelo que define os dados a serem incluídos com um evento.</span><span class="sxs-lookup"><span data-stu-id="25184-113">A template that defines the data to include with an event.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="25184-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25184-114">Requirements</span></span>



| <span data-ttu-id="25184-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="25184-115">Requirement</span></span> | <span data-ttu-id="25184-116">Valor</span><span class="sxs-lookup"><span data-stu-id="25184-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="25184-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25184-117">Minimum supported client</span></span><br/> | <span data-ttu-id="25184-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25184-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="25184-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25184-119">Minimum supported server</span></span><br/> | <span data-ttu-id="25184-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="25184-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





