---
description: Falha em um comando assíncrono para executar o grafo.
ms.assetid: 0bfcf4b4-b35a-4593-9956-8e1e8c9139cb
title: EC_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1c99db8c6b332ad4531f04171d960c5cfa9824
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782197"
---
# <a name="ec_error_stillplaying"></a><span data-ttu-id="56838-103">\_STILLPLAYING de erro do EC \_</span><span class="sxs-lookup"><span data-stu-id="56838-103">EC\_ERROR\_STILLPLAYING</span></span>

<span data-ttu-id="56838-104">Falha em um comando assíncrono para executar o grafo.</span><span class="sxs-lookup"><span data-stu-id="56838-104">An asynchronous command to run the graph has failed.</span></span>

## <a name="parameters"></a><span data-ttu-id="56838-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56838-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56838-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="56838-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="56838-107">(**HRESULT**) Código de falha da operação que falhou.</span><span class="sxs-lookup"><span data-stu-id="56838-107">(**HRESULT**) Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="56838-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="56838-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="56838-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="56838-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="56838-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="56838-110">Default Action</span></span>

<span data-ttu-id="56838-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="56838-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="56838-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="56838-112">Remarks</span></span>

<span data-ttu-id="56838-113">Se o Gerenciador de gráfico de filtro emitir um comando de execução assíncrona que falha, ele enviará esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="56838-113">If the filter graph manager issues an asynchronous run command that fails, it sends this event to the application.</span></span> <span data-ttu-id="56838-114">O grafo permanece em estado de execução.</span><span class="sxs-lookup"><span data-stu-id="56838-114">The graph remains in a running state.</span></span> <span data-ttu-id="56838-115">O estado dos filtros subjacentes é indeterminado.</span><span class="sxs-lookup"><span data-stu-id="56838-115">The state of the underlying filters is indeterminate.</span></span> <span data-ttu-id="56838-116">Alguns filtros podem estar em execução, outros podem não.</span><span class="sxs-lookup"><span data-stu-id="56838-116">Some filters might be running, others might not.</span></span>

## <a name="requirements"></a><span data-ttu-id="56838-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56838-117">Requirements</span></span>



| <span data-ttu-id="56838-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="56838-118">Requirement</span></span> | <span data-ttu-id="56838-119">Valor</span><span class="sxs-lookup"><span data-stu-id="56838-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="56838-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56838-120">Header</span></span><br/> | <dl> <span data-ttu-id="56838-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="56838-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56838-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="56838-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56838-123">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="56838-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="56838-124">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="56838-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




