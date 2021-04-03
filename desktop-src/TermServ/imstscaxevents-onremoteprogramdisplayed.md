---
title: Método IMsTscAxEvents OnRemoteProgramDisplayed
description: Chamado quando um programa do RemoteApp é exibido.
ms.assetid: 24f5ea52-0c13-4024-9448-5c2c1896ca8b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnRemoteProgramDisplayed
- Método OnRemoteProgramDisplayed Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnRemoteProgramDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 584e54c487ec24a3c165fdd5eb8e22f243e07f23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644802"
---
# <a name="imstscaxeventsonremoteprogramdisplayed-method"></a><span data-ttu-id="6b5e4-106">Método IMsTscAxEvents:: OnRemoteProgramDisplayed</span><span class="sxs-lookup"><span data-stu-id="6b5e4-106">IMsTscAxEvents::OnRemoteProgramDisplayed method</span></span>

<span data-ttu-id="6b5e4-107">Chamado quando um programa do RemoteApp é exibido.</span><span class="sxs-lookup"><span data-stu-id="6b5e4-107">Called when a RemoteApp program is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b5e4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b5e4-108">Syntax</span></span>


```C++
VOID OnRemoteProgramDisplayed(
  [in] VARIANT_BOOL vbDisplayed,
  [in] ULONG        uDisplayInformation
);
```



## <a name="parameters"></a><span data-ttu-id="6b5e4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b5e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b5e4-110">*vbDisplayed* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b5e4-110">*vbDisplayed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b5e4-111">Indica se o programa RemoteApp é exibido ou oculto.</span><span class="sxs-lookup"><span data-stu-id="6b5e4-111">Indicates whether the RemoteApp program is displayed or hidden.</span></span>

</dd> <dt>

<span data-ttu-id="6b5e4-112">*uDisplayInformation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b5e4-112">*uDisplayInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b5e4-113">As informações de exibição.</span><span class="sxs-lookup"><span data-stu-id="6b5e4-113">The display information.</span></span>

<dt>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>

<span data-ttu-id="6b5e4-114"><span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**\_falha APPDISPLAY \_ Rail**</span><span class="sxs-lookup"><span data-stu-id="6b5e4-114"><span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**RAIL\_APPDISPLAY\_AUTORECONNECT**</span></span>


</dt> <dd>

<span data-ttu-id="6b5e4-115">A reconexão automática está em andamento.</span><span class="sxs-lookup"><span data-stu-id="6b5e4-115">Automatic reconnect is in progress.</span></span>

</dd> <dt>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>

<span data-ttu-id="6b5e4-116"><span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**\_DESKTOPHOOKED APPDISPLAY \_ Rail**</span><span class="sxs-lookup"><span data-stu-id="6b5e4-116"><span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**RAIL\_APPDISPLAY\_DESKTOPHOOKED**</span></span>


</dt> <dd>

<span data-ttu-id="6b5e4-117">A contagem de RemoteApps acabou de entrar em zero.</span><span class="sxs-lookup"><span data-stu-id="6b5e4-117">The RemoteApp count just went to zero.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b5e4-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b5e4-118">Return value</span></span>

<span data-ttu-id="6b5e4-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6b5e4-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b5e4-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b5e4-120">Remarks</span></span>

<span data-ttu-id="6b5e4-121">Implemente esse método em seu coletor de eventos para receber uma notificação de que um RemoteApp foi exibido.</span><span class="sxs-lookup"><span data-stu-id="6b5e4-121">Implement this method in your event sink to receive notification that a RemoteApp has been displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b5e4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b5e4-122">Requirements</span></span>



| <span data-ttu-id="6b5e4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b5e4-123">Requirement</span></span> | <span data-ttu-id="6b5e4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6b5e4-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b5e4-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b5e4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6b5e4-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6b5e4-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6b5e4-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b5e4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6b5e4-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b5e4-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6b5e4-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6b5e4-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="6b5e4-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b5e4-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6b5e4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6b5e4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b5e4-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b5e4-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6b5e4-133">IID</span><span class="sxs-lookup"><span data-stu-id="6b5e4-133">IID</span></span><br/>                      | <span data-ttu-id="6b5e4-134">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="6b5e4-134">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



 

 





