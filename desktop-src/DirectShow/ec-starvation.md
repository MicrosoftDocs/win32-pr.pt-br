---
description: Um filtro não está recebendo dados suficientes.
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: EC_STARVATION (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988d550b93ecb9a3c2f78f2d07f50a3965be945d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751667"
---
# <a name="ec_starvation"></a><span data-ttu-id="8fc26-103">\_privação de EC</span><span class="sxs-lookup"><span data-stu-id="8fc26-103">EC\_STARVATION</span></span>

<span data-ttu-id="8fc26-104">Um filtro não está recebendo dados suficientes.</span><span class="sxs-lookup"><span data-stu-id="8fc26-104">A filter is not receiving enough data.</span></span>

## <a name="parameters"></a><span data-ttu-id="8fc26-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fc26-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc26-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="8fc26-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="8fc26-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="8fc26-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="8fc26-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="8fc26-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="8fc26-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="8fc26-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="8fc26-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="8fc26-110">Default Action</span></span>

<span data-ttu-id="8fc26-111">O evento não é enviado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8fc26-111">The event is not sent to the application.</span></span> <span data-ttu-id="8fc26-112">Se o grafo de filtro estiver em execução, o Gerenciador de gráfico de filtro pausará o grafo e aguardará a pausa ser concluída.</span><span class="sxs-lookup"><span data-stu-id="8fc26-112">If the filter graph is running, the filter graph manager pauses the graph and waits for the pause to complete.</span></span> <span data-ttu-id="8fc26-113">Em seguida, ele executa o grafo novamente.</span><span class="sxs-lookup"><span data-stu-id="8fc26-113">Then it runs the graph again.</span></span> <span data-ttu-id="8fc26-114">O filtro que envia o evento não deve concluir sua transição para em pausa até que ele tenha dados suficientes para retomar.</span><span class="sxs-lookup"><span data-stu-id="8fc26-114">The filter sending the event should not complete its transition to paused until it has enough data to resume.</span></span> <span data-ttu-id="8fc26-115">Se o grafo de filtro não estiver em execução, o Gerenciador de gráfico de filtro ignorará esse evento.</span><span class="sxs-lookup"><span data-stu-id="8fc26-115">If the filter graph is not running, the filter graph manager ignores this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fc26-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fc26-116">Remarks</span></span>

<span data-ttu-id="8fc26-117">Um analisador ou filtro de origem poderá enviar esse evento se houver poucos dados chegando.</span><span class="sxs-lookup"><span data-stu-id="8fc26-117">A parser or source filter can send this event if too little data is arriving.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fc26-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fc26-118">Requirements</span></span>



| <span data-ttu-id="8fc26-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fc26-119">Requirement</span></span> | <span data-ttu-id="8fc26-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc26-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc26-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8fc26-121">Header</span></span><br/> | <dl> <span data-ttu-id="8fc26-122"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fc26-122"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc26-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fc26-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc26-124">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="8fc26-124">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="8fc26-125">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="8fc26-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




