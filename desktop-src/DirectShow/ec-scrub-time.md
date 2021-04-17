---
description: Especifica o carimbo de data/hora para a etapa de quadro mais recente.
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: EC_SCRUB_TIME (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530362520f8e80ef06a769383f82dee1d60d66c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786978"
---
# <a name="ec_scrub_time"></a><span data-ttu-id="ea649-103">\_hora de limpeza do EC \_</span><span class="sxs-lookup"><span data-stu-id="ea649-103">EC\_SCRUB\_TIME</span></span>

<span data-ttu-id="ea649-104">Especifica o carimbo de data/hora para a etapa de quadro mais recente.</span><span class="sxs-lookup"><span data-stu-id="ea649-104">Specifies the time stamp for the most recent frame step.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea649-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea649-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea649-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ea649-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ea649-107">(**DWORD**) Menores 32 bits do carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="ea649-107">(**DWORD**) Lower 32 bits of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="ea649-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ea649-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ea649-109">(**DWORD**) Os bits superiores a 32 do carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="ea649-109">(**DWORD**) Upper 32 bits of the time stamp.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="ea649-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="ea649-110">Default Action</span></span>

<span data-ttu-id="ea649-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ea649-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea649-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea649-112">Remarks</span></span>

<span data-ttu-id="ea649-113">O apresentador do filtro EVR ( [**processador de vídeo avançado**](enhanced-video-renderer-filter.md) ) envia essa mensagem para o EVR quando ele conclui uma etapa de quadro.</span><span class="sxs-lookup"><span data-stu-id="ea649-113">The presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter sends this message to the EVR when it completes a frame step.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea649-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea649-114">Requirements</span></span>



| <span data-ttu-id="ea649-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea649-115">Requirement</span></span> | <span data-ttu-id="ea649-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ea649-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea649-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea649-117">Header</span></span><br/> | <dl> <span data-ttu-id="ea649-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea649-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea649-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea649-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea649-120">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="ea649-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> </dl>

 

 




