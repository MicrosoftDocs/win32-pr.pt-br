---
title: Mensagem de DRV_ENABLE (mmsystem. h)
description: Habilita o driver. O driver deve inicializar qualquer variável e localizar dispositivos com a interface de entrada e saída (e/s).
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- Multimídia do Windows de mensagem DRV_ENABLE
topic_type:
- apiref
api_name:
- DRV_ENABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569b4ca5f3d0dc5f439b1e2b0e25887ffd1da4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919151"
---
# <a name="drv_enable-message"></a><span data-ttu-id="523c1-105">\_Mensagem de habilitação de drv</span><span class="sxs-lookup"><span data-stu-id="523c1-105">DRV\_ENABLE message</span></span>

<span data-ttu-id="523c1-106">Habilita o driver.</span><span class="sxs-lookup"><span data-stu-id="523c1-106">Enables the driver.</span></span> <span data-ttu-id="523c1-107">O driver deve inicializar qualquer variável e localizar dispositivos com a interface de entrada e saída (e/s).</span><span class="sxs-lookup"><span data-stu-id="523c1-107">The driver should initialize any variables and locate devices with the input and output (I/O) interface.</span></span>

## <a name="parameters"></a><span data-ttu-id="523c1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="523c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="523c1-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="523c1-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="523c1-110">Identificador da instância de driver instalável.</span><span class="sxs-lookup"><span data-stu-id="523c1-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="523c1-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="523c1-111">Return Value</span></span>

<span data-ttu-id="523c1-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="523c1-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="523c1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="523c1-113">Remarks</span></span>

<span data-ttu-id="523c1-114">Os parâmetros *dwDriverId*, *lParam1* e *lParam2* não são usados.</span><span class="sxs-lookup"><span data-stu-id="523c1-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="523c1-115">Os drivers são considerados habilitados a partir do momento em que receberem essa mensagem até que sejam desabilitados usando a mensagem de [**\_ desativação de drv**](drv-disable.md) .</span><span class="sxs-lookup"><span data-stu-id="523c1-115">Drivers are considered enabled from the time they receive this message until they are disabled by using the [**DRV\_DISABLE**](drv-disable.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="523c1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="523c1-116">Requirements</span></span>



| <span data-ttu-id="523c1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="523c1-117">Requirement</span></span> | <span data-ttu-id="523c1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="523c1-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="523c1-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="523c1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="523c1-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="523c1-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="523c1-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="523c1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="523c1-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="523c1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="523c1-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="523c1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="523c1-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="523c1-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="523c1-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="523c1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="523c1-126">Drivers instaláveis</span><span class="sxs-lookup"><span data-stu-id="523c1-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="523c1-127">Mensagens de driver instaláveis</span><span class="sxs-lookup"><span data-stu-id="523c1-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





