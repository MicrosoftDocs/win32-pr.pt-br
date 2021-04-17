---
description: Gerado por uma saída confiável para enviar informações de status sobre a imposição da política de saída.
ms.assetid: 4906f6c3-1570-421f-aef1-914bd338bb1f
title: Evento MEPolicyReport (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0053fb551a69b820beeb4237211cb9af446f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757269"
---
# <a name="mepolicyreport-event"></a><span data-ttu-id="a4360-103">Evento MEPolicyReport</span><span class="sxs-lookup"><span data-stu-id="a4360-103">MEPolicyReport event</span></span>

<span data-ttu-id="a4360-104">Gerado por uma saída confiável para enviar informações de status sobre a imposição da política de saída.</span><span class="sxs-lookup"><span data-stu-id="a4360-104">Raised by a trusted output to send status information about the enforcement of the output policy.</span></span>

## <a name="event-values"></a><span data-ttu-id="a4360-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="a4360-105">Event values</span></span>

<span data-ttu-id="a4360-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="a4360-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a4360-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a4360-107">VARTYPE</span></span>              | <span data-ttu-id="a4360-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4360-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="a4360-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="a4360-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a4360-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="a4360-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a4360-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4360-111">Remarks</span></span>

<span data-ttu-id="a4360-112">Os atributos e códigos de status desse evento dependem do sistema de proteção de conteúdo específico imposto pela saída confiável.</span><span class="sxs-lookup"><span data-stu-id="a4360-112">Attributes and status codes for this event depend on the specific content protection system enforced by the trusted output.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4360-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4360-113">Requirements</span></span>



| <span data-ttu-id="a4360-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4360-114">Requirement</span></span> | <span data-ttu-id="a4360-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a4360-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4360-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4360-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a4360-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4360-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a4360-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4360-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a4360-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4360-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a4360-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4360-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4360-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4360-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4360-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4360-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4360-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a4360-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




