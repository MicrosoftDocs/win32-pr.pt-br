---
description: O grafo está armazenando dados em buffer ou parou de armazenar em buffer os dados.
ms.assetid: 39e8b151-0323-42b3-99f0-3dcd230925c8
title: EC_BUFFERING_DATA (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1395a10458abd7a29fdb65e7ab55fba62328d6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758473"
---
# <a name="ec_buffering_data"></a><span data-ttu-id="d9f6c-103">dados de buffer do EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="d9f6c-103">EC\_BUFFERING\_DATA</span></span>

<span data-ttu-id="d9f6c-104">O grafo está armazenando dados em buffer ou parou de armazenar em buffer os dados.</span><span class="sxs-lookup"><span data-stu-id="d9f6c-104">The graph is buffering data, or has stopped buffering data.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9f6c-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9f6c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9f6c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d9f6c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d9f6c-107">(**Bool**) **True** se o grafo estiver começando a ser armazenado em buffer ou **false** se o grafo tiver parado de armazenar em buffer.</span><span class="sxs-lookup"><span data-stu-id="d9f6c-107">(**BOOL**) **TRUE** if the graph is starting to buffer, or **FALSE** if the graph has stopped buffering.</span></span>

</dd> <dt>

<span data-ttu-id="d9f6c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d9f6c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d9f6c-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="d9f6c-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="d9f6c-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="d9f6c-110">Default Action</span></span>

<span data-ttu-id="d9f6c-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d9f6c-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9f6c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9f6c-112">Remarks</span></span>

<span data-ttu-id="d9f6c-113">Um filtro pode enviar esse evento se precisar armazenar em buffer dados de uma fonte externa.</span><span class="sxs-lookup"><span data-stu-id="d9f6c-113">A filter can send this event if it needs to buffer data from an external source.</span></span> <span data-ttu-id="d9f6c-114">(Por exemplo, ele pode estar carregando dados de uma rede). O aplicativo pode usar esse evento para ajustar sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d9f6c-114">(For example, it might be loading data from a network.) The application can use this event to adjust its user interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f6c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9f6c-115">Requirements</span></span>



| <span data-ttu-id="d9f6c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9f6c-116">Requirement</span></span> | <span data-ttu-id="d9f6c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d9f6c-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f6c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9f6c-118">Header</span></span><br/> | <dl> <span data-ttu-id="d9f6c-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9f6c-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f6c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9f6c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f6c-121">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="d9f6c-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d9f6c-122">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="d9f6c-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




