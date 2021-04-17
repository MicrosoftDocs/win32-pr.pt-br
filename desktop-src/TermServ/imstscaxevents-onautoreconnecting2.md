---
title: Método IMsTscAxEvents OnAutoReconnecting2
description: Chamado quando um cliente está no processo de reconexão automática de uma sessão com um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). | Método IMsTscAxEvents OnAutoReconnecting2
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnAutoReconnecting2
- Método OnAutoReconnecting2 Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnAutoReconnecting2
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901bb196922d1772782ab7f1c911c96573c88b36
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105759937"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a><span data-ttu-id="7a595-107">Método IMsTscAxEvents:: OnAutoReconnecting2</span><span class="sxs-lookup"><span data-stu-id="7a595-107">IMsTscAxEvents::OnAutoReconnecting2 method</span></span>

<span data-ttu-id="7a595-108">Chamado quando um cliente está no processo de reconexão automática de uma sessão com um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="7a595-108">Called when a client is in the process of automatically reconnecting a session with a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="7a595-109">Esta é uma versão aprimorada do método [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) .</span><span class="sxs-lookup"><span data-stu-id="7a595-109">This is an enhanced version of the [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a595-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a595-110">Syntax</span></span>


```C++
void OnAutoReconnecting2(
  [in] LONG         disconnectReason,
  [in] VARIANT_BOOL networkAvailable,
  [in] LONG         attemptCount,
  [in] LONG         maxAttemptCount
);
```



## <a name="parameters"></a><span data-ttu-id="7a595-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a595-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a595-112">*disconnectReason* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a595-112">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a595-113">Código que descreve o motivo para a última desconexão da sessão.</span><span class="sxs-lookup"><span data-stu-id="7a595-113">Code that describes the reason for the last session disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="7a595-114">*NetworkAvailable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a595-114">*networkAvailable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a595-115">Especifica se a rede está disponível.</span><span class="sxs-lookup"><span data-stu-id="7a595-115">Specifies if the network is available.</span></span>

</dd> <dt>

<span data-ttu-id="7a595-116">*attemptCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a595-116">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a595-117">Número de tentativas que foram feitas no processo de reconexão automática atual.</span><span class="sxs-lookup"><span data-stu-id="7a595-117">Number of attempts that have been made in the current automatic reconnection process.</span></span> <span data-ttu-id="7a595-118">Essa contagem aumenta em uma para cada tentativa feita.</span><span class="sxs-lookup"><span data-stu-id="7a595-118">This count increases by one for each attempt made.</span></span>

</dd> <dt>

<span data-ttu-id="7a595-119">*maxAttemptCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a595-119">*maxAttemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a595-120">O número máximo de tentativas que serão feitas no processo de reconexão automática atual.</span><span class="sxs-lookup"><span data-stu-id="7a595-120">The maximum number of attempts that will be made in the current automatic reconnection process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a595-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a595-121">Return value</span></span>

<span data-ttu-id="7a595-122">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7a595-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a595-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a595-123">Requirements</span></span>



| <span data-ttu-id="7a595-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a595-124">Requirement</span></span> | <span data-ttu-id="7a595-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7a595-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a595-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a595-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7a595-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7a595-127">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="7a595-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a595-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7a595-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a595-129">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="7a595-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7a595-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a595-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a595-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a595-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7a595-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a595-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a595-133"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a595-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a595-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a595-135">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="7a595-135">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





