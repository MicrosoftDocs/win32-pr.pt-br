---
description: Enviado quando o VMR seleciona seu mecanismo de renderização.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9855b23e25a2c3b955c1499b9505efffcc5637e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760748"
---
# <a name="ec_vmr_renderdevice_set"></a><span data-ttu-id="b661c-103">conjunto de RENDERDEVICE do EC \_ VMR \_ \_</span><span class="sxs-lookup"><span data-stu-id="b661c-103">EC\_VMR\_RENDERDEVICE\_SET</span></span>

<span data-ttu-id="b661c-104">Enviado quando o VMR seleciona seu mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="b661c-104">Sent when the VMR has selected its rendering mechanism.</span></span>

## <a name="parameters"></a><span data-ttu-id="b661c-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b661c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b661c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b661c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b661c-107">Pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b661c-107">May be one of the following values:</span></span>



| <span data-ttu-id="b661c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b661c-108">Value</span></span>                        | <span data-ttu-id="b661c-109">Significado</span><span class="sxs-lookup"><span data-stu-id="b661c-109">Meaning</span></span>                                                  |
|------------------------------|----------------------------------------------------------|
| <span data-ttu-id="b661c-110">sobreposição de dispositivo de renderização do VMR \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b661c-110">VMR\_RENDER\_DEVICE\_OVERLAY</span></span> | <span data-ttu-id="b661c-111">O VMR será renderizado para a superfície de sobreposição (somente VMR-7).</span><span class="sxs-lookup"><span data-stu-id="b661c-111">The VMR will render to the overlay surface (VMR-7 only).</span></span> |
| <span data-ttu-id="b661c-112">\_VIDMEM de \_ dispositivo de renderização VMR \_</span><span class="sxs-lookup"><span data-stu-id="b661c-112">VMR\_RENDER\_DEVICE\_VIDMEM</span></span>  | <span data-ttu-id="b661c-113">O VMR será renderizado para a memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b661c-113">The VMR will render to video memory.</span></span>                     |
| <span data-ttu-id="b661c-114">\_SYSMEM de \_ dispositivo de renderização VMR \_</span><span class="sxs-lookup"><span data-stu-id="b661c-114">VMR\_RENDER\_DEVICE\_SYSMEM</span></span>  | <span data-ttu-id="b661c-115">O VMR será renderizado para a memória do sistema (somente VMR-7).</span><span class="sxs-lookup"><span data-stu-id="b661c-115">The VMR will render to system memory (VMR-7 only).</span></span>       |



 

</dd> <dt>

<span data-ttu-id="b661c-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b661c-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b661c-117">Não usado.</span><span class="sxs-lookup"><span data-stu-id="b661c-117">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b661c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b661c-118">Remarks</span></span>

<span data-ttu-id="b661c-119">Esse evento é enviado pelo VMR-7 e pelo VMR-9 e é encaminhado para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b661c-119">This event is sent by both the VMR-7 and the VMR-9 and it is forwarded to applications.</span></span> <span data-ttu-id="b661c-120">Observe que o VMR-9 oferece suporte apenas a destinos de renderização de memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b661c-120">Note that the VMR-9 only supports video memory render targets.</span></span>

## <a name="requirements"></a><span data-ttu-id="b661c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b661c-121">Requirements</span></span>



| <span data-ttu-id="b661c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b661c-122">Requirement</span></span> | <span data-ttu-id="b661c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b661c-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b661c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b661c-124">Header</span></span><br/> | <dl> <span data-ttu-id="b661c-125"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="b661c-125"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b661c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b661c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b661c-127">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="b661c-127">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b661c-128">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="b661c-128">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




