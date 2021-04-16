---
title: Mensagem de DRV_CLOSE (mmsystem. h)
description: Direciona o driver para fechar a instância especificada. Se nenhuma outra instância estiver aberta, o driver deverá se preparar para a versão subsequente da memória.
ms.assetid: 98d7fe47-5194-4912-a9d6-3af3d1fa4e60
keywords:
- Multimídia do Windows de mensagem DRV_CLOSE
topic_type:
- apiref
api_name:
- DRV_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a205b7e6edb4a427b0e80d32cc711d9bf2b052c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749978"
---
# <a name="drv_close-message"></a><span data-ttu-id="df91a-105">\_Mensagem de fechamento drv</span><span class="sxs-lookup"><span data-stu-id="df91a-105">DRV\_CLOSE message</span></span>

<span data-ttu-id="df91a-106">Direciona o driver para fechar a instância especificada.</span><span class="sxs-lookup"><span data-stu-id="df91a-106">Directs the driver to close the given instance.</span></span> <span data-ttu-id="df91a-107">Se nenhuma outra instância estiver aberta, o driver deverá se preparar para a versão subsequente da memória.</span><span class="sxs-lookup"><span data-stu-id="df91a-107">If no other instances are open, the driver should prepare for subsequent release from memory.</span></span>

## <a name="parameters"></a><span data-ttu-id="df91a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df91a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df91a-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="df91a-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="df91a-110">Identificador do driver instalável.</span><span class="sxs-lookup"><span data-stu-id="df91a-110">Identifier of the installable driver.</span></span> <span data-ttu-id="df91a-111">Esse é o mesmo valor retornado anteriormente pelo driver da mensagem de [**\_ abertura do drv**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="df91a-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="df91a-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="df91a-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="df91a-113">Identificador da instância de driver instalável.</span><span class="sxs-lookup"><span data-stu-id="df91a-113">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="df91a-114"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="df91a-114"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="df91a-115">valor de 32 bits especificado como o parâmetro *lParam1* em uma chamada para a função **DriverClose** .</span><span class="sxs-lookup"><span data-stu-id="df91a-115">32-bit value specified as the *lParam1* parameter in a call to the **DriverClose** function.</span></span>

</dd> <dt>

<span data-ttu-id="df91a-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="df91a-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="df91a-117">valor de 32 bits especificado como o parâmetro *lParam2* em uma chamada para a função **DriverClose** .</span><span class="sxs-lookup"><span data-stu-id="df91a-117">32-bit value specified as the *lParam2* parameter in a call to the **DriverClose** function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df91a-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="df91a-118">Return Value</span></span>

<span data-ttu-id="df91a-119">Retornará zero, se for bem-sucedido ou zero.</span><span class="sxs-lookup"><span data-stu-id="df91a-119">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="df91a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df91a-120">Requirements</span></span>



| <span data-ttu-id="df91a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="df91a-121">Requirement</span></span> | <span data-ttu-id="df91a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="df91a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df91a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df91a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="df91a-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="df91a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="df91a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df91a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="df91a-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="df91a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="df91a-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="df91a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="df91a-128"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df91a-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df91a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="df91a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df91a-130">Drivers instaláveis</span><span class="sxs-lookup"><span data-stu-id="df91a-130">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="df91a-131">Mensagens de driver instaláveis</span><span class="sxs-lookup"><span data-stu-id="df91a-131">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





