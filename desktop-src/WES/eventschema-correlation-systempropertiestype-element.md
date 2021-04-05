---
title: Elemento de correlação (SystemPropertiesType)
description: Os identificadores de atividade que os consumidores podem usar para agrupar eventos relacionados.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- Log de elementos de correlação
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91baca47479fe19988f3bfb23d573b8d92583d79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918898"
---
# <a name="correlation-systempropertiestype-element"></a><span data-ttu-id="7996b-104">Elemento de correlação (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="7996b-104">Correlation (SystemPropertiesType) Element</span></span>

<span data-ttu-id="7996b-105">Os identificadores de atividade que os consumidores podem usar para agrupar eventos relacionados.</span><span class="sxs-lookup"><span data-stu-id="7996b-105">The activity identifiers that consumers can use to group related events together.</span></span>

``` syntax
<xs:element name="Correlation">
    <xs:complexType>
        <xs:attribute name="ActivityID"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="RelatedActivityID"
            type="GUIDType"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="7996b-106">O elemento de **correlação** é definido pelo tipo complexo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7996b-106">The **Correlation** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="7996b-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="7996b-107">Attributes</span></span>



| <span data-ttu-id="7996b-108">Nome</span><span class="sxs-lookup"><span data-stu-id="7996b-108">Name</span></span>              | <span data-ttu-id="7996b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7996b-109">Type</span></span>                                                | <span data-ttu-id="7996b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7996b-110">Description</span></span>                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7996b-111">ActivityID</span><span class="sxs-lookup"><span data-stu-id="7996b-111">ActivityID</span></span>        | [<span data-ttu-id="7996b-112">**GUIDtype**</span><span class="sxs-lookup"><span data-stu-id="7996b-112">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="7996b-113">Um identificador global exclusivo que identifica a atividade atual.</span><span class="sxs-lookup"><span data-stu-id="7996b-113">A globally unique identifier that identifies the current activity.</span></span> <span data-ttu-id="7996b-114">Os eventos que são publicados com esse identificador fazem parte da mesma atividade.</span><span class="sxs-lookup"><span data-stu-id="7996b-114">The events that are published with this identifier are part of the same activity.</span></span><br/>                              |
| <span data-ttu-id="7996b-115">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="7996b-115">RelatedActivityID</span></span> | [<span data-ttu-id="7996b-116">**GUIDtype**</span><span class="sxs-lookup"><span data-stu-id="7996b-116">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="7996b-117">Um identificador global exclusivo que identifica a atividade para a qual o controle foi transferido.</span><span class="sxs-lookup"><span data-stu-id="7996b-117">A globally unique identifier that identifies the activity to which control was transferred to.</span></span> <span data-ttu-id="7996b-118">Em seguida, os eventos relacionados teriam esse identificador como seu identificador de ActivityId.</span><span class="sxs-lookup"><span data-stu-id="7996b-118">The related events would then have this identifier as their ActivityID identifier.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7996b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7996b-119">Requirements</span></span>



| <span data-ttu-id="7996b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7996b-120">Requirement</span></span> | <span data-ttu-id="7996b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7996b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7996b-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7996b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7996b-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7996b-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7996b-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7996b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7996b-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7996b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7996b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="7996b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="7996b-127">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="7996b-127">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="7996b-128">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="7996b-128">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





