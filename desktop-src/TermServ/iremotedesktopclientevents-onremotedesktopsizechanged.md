---
title: Método IRemoteDesktopClientEvents OnRemoteDesktopSizeChanged
description: Chamado quando o tamanho da área de trabalho remota é alterado.
ms.assetid: DA641CA7-3214-4DB6-9A7F-75903FE93DB4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnRemoteDesktopSizeChanged
- Método OnRemoteDesktopSizeChanged Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientEvents
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientEvents, método OnRemoteDesktopSizeChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnRemoteDesktopSizeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7431d1a6f41a6f87bb34fe1486c203168f2c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644604"
---
# <a name="iremotedesktopclienteventsonremotedesktopsizechanged-method"></a><span data-ttu-id="9643d-106">Método IRemoteDesktopClientEvents:: OnRemoteDesktopSizeChanged</span><span class="sxs-lookup"><span data-stu-id="9643d-106">IRemoteDesktopClientEvents::OnRemoteDesktopSizeChanged method</span></span>

<span data-ttu-id="9643d-107">Chamado quando o tamanho da área de trabalho remota é alterado.</span><span class="sxs-lookup"><span data-stu-id="9643d-107">Called when the remote desktop size has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9643d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9643d-108">Syntax</span></span>


```C++
void OnRemoteDesktopSizeChanged(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a><span data-ttu-id="9643d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9643d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9643d-110">*largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9643d-110">*width* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9643d-111">*altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9643d-111">*height* \[in\]</span></span>
<span data-ttu-id="9643d-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9643d-112"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="9643d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9643d-113">Return value</span></span>

<span data-ttu-id="9643d-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9643d-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9643d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9643d-115">Requirements</span></span>



| <span data-ttu-id="9643d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9643d-116">Requirement</span></span> | <span data-ttu-id="9643d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9643d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9643d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9643d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9643d-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9643d-119">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="9643d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9643d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9643d-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9643d-121">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="9643d-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9643d-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="9643d-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9643d-123"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="9643d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9643d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9643d-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9643d-125"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="9643d-126">IID</span><span class="sxs-lookup"><span data-stu-id="9643d-126">IID</span></span><br/>                      | <span data-ttu-id="9643d-127">DIID \_ IRemoteDesktopClientEvents é definido como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="9643d-127">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9643d-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9643d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9643d-129">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="9643d-129">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





