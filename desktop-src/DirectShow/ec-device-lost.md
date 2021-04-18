---
description: Um dispositivo Plug and Play foi removido ou ficou disponível novamente.
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: EC_DEVICE_LOST (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fa3f6368e85f8dc54ca6fd8cc2e0eee21262a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760708"
---
# <a name="ec_device_lost"></a><span data-ttu-id="4bcc8-103">\_dispositivo EC \_ perdido</span><span class="sxs-lookup"><span data-stu-id="4bcc8-103">EC\_DEVICE\_LOST</span></span>

<span data-ttu-id="4bcc8-104">Um dispositivo Plug and Play foi removido ou ficou disponível novamente.</span><span class="sxs-lookup"><span data-stu-id="4bcc8-104">A Plug and Play device was removed or became available again.</span></span>

## <a name="parameters"></a><span data-ttu-id="4bcc8-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4bcc8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bcc8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="4bcc8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="4bcc8-107">(**IUnknown** \* ) Ponteiro para a interface **IUnknown** do filtro que representa o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4bcc8-107">(**IUnknown**\*) Pointer to the **IUnknown** interface of the filter that represents the device.</span></span>

</dd> <dt>

<span data-ttu-id="4bcc8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="4bcc8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="4bcc8-109">Zero se o dispositivo tiver sido removido ou 1 se o dispositivo estiver disponível novamente.</span><span class="sxs-lookup"><span data-stu-id="4bcc8-109">Zero if the device was removed, or 1 if the device is available again.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="4bcc8-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="4bcc8-110">Default Action</span></span>

<span data-ttu-id="4bcc8-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4bcc8-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bcc8-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4bcc8-112">Remarks</span></span>

<span data-ttu-id="4bcc8-113">Quando o dispositivo ficar disponível novamente, o estado anterior do filtro de dispositivo não será mais válido.</span><span class="sxs-lookup"><span data-stu-id="4bcc8-113">When the device becomes available again, the previous state of the device filter is no longer valid.</span></span> <span data-ttu-id="4bcc8-114">O aplicativo deve recriar o grafo para usar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4bcc8-114">The application must rebuild the graph in order to use the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bcc8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bcc8-115">Requirements</span></span>



| <span data-ttu-id="4bcc8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bcc8-116">Requirement</span></span> | <span data-ttu-id="4bcc8-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4bcc8-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4bcc8-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4bcc8-118">Header</span></span><br/> | <dl> <span data-ttu-id="4bcc8-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bcc8-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bcc8-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4bcc8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bcc8-121">Notificação de remoção de dispositivo</span><span class="sxs-lookup"><span data-stu-id="4bcc8-121">Device Removal Notification</span></span>](device-removal-notification.md)
</dt> <dt>

[<span data-ttu-id="4bcc8-122">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="4bcc8-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="4bcc8-123">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="4bcc8-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




