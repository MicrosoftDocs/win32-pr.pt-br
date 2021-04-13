---
title: Método IRemoteDesktopClientEvents OnKeyCombinationPressed
description: Chamado quando as combinações de teclas especiais são pressionadas na sessão remota.
ms.assetid: 0A4EAD6C-5DA9-4ED3-BA79-92AE5AE81C9F
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnKeyCombinationPressed
- Método OnKeyCombinationPressed Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientEvents
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientEvents, método OnKeyCombinationPressed
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnKeyCombinationPressed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192cad6323578a9bde9fe38af1d2b1d2cf83473c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369432"
---
# <a name="iremotedesktopclienteventsonkeycombinationpressed-method"></a><span data-ttu-id="3e50d-106">Método IRemoteDesktopClientEvents:: OnKeyCombinationPressed</span><span class="sxs-lookup"><span data-stu-id="3e50d-106">IRemoteDesktopClientEvents::OnKeyCombinationPressed method</span></span>

<span data-ttu-id="3e50d-107">Chamado quando as combinações de teclas especiais são pressionadas na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="3e50d-107">Called when special key combinations are pressed in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e50d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e50d-108">Syntax</span></span>


```C++
void OnKeyCombinationPressed(
  [in] long keyCombination
);
```



## <a name="parameters"></a><span data-ttu-id="3e50d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e50d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e50d-110">*combinação de teclas* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e50d-110">*keyCombination* \[in\]</span></span>
<span data-ttu-id="3e50d-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3e50d-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="3e50d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e50d-112">Return value</span></span>

<span data-ttu-id="3e50d-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3e50d-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e50d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e50d-114">Requirements</span></span>



| <span data-ttu-id="3e50d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e50d-115">Requirement</span></span> | <span data-ttu-id="3e50d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3e50d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e50d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e50d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3e50d-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3e50d-118">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="3e50d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e50d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3e50d-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e50d-120">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="3e50d-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3e50d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e50d-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e50d-122"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="3e50d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3e50d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e50d-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e50d-124"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="3e50d-125">IID</span><span class="sxs-lookup"><span data-stu-id="3e50d-125">IID</span></span><br/>                      | <span data-ttu-id="3e50d-126">DIID \_ IRemoteDesktopClientEvents é definido como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="3e50d-126">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3e50d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e50d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e50d-128">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="3e50d-128">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





