---
title: Método OnDisconnect IRemoteDesktopClientEvents
description: Chamado quando o controle de cliente foi desconectado de uma sessão remota.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- Método OnDisconnect Serviços de Área de Trabalho Remota
- Método OnDisconnect Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientEvents
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientEvents, método ondisconnectd
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd59b03fe9cb23309d53773289291c8a791935a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644870"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a><span data-ttu-id="2f1c6-106">Método IRemoteDesktopClientEvents:: OnDisconnect</span><span class="sxs-lookup"><span data-stu-id="2f1c6-106">IRemoteDesktopClientEvents::OnDisconnected method</span></span>

<span data-ttu-id="2f1c6-107">Chamado quando o controle de cliente foi desconectado de uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="2f1c6-107">Called when the client control has been disconnected from a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f1c6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f1c6-108">Syntax</span></span>


```C++
void OnDisconnected(
  [in] long disconnectReason,
  [in] long ExtendedDisconnectReason,
  [in] BSTR disconnectErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="2f1c6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f1c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f1c6-110">*disconnectReason* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f1c6-110">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f1c6-111">O motivo para o evento de desconexão.</span><span class="sxs-lookup"><span data-stu-id="2f1c6-111">The reason for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="2f1c6-112">*ExtendedDisconnectReason* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f1c6-112">*ExtendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f1c6-113">Informações estendidas para o evento de desconexão.</span><span class="sxs-lookup"><span data-stu-id="2f1c6-113">Extended information for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="2f1c6-114">*disconnectErrorMessage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f1c6-114">*disconnectErrorMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f1c6-115">A mensagem de erro para o evento de desconexão.</span><span class="sxs-lookup"><span data-stu-id="2f1c6-115">The error message for the disconnect event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f1c6-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f1c6-116">Return value</span></span>

<span data-ttu-id="2f1c6-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2f1c6-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f1c6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f1c6-118">Requirements</span></span>



| <span data-ttu-id="2f1c6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f1c6-119">Requirement</span></span> | <span data-ttu-id="2f1c6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2f1c6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f1c6-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f1c6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2f1c6-122">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2f1c6-122">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="2f1c6-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f1c6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2f1c6-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f1c6-124">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="2f1c6-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2f1c6-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f1c6-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f1c6-126"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="2f1c6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2f1c6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f1c6-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f1c6-128"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="2f1c6-129">IID</span><span class="sxs-lookup"><span data-stu-id="2f1c6-129">IID</span></span><br/>                      | <span data-ttu-id="2f1c6-130">DIID \_ IRemoteDesktopClientEvents é definido como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="2f1c6-130">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f1c6-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f1c6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f1c6-132">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="2f1c6-132">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





