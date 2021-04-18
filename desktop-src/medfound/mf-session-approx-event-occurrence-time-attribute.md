---
description: A hora aproximada em que a sessão de mídia gerou um evento.
ms.assetid: 58083bc8-59cc-4503-8fae-36fcd864921a
title: Atributo MF_SESSION_APPROX_EVENT_OCCURRENCE_TIME (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a31b1970c2c9d86384c12c50777a8cee55e3ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771425"
---
# <a name="mf_session_approx_event_occurrence_time-attribute"></a><span data-ttu-id="0bd5c-103">\_Atributo de \_ \_ tempo de ocorrência de evento aprox \_ de sessão MF \_</span><span class="sxs-lookup"><span data-stu-id="0bd5c-103">MF\_SESSION\_APPROX\_EVENT\_OCCURRENCE\_TIME attribute</span></span>

<span data-ttu-id="0bd5c-104">A hora aproximada em que a sessão de mídia gerou um evento.</span><span class="sxs-lookup"><span data-stu-id="0bd5c-104">The approximate time when the Media Session raised an event.</span></span>

## <a name="data-type"></a><span data-ttu-id="0bd5c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0bd5c-105">Data type</span></span>

<span data-ttu-id="0bd5c-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="0bd5c-106">**UINT64**</span></span>

<span data-ttu-id="0bd5c-107">Tratar como um valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="0bd5c-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bd5c-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bd5c-108">Remarks</span></span>

<span data-ttu-id="0bd5c-109">Alguns eventos da sessão de mídia têm esse atributo.</span><span class="sxs-lookup"><span data-stu-id="0bd5c-109">Some events from the Media Session have this attribute.</span></span> <span data-ttu-id="0bd5c-110">O valor fornece o tempo de apresentação aproximado quando o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="0bd5c-110">The value gives the approximate presentation time when the event was raised.</span></span>

<span data-ttu-id="0bd5c-111">Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="0bd5c-111">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="0bd5c-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0bd5c-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bd5c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bd5c-113">Requirements</span></span>



| <span data-ttu-id="0bd5c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bd5c-114">Requirement</span></span> | <span data-ttu-id="0bd5c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0bd5c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd5c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bd5c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0bd5c-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0bd5c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0bd5c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bd5c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0bd5c-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0bd5c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0bd5c-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0bd5c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bd5c-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bd5c-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bd5c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bd5c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bd5c-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0bd5c-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0bd5c-124">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="0bd5c-124">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="0bd5c-125">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="0bd5c-125">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="0bd5c-126">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="0bd5c-126">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




