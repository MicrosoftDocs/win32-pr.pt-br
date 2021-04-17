---
title: Elemento controlGuid (ChannelPublishingType)
description: Identifica o GUID de sessão para uma sessão de ETW que contém eventos de WPP.
ms.assetid: a9e86468-8a97-4689-a258-85d253debf55
keywords:
- EventLog do elemento controlGuid
topic_type:
- apiref
api_name:
- controlGuid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92d4f6e1d2985bc983c34552b2e7a973075c9989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369599"
---
# <a name="controlguid-channelpublishingtype-element"></a><span data-ttu-id="1deae-104">Elemento controlGuid (ChannelPublishingType)</span><span class="sxs-lookup"><span data-stu-id="1deae-104">controlGuid (ChannelPublishingType) Element</span></span>

<span data-ttu-id="1deae-105">Identifica o GUID de sessão para uma sessão de ETW que contém eventos de WPP.</span><span class="sxs-lookup"><span data-stu-id="1deae-105">Identifies the session GUID for an ETW session that contains WPP events.</span></span>

``` syntax
<xs:element name="controlGuid"
    type="GUIDType"
 />
```

<span data-ttu-id="1deae-106">O elemento **controlGuid** é definido pelo tipo complexo [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1deae-106">The **controlGuid** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="1deae-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1deae-107">Requirements</span></span>



| <span data-ttu-id="1deae-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="1deae-108">Requirement</span></span> | <span data-ttu-id="1deae-109">Valor</span><span class="sxs-lookup"><span data-stu-id="1deae-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1deae-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1deae-110">Minimum supported client</span></span><br/> | <span data-ttu-id="1deae-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1deae-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1deae-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1deae-112">Minimum supported server</span></span><br/> | <span data-ttu-id="1deae-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1deae-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1deae-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="1deae-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="1deae-115">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="1deae-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="1deae-116">**publicando (channelType)**</span><span class="sxs-lookup"><span data-stu-id="1deae-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





