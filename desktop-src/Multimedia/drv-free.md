---
title: Mensagem de DRV_FREE (mmsystem. h)
description: Notifica o driver de que ele está sendo removido da memória. O driver deve liberar qualquer memória e outros recursos do sistema alocados.
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- Multimídia do Windows de mensagem DRV_FREE
topic_type:
- apiref
api_name:
- DRV_FREE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb9d70d269cb84e0d6ef0881618b67cfef11068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919148"
---
# <a name="drv_free-message"></a><span data-ttu-id="267ec-105">Mensagem do DRV \_ Free</span><span class="sxs-lookup"><span data-stu-id="267ec-105">DRV\_FREE message</span></span>

<span data-ttu-id="267ec-106">Notifica o driver de que ele está sendo removido da memória.</span><span class="sxs-lookup"><span data-stu-id="267ec-106">Notifies the driver that it is being removed from memory.</span></span> <span data-ttu-id="267ec-107">O driver deve liberar qualquer memória e outros recursos do sistema alocados.</span><span class="sxs-lookup"><span data-stu-id="267ec-107">The driver should free any memory and other system resources that it has allocated.</span></span>

## <a name="parameters"></a><span data-ttu-id="267ec-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="267ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="267ec-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="267ec-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="267ec-110">Identificador da instância de driver instalável.</span><span class="sxs-lookup"><span data-stu-id="267ec-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="267ec-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="267ec-111">Return Value</span></span>

<span data-ttu-id="267ec-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="267ec-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="267ec-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="267ec-113">Remarks</span></span>

<span data-ttu-id="267ec-114">Os parâmetros *dwDriverId*, *lParam1* e *lParam2* não são usados.</span><span class="sxs-lookup"><span data-stu-id="267ec-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="267ec-115">A mensagem **drv \_ Free** é sempre a última mensagem que um driver de dispositivo recebe.</span><span class="sxs-lookup"><span data-stu-id="267ec-115">The **DRV\_FREE** message is always the last message that a device driver receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="267ec-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="267ec-116">Requirements</span></span>



| <span data-ttu-id="267ec-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="267ec-117">Requirement</span></span> | <span data-ttu-id="267ec-118">Valor</span><span class="sxs-lookup"><span data-stu-id="267ec-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="267ec-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="267ec-119">Minimum supported client</span></span><br/> | <span data-ttu-id="267ec-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="267ec-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="267ec-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="267ec-121">Minimum supported server</span></span><br/> | <span data-ttu-id="267ec-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="267ec-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="267ec-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="267ec-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="267ec-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="267ec-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="267ec-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="267ec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="267ec-126">Drivers instaláveis</span><span class="sxs-lookup"><span data-stu-id="267ec-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="267ec-127">Mensagens de driver instaláveis</span><span class="sxs-lookup"><span data-stu-id="267ec-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





