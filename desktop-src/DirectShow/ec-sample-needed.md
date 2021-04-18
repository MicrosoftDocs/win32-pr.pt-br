---
description: Solicita uma nova amostra de entrada do filtro EVR (processador de vídeo avançado).
ms.assetid: f1bf32ba-ecb7-435f-aefc-f60fdd355620
title: EC_SAMPLE_NEEDED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da73d02604e128fdf94edb8f84d1526cfcdb586e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812832"
---
# <a name="ec_sample_needed"></a><span data-ttu-id="5af9a-103">exemplo de EC \_ \_ necessário</span><span class="sxs-lookup"><span data-stu-id="5af9a-103">EC\_SAMPLE\_NEEDED</span></span>

<span data-ttu-id="5af9a-104">Solicita uma nova amostra de entrada do filtro EVR ( [**processador de vídeo avançado**](enhanced-video-renderer-filter.md) ).</span><span class="sxs-lookup"><span data-stu-id="5af9a-104">Requests a new input sample from the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="5af9a-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5af9a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5af9a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="5af9a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="5af9a-107">Identificador do fluxo de entrada que precisa de nova entrada.</span><span class="sxs-lookup"><span data-stu-id="5af9a-107">Identifier of the input stream that needs new input.</span></span>

</dd> <dt>

<span data-ttu-id="5af9a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="5af9a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="5af9a-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="5af9a-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="5af9a-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="5af9a-110">Default Action</span></span>

<span data-ttu-id="5af9a-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5af9a-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="5af9a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5af9a-112">Remarks</span></span>

<span data-ttu-id="5af9a-113">O mixer do filtro EVR envia essa mensagem quando precisa de um novo exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="5af9a-113">The mixer for the EVR filter sends this message when it needs a new input sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="5af9a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5af9a-114">Requirements</span></span>



| <span data-ttu-id="5af9a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5af9a-115">Requirement</span></span> | <span data-ttu-id="5af9a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5af9a-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5af9a-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5af9a-117">Header</span></span><br/> | <dl> <span data-ttu-id="5af9a-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="5af9a-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5af9a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5af9a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af9a-120">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="5af9a-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> </dl>

 

 




