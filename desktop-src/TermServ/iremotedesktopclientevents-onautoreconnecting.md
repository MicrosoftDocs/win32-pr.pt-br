---
title: Método IRemoteDesktopClientEvents OnAutoReconnecting
description: Chamado quando o controle de cliente tenta restabelecer automaticamente uma conexão com uma sessão remota.
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnAutoReconnecting
- Método OnAutoReconnecting Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientEvents
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientEvents, método OnAutoReconnecting
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74c37919384727fdf51aad004349478798a3ffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499784"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a><span data-ttu-id="09e0d-106">Método IRemoteDesktopClientEvents:: OnAutoReconnecting</span><span class="sxs-lookup"><span data-stu-id="09e0d-106">IRemoteDesktopClientEvents::OnAutoReconnecting method</span></span>

<span data-ttu-id="09e0d-107">Chamado quando o controle de cliente tenta restabelecer automaticamente uma conexão com uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="09e0d-107">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e0d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09e0d-108">Syntax</span></span>


```C++
void OnAutoReconnecting(
  [in] long         disconnectReason,
  [in] long         ExtendedDisconnectReason,
  [in] BSTR         disconnectErrorMessage,
  [in] VARIANT_BOOL networkAvailable,
  [in] long         attemptCount,
  [in] long         maxAttemptCount
);
```



## <a name="parameters"></a><span data-ttu-id="09e0d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09e0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09e0d-110">*disconnectReason* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09e0d-110">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e0d-111">O motivo para o evento de desconexão.</span><span class="sxs-lookup"><span data-stu-id="09e0d-111">The reason for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="09e0d-112">*ExtendedDisconnectReason* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09e0d-112">*ExtendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e0d-113">Informações estendidas para o evento de desconexão.</span><span class="sxs-lookup"><span data-stu-id="09e0d-113">Extended information for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="09e0d-114">*disconnectErrorMessage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09e0d-114">*disconnectErrorMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e0d-115">A mensagem de erro para o evento de desconexão.</span><span class="sxs-lookup"><span data-stu-id="09e0d-115">The error message for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="09e0d-116">*NetworkAvailable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09e0d-116">*networkAvailable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e0d-117">Se a rede está disponível.</span><span class="sxs-lookup"><span data-stu-id="09e0d-117">Whether the network is available.</span></span>

</dd> <dt>

<span data-ttu-id="09e0d-118">*attemptCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09e0d-118">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e0d-119">Que tente isso.</span><span class="sxs-lookup"><span data-stu-id="09e0d-119">Which attempt this is.</span></span>

</dd> <dt>

<span data-ttu-id="09e0d-120">*maxAttemptCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09e0d-120">*maxAttemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e0d-121">O número máximo de tentativas de reconexão será executado.</span><span class="sxs-lookup"><span data-stu-id="09e0d-121">The maximum number of reconnect attempts will be performed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09e0d-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09e0d-122">Return value</span></span>

<span data-ttu-id="09e0d-123">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="09e0d-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="09e0d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09e0d-124">Requirements</span></span>



| <span data-ttu-id="09e0d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="09e0d-125">Requirement</span></span> | <span data-ttu-id="09e0d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="09e0d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09e0d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09e0d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="09e0d-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="09e0d-128">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="09e0d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09e0d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="09e0d-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09e0d-130">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="09e0d-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="09e0d-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="09e0d-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09e0d-132"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="09e0d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="09e0d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09e0d-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09e0d-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="09e0d-135">IID</span><span class="sxs-lookup"><span data-stu-id="09e0d-135">IID</span></span><br/>                      | <span data-ttu-id="09e0d-136">DIID \_ IRemoteDesktopClientEvents é definido como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="09e0d-136">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09e0d-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="09e0d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09e0d-138">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="09e0d-138">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





