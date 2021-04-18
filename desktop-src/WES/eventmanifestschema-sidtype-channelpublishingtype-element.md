---
title: Elemento sidType (ChannelPublishingType)
description: Determina se um SID (identificador de segurança) do principal deve ser incluído em cada evento gravado no canal.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- EventLog do elemento sidType
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d65e1ade4ded95b070b45de9462f6aee2c60ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784934"
---
# <a name="sidtype-channelpublishingtype-element"></a><span data-ttu-id="a8367-104">Elemento sidType (ChannelPublishingType)</span><span class="sxs-lookup"><span data-stu-id="a8367-104">sidType (ChannelPublishingType) Element</span></span>

<span data-ttu-id="a8367-105">Determina se um SID (identificador de segurança) do principal deve ser incluído em cada evento gravado no canal.</span><span class="sxs-lookup"><span data-stu-id="a8367-105">Determines whether to include a security identifier (SID) of the principal with each event written to the channel.</span></span>

``` syntax
<xs:element name="sidType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="None"
             />
            <xs:enumeration
                value="Publishing"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="a8367-106">O elemento **sidType** é definido pelo tipo complexo [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a8367-106">The **sidType** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8367-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8367-107">Requirements</span></span>



| <span data-ttu-id="a8367-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8367-108">Requirement</span></span> | <span data-ttu-id="a8367-109">Valor</span><span class="sxs-lookup"><span data-stu-id="a8367-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8367-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8367-110">Minimum supported client</span></span><br/> | <span data-ttu-id="a8367-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8367-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8367-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8367-112">Minimum supported server</span></span><br/> | <span data-ttu-id="a8367-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8367-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8367-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8367-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8367-115">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="a8367-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="a8367-116">**publicando (channelType)**</span><span class="sxs-lookup"><span data-stu-id="a8367-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





