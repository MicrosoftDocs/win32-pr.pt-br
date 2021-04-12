---
title: Método onstatuschanged do IRemoteDesktopClientEvents (Locationapi. h)
description: Chamado quando o controle de cliente atualizou seu status.
ms.assetid: AAFBDC9E-C8B5-4924-AA69-82EF09996AF7
ms.tgt_platform: multiple
keywords:
- Método onstatuschanged Serviços de Área de Trabalho Remota
- Método onstatuschanged Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientEvents
- Interface IRemoteDesktopClientEvents Serviços de Área de Trabalho Remota, método onstatuschanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b17e42e75072033f952c7ef790365d6a363a5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455867"
---
# <a name="iremotedesktopclienteventsonstatuschanged-method"></a><span data-ttu-id="408b0-106">Método IRemoteDesktopClientEvents:: onstatuschanged</span><span class="sxs-lookup"><span data-stu-id="408b0-106">IRemoteDesktopClientEvents::OnStatusChanged method</span></span>

<span data-ttu-id="408b0-107">Chamado quando o controle de cliente atualizou seu status.</span><span class="sxs-lookup"><span data-stu-id="408b0-107">Called when the client control has updated its status.</span></span>

## <a name="syntax"></a><span data-ttu-id="408b0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="408b0-108">Syntax</span></span>


```C++
void OnStatusChanged(
   long statusCode,
   BSTR statusMessage
);
```



## <a name="parameters"></a><span data-ttu-id="408b0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="408b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="408b0-110">*statusCode*</span><span class="sxs-lookup"><span data-stu-id="408b0-110">*statusCode*</span></span> 
</dt> <dd>

<span data-ttu-id="408b0-111">O novo código de status.</span><span class="sxs-lookup"><span data-stu-id="408b0-111">The new status code.</span></span>

</dd> <dt>

<span data-ttu-id="408b0-112">*statusMessage*</span><span class="sxs-lookup"><span data-stu-id="408b0-112">*statusMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="408b0-113">O texto da mensagem de status.</span><span class="sxs-lookup"><span data-stu-id="408b0-113">The status message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="408b0-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="408b0-114">Return value</span></span>

<span data-ttu-id="408b0-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="408b0-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="408b0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="408b0-116">Requirements</span></span>



| <span data-ttu-id="408b0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="408b0-117">Requirement</span></span> | <span data-ttu-id="408b0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="408b0-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="408b0-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="408b0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="408b0-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="408b0-120">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="408b0-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="408b0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="408b0-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="408b0-122">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="408b0-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="408b0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="408b0-124"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="408b0-124"><dt>Locationapi.h</dt></span></span> </dl>       |
| <span data-ttu-id="408b0-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="408b0-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="408b0-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="408b0-126"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="408b0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="408b0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="408b0-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="408b0-128"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="408b0-129">IID</span><span class="sxs-lookup"><span data-stu-id="408b0-129">IID</span></span><br/>                      | <span data-ttu-id="408b0-130">DIID \_ IRemoteDesktopClientEvents é definido como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="408b0-130">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="408b0-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="408b0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="408b0-132">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="408b0-132">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





