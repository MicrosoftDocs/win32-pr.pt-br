---
title: Mensagem de DRV_LOAD (mmsystem. h)
description: Notifica o driver de que ele foi carregado. O driver deve certificar-se de que qualquer hardware e drivers de suporte necessários para funcionar corretamente estão presentes.
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- Multimídia do Windows de mensagem DRV_LOAD
topic_type:
- apiref
api_name:
- DRV_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dda950eaa84f924f4845d99d5740e37d6b354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919146"
---
# <a name="drv_load-message"></a><span data-ttu-id="b44ee-105">Mensagem de carregamento de DRV \_</span><span class="sxs-lookup"><span data-stu-id="b44ee-105">DRV\_LOAD message</span></span>

<span data-ttu-id="b44ee-106">Notifica o driver de que ele foi carregado.</span><span class="sxs-lookup"><span data-stu-id="b44ee-106">Notifies the driver that it has been loaded.</span></span> <span data-ttu-id="b44ee-107">O driver deve certificar-se de que qualquer hardware e drivers de suporte necessários para funcionar corretamente estão presentes.</span><span class="sxs-lookup"><span data-stu-id="b44ee-107">The driver should make sure that any hardware and supporting drivers it needs to function properly are present.</span></span>

## <a name="parameters"></a><span data-ttu-id="b44ee-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b44ee-108">Parameters</span></span>

<span data-ttu-id="b44ee-109">O parâmetro *hdrvr* é sempre zero.</span><span class="sxs-lookup"><span data-stu-id="b44ee-109">The *hdrvr* parameter is always zero.</span></span> <span data-ttu-id="b44ee-110">Os parâmetros *dwDriverId*, *lParam1* e *lParam2* não são usados.</span><span class="sxs-lookup"><span data-stu-id="b44ee-110">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b44ee-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b44ee-111">Return Value</span></span>

<span data-ttu-id="b44ee-112">Retornará zero, se for bem-sucedido ou zero.</span><span class="sxs-lookup"><span data-stu-id="b44ee-112">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b44ee-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b44ee-113">Remarks</span></span>

<span data-ttu-id="b44ee-114">A mensagem de **\_ carregamento de drv** é sempre a primeira mensagem que um driver de dispositivo recebe.</span><span class="sxs-lookup"><span data-stu-id="b44ee-114">The **DRV\_LOAD** message is always the first message that a device driver receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="b44ee-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b44ee-115">Requirements</span></span>



| <span data-ttu-id="b44ee-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b44ee-116">Requirement</span></span> | <span data-ttu-id="b44ee-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b44ee-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b44ee-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b44ee-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b44ee-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b44ee-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b44ee-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b44ee-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b44ee-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b44ee-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b44ee-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b44ee-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b44ee-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b44ee-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b44ee-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b44ee-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b44ee-125">Drivers instaláveis</span><span class="sxs-lookup"><span data-stu-id="b44ee-125">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="b44ee-126">Mensagens de driver instaláveis</span><span class="sxs-lookup"><span data-stu-id="b44ee-126">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





