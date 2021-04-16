---
title: Mensagem de DRV_EXITSESSION (mmsystem. h)
description: Notifica o driver que o Windows está preparando para sair. O driver deve se preparar para o encerramento.
ms.assetid: 8d200d64-b89b-47f1-ad21-ab86987efa4b
keywords:
- Multimídia do Windows de mensagem DRV_EXITSESSION
topic_type:
- apiref
api_name:
- DRV_EXITSESSION
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236da457541af2d594bc708caf5b5ed07e58cc04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455957"
---
# <a name="drv_exitsession-message"></a><span data-ttu-id="d7fac-105">\_Mensagem EXITSESSION drv</span><span class="sxs-lookup"><span data-stu-id="d7fac-105">DRV\_EXITSESSION message</span></span>

<span data-ttu-id="d7fac-106">Notifica o driver que o Windows está preparando para sair.</span><span class="sxs-lookup"><span data-stu-id="d7fac-106">Notifies the driver that Windows is preparing to exit.</span></span> <span data-ttu-id="d7fac-107">O driver deve se preparar para o encerramento.</span><span class="sxs-lookup"><span data-stu-id="d7fac-107">The driver should prepare for termination.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7fac-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7fac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7fac-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="d7fac-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="d7fac-110">Identificador do driver instalável.</span><span class="sxs-lookup"><span data-stu-id="d7fac-110">Identifier of the installable driver.</span></span> <span data-ttu-id="d7fac-111">Esse é o mesmo valor retornado anteriormente pelo driver da mensagem de [**\_ abertura do drv**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="d7fac-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="d7fac-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="d7fac-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="d7fac-113">Identificador da instância de driver instalável.</span><span class="sxs-lookup"><span data-stu-id="d7fac-113">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7fac-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d7fac-114">Return Value</span></span>

<span data-ttu-id="d7fac-115">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d7fac-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7fac-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7fac-116">Remarks</span></span>

<span data-ttu-id="d7fac-117">Os parâmetros *lParam1* e *lParam2* não são usados.</span><span class="sxs-lookup"><span data-stu-id="d7fac-117">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7fac-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7fac-118">Requirements</span></span>



| <span data-ttu-id="d7fac-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7fac-119">Requirement</span></span> | <span data-ttu-id="d7fac-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d7fac-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fac-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7fac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d7fac-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7fac-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d7fac-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7fac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d7fac-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7fac-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d7fac-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d7fac-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7fac-126"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7fac-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7fac-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7fac-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7fac-128">Drivers instaláveis</span><span class="sxs-lookup"><span data-stu-id="d7fac-128">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="d7fac-129">Mensagens de driver instaláveis</span><span class="sxs-lookup"><span data-stu-id="d7fac-129">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





