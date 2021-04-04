---
description: Especifica a hora de início para uma topologia de segmento.
ms.assetid: d8902fb6-c758-4d3d-9230-e918948bda19
title: Atributo MF_EVENT_SOURCE_PROJECTSTART (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512e2129c3104d9e7160163f03a9c28b2716273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837438"
---
# <a name="mf_event_source_projectstart-attribute"></a><span data-ttu-id="fe6e9-103">\_ \_ Atributo PROJECTSTART de origem do evento MF \_</span><span class="sxs-lookup"><span data-stu-id="fe6e9-103">MF\_EVENT\_SOURCE\_PROJECTSTART attribute</span></span>

<span data-ttu-id="fe6e9-104">Especifica a hora de início para uma topologia de segmento.</span><span class="sxs-lookup"><span data-stu-id="fe6e9-104">Specifies the start time for a segment topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="fe6e9-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fe6e9-105">Data type</span></span>

<span data-ttu-id="fe6e9-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="fe6e9-106">**UINT64**</span></span>

<span data-ttu-id="fe6e9-107">Tratar como um valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="fe6e9-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe6e9-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe6e9-108">Remarks</span></span>

<span data-ttu-id="fe6e9-109">Esse atributo é usado com o evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="fe6e9-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span> <span data-ttu-id="fe6e9-110">A origem do sequenciador define esse atributo quando a topologia de segmento atual tem o atributo [**MF \_ Topology \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="fe6e9-110">The sequencer source sets this attribute when the current segment topology has the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) attribute.</span></span> <span data-ttu-id="fe6e9-111">Os dois atributos têm o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="fe6e9-111">The two attributes have the same value.</span></span>

<span data-ttu-id="fe6e9-112">Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="fe6e9-112">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="fe6e9-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="fe6e9-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe6e9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe6e9-114">Requirements</span></span>



| <span data-ttu-id="fe6e9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe6e9-115">Requirement</span></span> | <span data-ttu-id="fe6e9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fe6e9-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe6e9-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe6e9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fe6e9-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe6e9-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fe6e9-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe6e9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fe6e9-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe6e9-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fe6e9-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe6e9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe6e9-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe6e9-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe6e9-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe6e9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe6e9-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fe6e9-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe6e9-125">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="fe6e9-125">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe6e9-126">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="fe6e9-126">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="fe6e9-127">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="fe6e9-127">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




