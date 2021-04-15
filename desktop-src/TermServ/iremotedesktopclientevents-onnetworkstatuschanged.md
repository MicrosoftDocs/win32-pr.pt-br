---
title: Método IRemoteDesktopClientEvents OnNetworkStatusChanged
description: Chamado quando o status da rede é alterado. | Método IRemoteDesktopClientEvents OnNetworkStatusChanged
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnNetworkStatusChanged
- Método OnNetworkStatusChanged Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientEvents
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientEvents, método OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de64d8b16ea9acf9defc976d4baa91afd64f8fa7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506397"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a><span data-ttu-id="36208-107">Método IRemoteDesktopClientEvents:: OnNetworkStatusChanged</span><span class="sxs-lookup"><span data-stu-id="36208-107">IRemoteDesktopClientEvents::OnNetworkStatusChanged method</span></span>

<span data-ttu-id="36208-108">Chamado quando o status da rede é alterado.</span><span class="sxs-lookup"><span data-stu-id="36208-108">Called when the network status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="36208-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36208-109">Syntax</span></span>


```C++
void OnNetworkStatusChanged(
  [in] unsigned long qualityLevel,
  [in] long          bandwidth,
  [in] long          rtt
);
```



## <a name="parameters"></a><span data-ttu-id="36208-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36208-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36208-111">*qualityLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="36208-111">*qualityLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36208-112">O novo nível de qualidade da conexão.</span><span class="sxs-lookup"><span data-stu-id="36208-112">The new quality level of the connection.</span></span> <span data-ttu-id="36208-113">O nível de qualidade é determinado da largura de banda e dos valores de RTT (tempo de ida e volta).</span><span class="sxs-lookup"><span data-stu-id="36208-113">The quality level is determined from the bandwidth and round-trip time (rtt) values.</span></span>

<span data-ttu-id="36208-114">Um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="36208-114">One of the following values.</span></span>



| <span data-ttu-id="36208-115">Valor</span><span class="sxs-lookup"><span data-stu-id="36208-115">Value</span></span>                                                                        | <span data-ttu-id="36208-116">Significado</span><span class="sxs-lookup"><span data-stu-id="36208-116">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="36208-117"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="36208-117"><dt>0</dt></span></span> </dl> | <span data-ttu-id="36208-118">Não foi possível determinar o nível de qualidade.</span><span class="sxs-lookup"><span data-stu-id="36208-118">The quality level could not be determined.</span></span><br/>       |
| <dl> <span data-ttu-id="36208-119"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="36208-119"><dt>1</dt></span></span> </dl> | <span data-ttu-id="36208-120">A qualidade da conexão é ruim (uma barra).</span><span class="sxs-lookup"><span data-stu-id="36208-120">The connection quality is poor (one bar).</span></span><br/>        |
| <dl> <span data-ttu-id="36208-121"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="36208-121"><dt>2</dt></span></span> </dl> | <span data-ttu-id="36208-122">A qualidade da conexão é justa (duas barras).</span><span class="sxs-lookup"><span data-stu-id="36208-122">The connection quality is fair (two bars).</span></span><br/>       |
| <dl> <span data-ttu-id="36208-123"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="36208-123"><dt>3</dt></span></span> </dl> | <span data-ttu-id="36208-124">A qualidade da conexão é boa (três barras).</span><span class="sxs-lookup"><span data-stu-id="36208-124">The connection quality is good (three bars).</span></span><br/>     |
| <dl> <span data-ttu-id="36208-125"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="36208-125"><dt>4</dt></span></span> </dl> | <span data-ttu-id="36208-126">A qualidade da conexão é excelente (quatro barras).</span><span class="sxs-lookup"><span data-stu-id="36208-126">The connection quality is excellent (four bars).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="36208-127">*largura de banda* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="36208-127">*bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36208-128">Especifica a nova largura de banda de conexão, em kilobits por segundo (Kbps).</span><span class="sxs-lookup"><span data-stu-id="36208-128">Specifies the new connection bandwidth, in kilobits per second (Kbps).</span></span>

</dd> <dt>

<span data-ttu-id="36208-129">*RTT* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="36208-129">*rtt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36208-130">Especifica o novo tempo de ida e volta da conexão (latência), em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="36208-130">Specifies the new connection roundtrip time (latency), in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36208-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36208-131">Return value</span></span>

<span data-ttu-id="36208-132">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="36208-132">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="36208-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36208-133">Requirements</span></span>



| <span data-ttu-id="36208-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="36208-134">Requirement</span></span> | <span data-ttu-id="36208-135">Valor</span><span class="sxs-lookup"><span data-stu-id="36208-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36208-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36208-136">Minimum supported client</span></span><br/> | <span data-ttu-id="36208-137">Windows 8</span><span class="sxs-lookup"><span data-stu-id="36208-137">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="36208-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36208-138">Minimum supported server</span></span><br/> | <span data-ttu-id="36208-139">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36208-139">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="36208-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="36208-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="36208-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36208-141"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="36208-142">DLL</span><span class="sxs-lookup"><span data-stu-id="36208-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36208-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36208-143"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="36208-144">IID</span><span class="sxs-lookup"><span data-stu-id="36208-144">IID</span></span><br/>                      | <span data-ttu-id="36208-145">DIID \_ IRemoteDesktopClientEvents é definido como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="36208-145">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="36208-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="36208-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36208-147">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="36208-147">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





