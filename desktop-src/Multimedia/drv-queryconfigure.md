---
title: Mensagem de DRV_QUERYCONFIGURE (mmsystem. h)
description: Direciona o driver para especificar se ele oferece suporte à configuração personalizada.
ms.assetid: fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc
keywords:
- Multimídia do Windows de mensagem DRV_QUERYCONFIGURE
topic_type:
- apiref
api_name:
- DRV_QUERYCONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66780106fdd42364d247db534a838842f25dc16a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163615"
---
# <a name="drv_queryconfigure-message"></a><span data-ttu-id="6691b-104">\_Mensagem QUERYCONFIGURE drv</span><span class="sxs-lookup"><span data-stu-id="6691b-104">DRV\_QUERYCONFIGURE message</span></span>

<span data-ttu-id="6691b-105">Direciona o driver para especificar se ele oferece suporte à configuração personalizada.</span><span class="sxs-lookup"><span data-stu-id="6691b-105">Directs the driver to specify whether it supports custom configuration.</span></span>

## <a name="parameters"></a><span data-ttu-id="6691b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6691b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6691b-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="6691b-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="6691b-108">Identificador do driver instalável.</span><span class="sxs-lookup"><span data-stu-id="6691b-108">Identifier of the installable driver.</span></span> <span data-ttu-id="6691b-109">Esse é o mesmo valor retornado anteriormente pelo driver da mensagem de [**\_ abertura do drv**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="6691b-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="6691b-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="6691b-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="6691b-111">Identificador da instância de driver instalável.</span><span class="sxs-lookup"><span data-stu-id="6691b-111">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6691b-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6691b-112">Return Value</span></span>

<span data-ttu-id="6691b-113">Retorna um valor diferente de zero se o driver pode exibir uma caixa de diálogo de configuração ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6691b-113">Returns a nonzero value if the driver can display a configuration dialog box or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6691b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6691b-114">Remarks</span></span>

<span data-ttu-id="6691b-115">Os parâmetros *lParam1* e *lParam2* não são usados.</span><span class="sxs-lookup"><span data-stu-id="6691b-115">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6691b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6691b-116">Requirements</span></span>



| <span data-ttu-id="6691b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6691b-117">Requirement</span></span> | <span data-ttu-id="6691b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6691b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6691b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6691b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6691b-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6691b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6691b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6691b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6691b-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6691b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6691b-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6691b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6691b-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6691b-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6691b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6691b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6691b-126">Drivers instaláveis</span><span class="sxs-lookup"><span data-stu-id="6691b-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="6691b-127">Mensagens de driver instaláveis</span><span class="sxs-lookup"><span data-stu-id="6691b-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





