---
title: Método IMsTscAxEvents OnMouseInputModeChanged
description: Chamado quando o modo de entrada do mouse é alterado.
ms.assetid: d0554c59-967d-4181-98cd-9e88dde32752
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnMouseInputModeChanged
- Método OnMouseInputModeChanged Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnMouseInputModeChanged
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnMouseInputModeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbfef19aa79ba634a13d92b8d11866b8016e893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085769"
---
# <a name="imstscaxeventsonmouseinputmodechanged-method"></a><span data-ttu-id="16084-106">Método IMsTscAxEvents:: OnMouseInputModeChanged</span><span class="sxs-lookup"><span data-stu-id="16084-106">IMsTscAxEvents::OnMouseInputModeChanged method</span></span>

<span data-ttu-id="16084-107">Chamado quando o modo de entrada do mouse é alterado.</span><span class="sxs-lookup"><span data-stu-id="16084-107">Called when the mouse input mode has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="16084-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16084-108">Syntax</span></span>


```C++
void OnMouseInputModeChanged(
  [in] VARIANT_BOOL fMouseModeRelative
);
```



## <a name="parameters"></a><span data-ttu-id="16084-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16084-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16084-110">*fMouseModeRelative* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16084-110">*fMouseModeRelative* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16084-111">Indica se o mouse está no modo relativo.</span><span class="sxs-lookup"><span data-stu-id="16084-111">Indicates whether the mouse is in relative mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16084-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16084-112">Return value</span></span>

<span data-ttu-id="16084-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="16084-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16084-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="16084-114">Remarks</span></span>

<span data-ttu-id="16084-115">Implemente esse método em seu coletor de eventos para receber uma notificação de que o modo de entrada do mouse foi alterado.</span><span class="sxs-lookup"><span data-stu-id="16084-115">Implement this method in your event sink to receive notification that the mouse input mode has changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="16084-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16084-116">Requirements</span></span>



| <span data-ttu-id="16084-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="16084-117">Requirement</span></span> | <span data-ttu-id="16084-118">Valor</span><span class="sxs-lookup"><span data-stu-id="16084-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16084-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16084-119">Minimum supported client</span></span><br/> | <span data-ttu-id="16084-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16084-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="16084-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16084-121">Minimum supported server</span></span><br/> | <span data-ttu-id="16084-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16084-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="16084-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="16084-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="16084-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16084-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="16084-125">DLL</span><span class="sxs-lookup"><span data-stu-id="16084-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16084-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16084-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="16084-127">IID</span><span class="sxs-lookup"><span data-stu-id="16084-127">IID</span></span><br/>                      | <span data-ttu-id="16084-128">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="16084-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="16084-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="16084-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16084-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="16084-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





