---
description: O estado do grafo de filtro foi alterado.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64cc62ba15f77370e52821c3335f9a22f573d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758067"
---
# <a name="ec_state_change"></a><span data-ttu-id="8badf-103">\_alteração de estado do EC \_</span><span class="sxs-lookup"><span data-stu-id="8badf-103">EC\_STATE\_CHANGE</span></span>

<span data-ttu-id="8badf-104">O estado do grafo de filtro foi alterado.</span><span class="sxs-lookup"><span data-stu-id="8badf-104">The filter graph has changed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="8badf-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8badf-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8badf-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="8badf-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="8badf-107">(**DWORD**) Membro do tipo enumerado de [**\_ estado do filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , indicando o novo estado do grafo.</span><span class="sxs-lookup"><span data-stu-id="8badf-107">(**DWORD**) Member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the new graph state.</span></span>

</dd> <dt>

<span data-ttu-id="8badf-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="8badf-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="8badf-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="8badf-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="8badf-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="8badf-110">Default Action</span></span>

<span data-ttu-id="8badf-111">Nenhuma ação padrão.</span><span class="sxs-lookup"><span data-stu-id="8badf-111">No default action.</span></span> <span data-ttu-id="8badf-112">O evento não é enviado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8badf-112">The event is not sent to the application.</span></span>

> [!Note]  
> <span data-ttu-id="8badf-113">Esse evento pode ocorrer quando o grafo é desligado.</span><span class="sxs-lookup"><span data-stu-id="8badf-113">This event can occur when the graph shuts down.</span></span> <span data-ttu-id="8badf-114">Se você substituir a ação padrão e escutar esse evento, deverá ter cuidado para não processar eventos depois de liberar o Gerenciador de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="8badf-114">If you override the default action and listen for this event, you must be especially careful not to process events after releasing the Filter Graph Manager.</span></span> <span data-ttu-id="8badf-115">Caso contrário, seu aplicativo poderá fazer referência a um ponteiro [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) inválido e falhar.</span><span class="sxs-lookup"><span data-stu-id="8badf-115">Otherwise, your application might reference an invalid [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) pointer and crash.</span></span> <span data-ttu-id="8badf-116">Para obter mais informações, consulte [respondendo a eventos](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="8badf-116">For more information, see [Responding to Events](responding-to-events.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8badf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8badf-117">Requirements</span></span>



| <span data-ttu-id="8badf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8badf-118">Requirement</span></span> | <span data-ttu-id="8badf-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8badf-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8badf-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8badf-120">Header</span></span><br/> | <dl> <span data-ttu-id="8badf-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="8badf-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8badf-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="8badf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8badf-123">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="8badf-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="8badf-124">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="8badf-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




