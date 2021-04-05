---
title: Mensagem de DRV_REMOVE (mmsystem. h)
description: Notifica o driver que ele está prestes a ser removido do sistema. Quando um driver recebe essa mensagem, ele deve remover todas as seções criadas no registro.
ms.assetid: e4f6ce7c-29e5-4256-b08a-13571256207c
keywords:
- Multimídia do Windows de mensagem DRV_REMOVE
topic_type:
- apiref
api_name:
- DRV_REMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfc94d648f83e618a20323ed7bbe3694616bc06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009749"
---
# <a name="drv_remove-message"></a><span data-ttu-id="c4ba9-105">\_Remoção de mensagem drv</span><span class="sxs-lookup"><span data-stu-id="c4ba9-105">DRV\_REMOVE message</span></span>

<span data-ttu-id="c4ba9-106">Notifica o driver que ele está prestes a ser removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="c4ba9-106">Notifies the driver that it is about to be removed from the system.</span></span> <span data-ttu-id="c4ba9-107">Quando um driver recebe essa mensagem, ele deve remover todas as seções criadas no registro.</span><span class="sxs-lookup"><span data-stu-id="c4ba9-107">When a driver receives this message, it should remove any sections it created in the registry.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4ba9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4ba9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4ba9-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="c4ba9-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="c4ba9-110">Identificador do driver instalável.</span><span class="sxs-lookup"><span data-stu-id="c4ba9-110">Identifier of the installable driver.</span></span> <span data-ttu-id="c4ba9-111">Esse é o mesmo valor retornado anteriormente pelo driver da mensagem de [**\_ abertura do drv**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="c4ba9-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="c4ba9-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="c4ba9-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="c4ba9-113">Identificador da instância de driver instalável.</span><span class="sxs-lookup"><span data-stu-id="c4ba9-113">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4ba9-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c4ba9-114">Return Value</span></span>

<span data-ttu-id="c4ba9-115">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="c4ba9-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4ba9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4ba9-116">Remarks</span></span>

<span data-ttu-id="c4ba9-117">Os parâmetros *lParam1* e *lParam2* não são usados.</span><span class="sxs-lookup"><span data-stu-id="c4ba9-117">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4ba9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4ba9-118">Requirements</span></span>



| <span data-ttu-id="c4ba9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4ba9-119">Requirement</span></span> | <span data-ttu-id="c4ba9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c4ba9-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ba9-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4ba9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c4ba9-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c4ba9-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c4ba9-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4ba9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c4ba9-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c4ba9-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c4ba9-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c4ba9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4ba9-126"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4ba9-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4ba9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4ba9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4ba9-128">Drivers instaláveis</span><span class="sxs-lookup"><span data-stu-id="c4ba9-128">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="c4ba9-129">Mensagens de driver instaláveis</span><span class="sxs-lookup"><span data-stu-id="c4ba9-129">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





