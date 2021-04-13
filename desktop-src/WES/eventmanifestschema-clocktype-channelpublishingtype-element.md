---
title: Elemento clocktype (ChannelPublishingType)
description: A resolução de relógio a ser usada ao registrar em log o carimbo de data/hora para cada evento.
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- Log do elemento EventLogtype
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6b85537ec209f39da87e74db6881abdf60e488b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369301"
---
# <a name="clocktype-channelpublishingtype-element"></a><span data-ttu-id="8a36e-104">Elemento clocktype (ChannelPublishingType)</span><span class="sxs-lookup"><span data-stu-id="8a36e-104">clockType (ChannelPublishingType) Element</span></span>

<span data-ttu-id="8a36e-105">A resolução de relógio a ser usada ao registrar em log o carimbo de data/hora para cada evento.</span><span class="sxs-lookup"><span data-stu-id="8a36e-105">The clock resolution to use when logging the time stamp for each event.</span></span>

``` syntax
<xs:element name="clockType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="SystemTime"
             />
            <xs:enumeration
                value="QPC"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="8a36e-106">O elemento **clocktype** é definido pelo tipo complexo [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8a36e-106">The **clockType** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a36e-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a36e-107">Requirements</span></span>



| <span data-ttu-id="8a36e-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a36e-108">Requirement</span></span> | <span data-ttu-id="8a36e-109">Valor</span><span class="sxs-lookup"><span data-stu-id="8a36e-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8a36e-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a36e-110">Minimum supported client</span></span><br/> | <span data-ttu-id="8a36e-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a36e-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8a36e-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a36e-112">Minimum supported server</span></span><br/> | <span data-ttu-id="8a36e-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a36e-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a36e-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a36e-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="8a36e-115">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="8a36e-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="8a36e-116">**publicando (channelType)**</span><span class="sxs-lookup"><span data-stu-id="8a36e-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





