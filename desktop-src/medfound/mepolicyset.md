---
description: 'Gerado por uma autoridade de confiança de saída (OTA) quando o método IMFOutputTrustAuthority:: setpolicy é concluído de forma assíncrona.'
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: Evento MEPolicySet (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238af6cbd740e62825ae0b661769c1cf1bf880ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808243"
---
# <a name="mepolicyset-event"></a><span data-ttu-id="84dfe-103">Evento MEPolicySet</span><span class="sxs-lookup"><span data-stu-id="84dfe-103">MEPolicySet event</span></span>

<span data-ttu-id="84dfe-104">Gerado por uma autoridade de confiança de saída (OTA) quando o método [**IMFOutputTrustAuthority:: setpolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="84dfe-104">Raised by an output trust authority (OTA) when the [**IMFOutputTrustAuthority::SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="84dfe-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="84dfe-105">Event values</span></span>

<span data-ttu-id="84dfe-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="84dfe-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="84dfe-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="84dfe-107">VARTYPE</span></span>              | <span data-ttu-id="84dfe-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="84dfe-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="84dfe-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="84dfe-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="84dfe-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="84dfe-110">No event data.</span></span><br/> <br/> |
| <span data-ttu-id="84dfe-111">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="84dfe-111">VT\_UI4</span></span><br/> | <span data-ttu-id="84dfe-112">Um identificador que pode ser definido em um [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) por meio do atributo [MF_POLICY_ID](mf-policy-id.md) .</span><span class="sxs-lookup"><span data-stu-id="84dfe-112">An identifier that can be set on an [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) through the [MF_POLICY_ID](mf-policy-id.md) attribute.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="84dfe-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84dfe-113">Requirements</span></span>



| <span data-ttu-id="84dfe-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="84dfe-114">Requirement</span></span> | <span data-ttu-id="84dfe-115">Valor</span><span class="sxs-lookup"><span data-stu-id="84dfe-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84dfe-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84dfe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="84dfe-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84dfe-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="84dfe-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84dfe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="84dfe-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="84dfe-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="84dfe-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84dfe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="84dfe-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84dfe-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84dfe-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="84dfe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84dfe-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84dfe-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




