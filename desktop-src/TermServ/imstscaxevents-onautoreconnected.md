---
title: Método IMsTscAxEvents OnAutoReconnected
description: Chamado quando o controle de cliente é reconectado automaticamente a uma sessão remota. | Método IMsTscAxEvents OnAutoReconnected
ms.assetid: 50307002-33F9-453C-A880-AF4111412854
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnAutoReconnected
- Método OnAutoReconnected Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnAutoReconnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29f0e9a498a727614bdfda621c214199918e2ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105787583"
---
# <a name="imstscaxeventsonautoreconnected-method"></a><span data-ttu-id="2b085-107">Método IMsTscAxEvents:: OnAutoReconnected</span><span class="sxs-lookup"><span data-stu-id="2b085-107">IMsTscAxEvents::OnAutoReconnected method</span></span>

<span data-ttu-id="2b085-108">Chamado quando o controle de cliente é reconectado automaticamente a uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="2b085-108">Called when the client control has automatically reconnected to a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b085-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b085-109">Syntax</span></span>


```C++
HRESULT OnAutoReconnected();
```



## <a name="parameters"></a><span data-ttu-id="2b085-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b085-110">Parameters</span></span>

<span data-ttu-id="2b085-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2b085-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b085-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b085-112">Return value</span></span>

<span data-ttu-id="2b085-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2b085-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2b085-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2b085-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b085-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b085-115">Requirements</span></span>



| <span data-ttu-id="2b085-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b085-116">Requirement</span></span> | <span data-ttu-id="2b085-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2b085-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b085-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b085-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2b085-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2b085-119">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="2b085-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b085-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2b085-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b085-121">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="2b085-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2b085-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b085-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b085-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b085-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2b085-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b085-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b085-125"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b085-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b085-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b085-127">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="2b085-127">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





