---
description: Ocorreu um erro em um fluxo, mas o fluxo ainda está sendo executado.
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: EC_STREAM_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db74a9f16a0ca01ce74e6d94df50cc402221aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775560"
---
# <a name="ec_stream_error_stillplaying"></a><span data-ttu-id="8cf8b-103">\_STILLPLAYING de \_ erro de fluxo do EC \_</span><span class="sxs-lookup"><span data-stu-id="8cf8b-103">EC\_STREAM\_ERROR\_STILLPLAYING</span></span>

<span data-ttu-id="8cf8b-104">Ocorreu um erro em um fluxo, mas o fluxo ainda está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-104">An error occurred in a stream, but the stream is still playing.</span></span>

## <a name="parameters"></a><span data-ttu-id="8cf8b-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cf8b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cf8b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="8cf8b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="8cf8b-107">(**HRESULT**) Código de falha da operação que falhou.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-107">(**HRESULT**) Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="8cf8b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="8cf8b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="8cf8b-109">(**DWORD**) Código de erro secundário.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-109">(**DWORD**) Minor error code.</span></span> <span data-ttu-id="8cf8b-110">Esse valor geralmente é zero.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-110">This value is usually zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="8cf8b-111">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="8cf8b-111">Default Action</span></span>

<span data-ttu-id="8cf8b-112">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-112">None.</span></span> <span data-ttu-id="8cf8b-113">O aplicativo deve decidir se deseja parar o grafo.</span><span class="sxs-lookup"><span data-stu-id="8cf8b-113">The application must decide whether to stop the graph.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cf8b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cf8b-114">Requirements</span></span>



| <span data-ttu-id="8cf8b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cf8b-115">Requirement</span></span> | <span data-ttu-id="8cf8b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8cf8b-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf8b-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8cf8b-117">Header</span></span><br/> | <dl> <span data-ttu-id="8cf8b-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cf8b-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cf8b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cf8b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf8b-120">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="8cf8b-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="8cf8b-121">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="8cf8b-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




