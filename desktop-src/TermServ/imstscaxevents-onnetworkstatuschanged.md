---
title: Método IMsTscAxEvents OnNetworkStatusChanged
description: Chamado quando o status da rede é alterado. | Método IMsTscAxEvents OnNetworkStatusChanged
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnNetworkStatusChanged
- Método OnNetworkStatusChanged Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b9bdcd7774493fcc54e1390ad199a6a56a7c51
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105756808"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a><span data-ttu-id="3d063-107">Método IMsTscAxEvents:: OnNetworkStatusChanged</span><span class="sxs-lookup"><span data-stu-id="3d063-107">IMsTscAxEvents::OnNetworkStatusChanged method</span></span>

<span data-ttu-id="3d063-108">Chamado quando o status da rede é alterado.</span><span class="sxs-lookup"><span data-stu-id="3d063-108">Called when the network status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d063-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d063-109">Syntax</span></span>


```C++
void OnNetworkStatusChanged(
  [in] ULONG qualityLevel,
  [in] LONG  bandwidth,
  [in] LONG  rtt
);
```



## <a name="parameters"></a><span data-ttu-id="3d063-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d063-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d063-111">*qualityLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3d063-111">*qualityLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d063-112">Especifica a nova velocidade de conexão.</span><span class="sxs-lookup"><span data-stu-id="3d063-112">Specifies the new connection speed.</span></span> <span data-ttu-id="3d063-113">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3d063-113">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="3d063-114">1</span><span class="sxs-lookup"><span data-stu-id="3d063-114">1</span></span>
</dt> <dd>

<span data-ttu-id="3d063-115">Menos de 512 quilobytes por segundo (KBps).</span><span class="sxs-lookup"><span data-stu-id="3d063-115">Less than 512 kilobytes per second (KBps).</span></span>

</dd> <dt>

<span data-ttu-id="3d063-116">2</span><span class="sxs-lookup"><span data-stu-id="3d063-116">2</span></span>
</dt> <dd>

<span data-ttu-id="3d063-117">512 a 1.999 KBps.</span><span class="sxs-lookup"><span data-stu-id="3d063-117">512 to 1,999 KBps.</span></span>

</dd> <dt>

<span data-ttu-id="3d063-118">3</span><span class="sxs-lookup"><span data-stu-id="3d063-118">3</span></span>
</dt> <dd>

<span data-ttu-id="3d063-119">2.000 a 9.999 KBps.</span><span class="sxs-lookup"><span data-stu-id="3d063-119">2,000 to 9,999 KBps.</span></span>

</dd> <dt>

<span data-ttu-id="3d063-120">4</span><span class="sxs-lookup"><span data-stu-id="3d063-120">4</span></span>
</dt> <dd>

<span data-ttu-id="3d063-121">Maior ou igual a 10.000 KBps.</span><span class="sxs-lookup"><span data-stu-id="3d063-121">Greater than or equal to 10,000 KBps.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3d063-122">*largura de banda* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3d063-122">*bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d063-123">Especifica a largura de banda da conexão.</span><span class="sxs-lookup"><span data-stu-id="3d063-123">Specifies the connection bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="3d063-124">*RTT* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3d063-124">*rtt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d063-125">Especifica a latência de conexão.</span><span class="sxs-lookup"><span data-stu-id="3d063-125">Specifies the connection latency.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d063-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3d063-126">Return value</span></span>

<span data-ttu-id="3d063-127">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3d063-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d063-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d063-128">Requirements</span></span>



| <span data-ttu-id="3d063-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d063-129">Requirement</span></span> | <span data-ttu-id="3d063-130">Valor</span><span class="sxs-lookup"><span data-stu-id="3d063-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d063-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d063-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3d063-132">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3d063-132">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="3d063-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d063-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3d063-134">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d063-134">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="3d063-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3d063-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="3d063-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d063-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3d063-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3d063-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d063-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d063-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3d063-139">IID</span><span class="sxs-lookup"><span data-stu-id="3d063-139">IID</span></span><br/>                      | <span data-ttu-id="3d063-140">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="3d063-140">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="3d063-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d063-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d063-142">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="3d063-142">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





