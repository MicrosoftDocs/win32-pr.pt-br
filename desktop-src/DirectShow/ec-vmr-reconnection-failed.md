---
description: Enviado pelo VMR-7 e o VMR-9 quando não foi possível aceitar uma solicitação de alteração de formato dinâmico do decodificador upstream.
ms.assetid: 0c865853-2484-4833-9c92-3d6452b655f1
title: EC_VMR_RECONNECTION_FAILED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d29703d5ede068710966119f16c44a9e3637249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760706"
---
# <a name="ec_vmr_reconnection_failed"></a><span data-ttu-id="4c07d-103">\_ \_ falha na reconexão do EC VMR \_</span><span class="sxs-lookup"><span data-stu-id="4c07d-103">EC\_VMR\_RECONNECTION\_FAILED</span></span>

<span data-ttu-id="4c07d-104">Enviado pelo VMR-7 e o VMR-9 quando não foi possível aceitar uma solicitação de alteração de formato dinâmico do decodificador upstream.</span><span class="sxs-lookup"><span data-stu-id="4c07d-104">Sent by the VMR-7 and the VMR-9 when it was unable to accept a dynamic format change request from the upstream decoder.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c07d-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c07d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c07d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="4c07d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="4c07d-107">(**HRESULT**) Código de status retornado de [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) no pino de entrada do VMR que falhou na reconexão.</span><span class="sxs-lookup"><span data-stu-id="4c07d-107">(**HRESULT**) Status code returned from [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the VMR's input pin that failed the reconnection.</span></span>

</dd> <dt>

<span data-ttu-id="4c07d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="4c07d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="4c07d-109">Não usado.</span><span class="sxs-lookup"><span data-stu-id="4c07d-109">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c07d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c07d-110">Remarks</span></span>

<span data-ttu-id="4c07d-111">Esse evento é encaminhado para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4c07d-111">This event is forwarded to applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c07d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c07d-112">Requirements</span></span>



| <span data-ttu-id="4c07d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c07d-113">Requirement</span></span> | <span data-ttu-id="4c07d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="4c07d-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c07d-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c07d-115">Header</span></span><br/> | <dl> <span data-ttu-id="4c07d-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c07d-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c07d-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c07d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c07d-118">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="4c07d-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="4c07d-119">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="4c07d-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




