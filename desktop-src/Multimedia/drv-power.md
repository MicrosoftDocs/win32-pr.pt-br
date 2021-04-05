---
title: Mensagem de DRV_POWER (mmsystem. h)
description: Notifica o driver de que a alimentação do dispositivo está sendo ativada ou desativada.
ms.assetid: b3bbd16a-5b90-4127-a1dd-f2ddfd918f0a
keywords:
- Multimídia do Windows de mensagem DRV_POWER
topic_type:
- apiref
api_name:
- DRV_POWER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8113b7fe544bf36a35b6e516c7a98ae71082577d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919144"
---
# <a name="drv_power-message"></a><span data-ttu-id="352a4-104">\_Mensagem de energia drv</span><span class="sxs-lookup"><span data-stu-id="352a4-104">DRV\_POWER message</span></span>

<span data-ttu-id="352a4-105">Notifica o driver de que a alimentação do dispositivo está sendo ativada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="352a4-105">Notifies the driver that power to the device is being turned on or off.</span></span>

## <a name="parameters"></a><span data-ttu-id="352a4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="352a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="352a4-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="352a4-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="352a4-108">Identificador do driver instalável.</span><span class="sxs-lookup"><span data-stu-id="352a4-108">Identifier of the installable driver.</span></span> <span data-ttu-id="352a4-109">Esse é o mesmo valor retornado anteriormente pelo driver da mensagem de [**\_ abertura do drv**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="352a4-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="352a4-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="352a4-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="352a4-111">Identificador da instância de driver instalável.</span><span class="sxs-lookup"><span data-stu-id="352a4-111">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="352a4-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="352a4-112">Return Value</span></span>

<span data-ttu-id="352a4-113">Retornará zero, se for bem-sucedido ou zero.</span><span class="sxs-lookup"><span data-stu-id="352a4-113">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="352a4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="352a4-114">Remarks</span></span>

<span data-ttu-id="352a4-115">Os parâmetros *lParam1* e *lParam2* não são usados.</span><span class="sxs-lookup"><span data-stu-id="352a4-115">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="352a4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="352a4-116">Requirements</span></span>



| <span data-ttu-id="352a4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="352a4-117">Requirement</span></span> | <span data-ttu-id="352a4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="352a4-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="352a4-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="352a4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="352a4-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="352a4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="352a4-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="352a4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="352a4-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="352a4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="352a4-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="352a4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="352a4-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="352a4-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="352a4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="352a4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="352a4-126">Drivers instaláveis</span><span class="sxs-lookup"><span data-stu-id="352a4-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="352a4-127">Mensagens de driver instaláveis</span><span class="sxs-lookup"><span data-stu-id="352a4-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





