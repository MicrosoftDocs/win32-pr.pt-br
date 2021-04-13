---
title: Tipo complexo LevelListType
description: Define uma lista de níveis de severidade que especificam o detalhamento de um evento.
ms.assetid: 82102f8a-271e-4c3d-9b0a-1e20eaa87497
keywords:
- Log de eventos do tipo complexo LevelListType
topic_type:
- apiref
api_name:
- LevelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4456ade3977603948997304393a1c9414cb0c458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455973"
---
# <a name="levellisttype-complex-type"></a><span data-ttu-id="974c3-104">Tipo complexo LevelListType</span><span class="sxs-lookup"><span data-stu-id="974c3-104">LevelListType Complex Type</span></span>

<span data-ttu-id="974c3-105">Define uma lista de níveis de severidade que especificam o detalhamento de um evento.</span><span class="sxs-lookup"><span data-stu-id="974c3-105">Defines a list of severity levels that specify the verbosity of an event.</span></span>

``` syntax
<xs:complexType name="LevelListType">
    <xs:sequence>
        <xs:element name="level"
            type="LevelType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="974c3-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="974c3-106">Child elements</span></span>



| <span data-ttu-id="974c3-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="974c3-107">Element</span></span>                                                          | <span data-ttu-id="974c3-108">Type</span><span class="sxs-lookup"><span data-stu-id="974c3-108">Type</span></span>                                                           | <span data-ttu-id="974c3-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="974c3-109">Description</span></span>                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="974c3-110">**geral**</span><span class="sxs-lookup"><span data-stu-id="974c3-110">**level**</span></span>](eventmanifestschema-level-levellisttype-element.md) | [<span data-ttu-id="974c3-111">**LevelType**</span><span class="sxs-lookup"><span data-stu-id="974c3-111">**LevelType**</span></span>](eventmanifestschema-leveltype-complextype.md) | <span data-ttu-id="974c3-112">Define um valor de severidade que determina o detalhamento de eventos durante o registro em log.</span><span class="sxs-lookup"><span data-stu-id="974c3-112">Defines a severity value that determines the verbosity of events during logging.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="974c3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="974c3-113">Requirements</span></span>



| <span data-ttu-id="974c3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="974c3-114">Requirement</span></span> | <span data-ttu-id="974c3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="974c3-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="974c3-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="974c3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="974c3-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="974c3-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="974c3-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="974c3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="974c3-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="974c3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





