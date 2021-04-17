---
title: Tipo complexo InstrumentationType
description: Define o conteúdo da seção de instrumentação do manifesto.
ms.assetid: dbbb978d-50dd-44c0-8bd1-3e48b41afb88
keywords:
- Log de eventos do tipo complexo InstrumentationType
topic_type:
- apiref
api_name:
- InstrumentationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1679ae310a996458aad3e25aba74955036094e00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811375"
---
# <a name="instrumentationtype-complex-type"></a><span data-ttu-id="136fb-104">Tipo complexo InstrumentationType</span><span class="sxs-lookup"><span data-stu-id="136fb-104">InstrumentationType Complex Type</span></span>

<span data-ttu-id="136fb-105">Define o conteúdo da seção de instrumentação do manifesto.</span><span class="sxs-lookup"><span data-stu-id="136fb-105">Defines the contents of the instrumentation section of the manifest.</span></span>

``` syntax
<xs:complexType name="InstrumentationType">
    <xs:sequence>
        <xs:element name="events"
            type="EventsType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="136fb-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="136fb-106">Child elements</span></span>



| <span data-ttu-id="136fb-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="136fb-107">Element</span></span>                                                                  | <span data-ttu-id="136fb-108">Type</span><span class="sxs-lookup"><span data-stu-id="136fb-108">Type</span></span>                                                             | <span data-ttu-id="136fb-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="136fb-109">Description</span></span>                                                        |
|--------------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="136fb-110">**LostFocus**</span><span class="sxs-lookup"><span data-stu-id="136fb-110">**events**</span></span>](eventmanifestschema-events-instrumentationtype-element.md) | [<span data-ttu-id="136fb-111">**EventType**</span><span class="sxs-lookup"><span data-stu-id="136fb-111">**EventsType**</span></span>](eventmanifestschema-eventstype-complextype.md) | <span data-ttu-id="136fb-112">Contém uma lista de provedores que o manifesto define.</span><span class="sxs-lookup"><span data-stu-id="136fb-112">Contains a list of providers that the manifest defines.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="136fb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="136fb-113">Requirements</span></span>



| <span data-ttu-id="136fb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="136fb-114">Requirement</span></span> | <span data-ttu-id="136fb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="136fb-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="136fb-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="136fb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="136fb-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="136fb-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="136fb-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="136fb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="136fb-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="136fb-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





