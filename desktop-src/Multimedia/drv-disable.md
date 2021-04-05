---
title: Mensagem de DRV_DISABLE (mmsystem. h)
description: Desabilita o driver. O driver deve posicionar o dispositivo correspondente, se houver, em um estado inativo e encerrar quaisquer funções ou threads de retorno de chamada.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- Multimídia do Windows de mensagem DRV_DISABLE
topic_type:
- apiref
api_name:
- DRV_DISABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b512e90612a02681008474c7f1323f17304422d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919149"
---
# <a name="drv_disable-message"></a><span data-ttu-id="af177-105">\_Mensagem de desabilitação de drv</span><span class="sxs-lookup"><span data-stu-id="af177-105">DRV\_DISABLE message</span></span>

<span data-ttu-id="af177-106">Desabilita o driver.</span><span class="sxs-lookup"><span data-stu-id="af177-106">Disables the driver.</span></span> <span data-ttu-id="af177-107">O driver deve posicionar o dispositivo correspondente, se houver, em um estado inativo e encerrar quaisquer funções ou threads de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="af177-107">The driver should place the corresponding device, if any, in an inactive state and terminate any callback functions or threads.</span></span>

## <a name="parameters"></a><span data-ttu-id="af177-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af177-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af177-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="af177-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="af177-110">Identificador da instância de driver instalável.</span><span class="sxs-lookup"><span data-stu-id="af177-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af177-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="af177-111">Return Value</span></span>

<span data-ttu-id="af177-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="af177-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af177-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="af177-113">Remarks</span></span>

<span data-ttu-id="af177-114">Os parâmetros *dwDriverId*, *lParam1* e *lParam2* não são usados.</span><span class="sxs-lookup"><span data-stu-id="af177-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="af177-115">Depois de desabilitar o driver, o sistema normalmente envia o driver a uma mensagem [**drv \_ Free**](drv-free.md) antes de remover o driver da memória.</span><span class="sxs-lookup"><span data-stu-id="af177-115">After disabling the driver, the system typically sends the driver a [**DRV\_FREE**](drv-free.md) message before removing the driver from memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="af177-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af177-116">Requirements</span></span>



| <span data-ttu-id="af177-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="af177-117">Requirement</span></span> | <span data-ttu-id="af177-118">Valor</span><span class="sxs-lookup"><span data-stu-id="af177-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af177-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af177-119">Minimum supported client</span></span><br/> | <span data-ttu-id="af177-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="af177-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="af177-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af177-121">Minimum supported server</span></span><br/> | <span data-ttu-id="af177-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="af177-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="af177-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="af177-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="af177-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af177-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af177-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="af177-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af177-126">Drivers instaláveis</span><span class="sxs-lookup"><span data-stu-id="af177-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="af177-127">Mensagens de driver instaláveis</span><span class="sxs-lookup"><span data-stu-id="af177-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





