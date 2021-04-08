---
title: Elemento timecriado (SystemPropertiesType)
description: O carimbo de data/hora que identifica quando o evento foi registrado.
ms.assetid: 16b2b71b-078e-4862-b1be-ef7cec315bc5
keywords:
- EventLog de elemento TimeCreated
topic_type:
- apiref
api_name:
- TimeCreated
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 998bb03601f0ecbe87c571daa94b1f33e307d6af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918635"
---
# <a name="timecreated-systempropertiestype-element"></a><span data-ttu-id="17647-104">Elemento timecriado (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="17647-104">TimeCreated (SystemPropertiesType) Element</span></span>

<span data-ttu-id="17647-105">O carimbo de data/hora que identifica quando o evento foi registrado.</span><span class="sxs-lookup"><span data-stu-id="17647-105">The time stamp that identifies when the event was logged.</span></span>

``` syntax
<xs:element name="TimeCreated">
    <xs:complexType>
        <xs:attribute name="SystemTime"
            type="dateTime"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="17647-106">O elemento **Timecriated** é definido pelo tipo complexo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="17647-106">The **TimeCreated** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="17647-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="17647-107">Attributes</span></span>



| <span data-ttu-id="17647-108">Nome</span><span class="sxs-lookup"><span data-stu-id="17647-108">Name</span></span>       | <span data-ttu-id="17647-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="17647-109">Type</span></span>     | <span data-ttu-id="17647-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="17647-110">Description</span></span>                                              |
|------------|----------|----------------------------------------------------------|
| <span data-ttu-id="17647-111">SystemTime</span><span class="sxs-lookup"><span data-stu-id="17647-111">SystemTime</span></span> | <span data-ttu-id="17647-112">dateTime</span><span class="sxs-lookup"><span data-stu-id="17647-112">dateTime</span></span> | <span data-ttu-id="17647-113">A hora do sistema de quando o evento foi registrado.</span><span class="sxs-lookup"><span data-stu-id="17647-113">The system time of when the event was logged.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="17647-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17647-114">Requirements</span></span>



| <span data-ttu-id="17647-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="17647-115">Requirement</span></span> | <span data-ttu-id="17647-116">Valor</span><span class="sxs-lookup"><span data-stu-id="17647-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="17647-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17647-117">Minimum supported client</span></span><br/> | <span data-ttu-id="17647-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17647-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="17647-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17647-119">Minimum supported server</span></span><br/> | <span data-ttu-id="17647-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17647-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17647-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="17647-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="17647-122">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="17647-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="17647-123">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="17647-123">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





