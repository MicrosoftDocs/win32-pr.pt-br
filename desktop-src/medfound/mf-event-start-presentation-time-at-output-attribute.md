---
description: A hora da apresentação na qual os coletores de mídia processarão o primeiro exemplo da nova topologia.
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: Atributo MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a588bc6604deed6c6865cd8283390d28e3ffd49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828924"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a><span data-ttu-id="883ba-103">\_ \_ \_ Hora de início da apresentação do evento MF \_ \_ no \_ atributo de saída</span><span class="sxs-lookup"><span data-stu-id="883ba-103">MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT attribute</span></span>

<span data-ttu-id="883ba-104">A hora da apresentação na qual os coletores de mídia processarão o primeiro exemplo da nova topologia.</span><span class="sxs-lookup"><span data-stu-id="883ba-104">The presentation time at which the media sinks will render the first sample of the new topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="883ba-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="883ba-105">Data type</span></span>

<span data-ttu-id="883ba-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="883ba-106">**UINT64**</span></span>

<span data-ttu-id="883ba-107">Tratar como um valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="883ba-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="883ba-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="883ba-108">Remarks</span></span>

<span data-ttu-id="883ba-109">Se qualquer objeto de pipeline na topologia anterior tiver dado buffer, esse valor será um pouco menor do que o valor no atributo de [**deslocamento de tempo de \_ apresentação de evento \_ \_ \_ MF**](mf-event-presentation-time-offset-attribute.md) , pois os coletores devem renderizar os dados armazenados em buffer.</span><span class="sxs-lookup"><span data-stu-id="883ba-109">If any pipeline objects in the previous topology buffered data, this value will be slightly less than the value in the [**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**](mf-event-presentation-time-offset-attribute.md) attribute, because the sinks must render the buffered data.</span></span>

<span data-ttu-id="883ba-110">Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="883ba-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="883ba-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="883ba-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="883ba-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="883ba-112">Requirements</span></span>



| <span data-ttu-id="883ba-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="883ba-113">Requirement</span></span> | <span data-ttu-id="883ba-114">Valor</span><span class="sxs-lookup"><span data-stu-id="883ba-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="883ba-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="883ba-115">Minimum supported client</span></span><br/> | <span data-ttu-id="883ba-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="883ba-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="883ba-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="883ba-117">Minimum supported server</span></span><br/> | <span data-ttu-id="883ba-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="883ba-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="883ba-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="883ba-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="883ba-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="883ba-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="883ba-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="883ba-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="883ba-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="883ba-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="883ba-123">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="883ba-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="883ba-124">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="883ba-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="883ba-125">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="883ba-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




