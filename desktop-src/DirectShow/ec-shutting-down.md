---
description: O grafo de filtro está sendo desligado, antes de ser destruído.
ms.assetid: f1b3fc87-16ec-485b-b659-fc7d975c4a22
title: EC_SHUTTING_DOWN (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 471b746df3980afd96bbfc122a164ccd30561846
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748004"
---
# <a name="ec_shutting_down"></a><span data-ttu-id="b3008-103">desligar \_ o EC \_</span><span class="sxs-lookup"><span data-stu-id="b3008-103">EC\_SHUTTING\_DOWN</span></span>

<span data-ttu-id="b3008-104">O grafo de filtro está sendo desligado, antes de ser destruído.</span><span class="sxs-lookup"><span data-stu-id="b3008-104">The filter graph is shutting down, prior to being destroyed.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3008-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3008-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3008-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b3008-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b3008-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="b3008-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="b3008-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b3008-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b3008-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="b3008-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="b3008-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="b3008-110">Default Action</span></span>

<span data-ttu-id="b3008-111">Esse evento não é enviado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b3008-111">This event is not sent to the application.</span></span> <span data-ttu-id="b3008-112">O Gerenciador de gráfico de filtro o envia para os distribuidores de plug-in, para notificá-los de que o grafo está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="b3008-112">The filter graph manager sends it to plug-in distributors, to notify them that the graph is shutting down.</span></span> <span data-ttu-id="b3008-113">Os aplicativos não podem substituir a ação padrão desse evento.</span><span class="sxs-lookup"><span data-stu-id="b3008-113">Applications cannot override the default action of this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3008-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3008-114">Requirements</span></span>



| <span data-ttu-id="b3008-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3008-115">Requirement</span></span> | <span data-ttu-id="b3008-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b3008-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3008-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3008-117">Header</span></span><br/> | <dl> <span data-ttu-id="b3008-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3008-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3008-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3008-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3008-120">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="b3008-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b3008-121">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="b3008-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




