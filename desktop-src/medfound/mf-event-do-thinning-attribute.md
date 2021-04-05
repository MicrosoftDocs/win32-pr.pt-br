---
description: Quando uma fonte de mídia solicita uma nova taxa de reprodução, esse atributo especifica se a origem também solicita a fina. Para obter uma definição de estreitamento, consulte sobre o controle de taxa.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: Atributo MF_EVENT_DO_THINNING (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08807413881a13789c50dbf2d063693e7e4539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921029"
---
# <a name="mf_event_do_thinning-attribute"></a><span data-ttu-id="f4abf-104">O \_ evento MF \_ faz o atributo de \_ finamento</span><span class="sxs-lookup"><span data-stu-id="f4abf-104">MF\_EVENT\_DO\_THINNING attribute</span></span>

<span data-ttu-id="f4abf-105">Quando uma fonte de mídia solicita uma nova taxa de reprodução, esse atributo especifica se a origem também solicita a fina.</span><span class="sxs-lookup"><span data-stu-id="f4abf-105">When a media source requests a new playback rate, this attribute specifies whether the source also requests thinning.</span></span> <span data-ttu-id="f4abf-106">Para obter uma definição de estreitamento, consulte [sobre o controle de taxa](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="f4abf-106">For a definition of thinning, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="f4abf-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f4abf-107">Data type</span></span>

<span data-ttu-id="f4abf-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f4abf-108">**UINT32**</span></span>

<span data-ttu-id="f4abf-109">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="f4abf-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4abf-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4abf-110">Remarks</span></span>

<span data-ttu-id="f4abf-111">Esse atributo é usado com o evento [MESourceRateChangeRequested](mesourceratechangerequested.md) .</span><span class="sxs-lookup"><span data-stu-id="f4abf-111">This attribute is used with the [MESourceRateChangeRequested](mesourceratechangerequested.md) event.</span></span> <span data-ttu-id="f4abf-112">Se o valor for **true**, a origem da mídia estará solicitando um comutador para reprodução fina.</span><span class="sxs-lookup"><span data-stu-id="f4abf-112">If the value is **TRUE**, the media source is requesting a switch to thinned playback.</span></span>

<span data-ttu-id="f4abf-113">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="f4abf-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="f4abf-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f4abf-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4abf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4abf-115">Requirements</span></span>



| <span data-ttu-id="f4abf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4abf-116">Requirement</span></span> | <span data-ttu-id="f4abf-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f4abf-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4abf-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4abf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f4abf-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4abf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f4abf-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4abf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f4abf-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4abf-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f4abf-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4abf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4abf-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4abf-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4abf-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4abf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4abf-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4abf-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4abf-126">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="f4abf-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4abf-127">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f4abf-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f4abf-128">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="f4abf-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




