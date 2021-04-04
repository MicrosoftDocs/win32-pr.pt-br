---
title: Método onconnected IMsTscAxEvents
description: Chamado quando o controle de cliente está no processo de estabelecer uma conexão com um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 9c26d112-c070-4870-93d5-2fcc84a1331f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método onconnected
- Método onconnected Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método onconnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d83a6a14f58a0704f0a3110532ad8cf8c0d7dc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644605"
---
# <a name="imstscaxeventsonconnected-method"></a><span data-ttu-id="b5dff-106">Método IMsTscAxEvents:: onconnected</span><span class="sxs-lookup"><span data-stu-id="b5dff-106">IMsTscAxEvents::OnConnected method</span></span>

<span data-ttu-id="b5dff-107">Chamado quando o controle de cliente está no processo de estabelecer uma conexão com um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="b5dff-107">Called when the client control is in the process of establishing a connection with a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5dff-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5dff-108">Syntax</span></span>


```C++
void OnConnected();
```



## <a name="parameters"></a><span data-ttu-id="b5dff-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5dff-109">Parameters</span></span>

<span data-ttu-id="b5dff-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b5dff-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5dff-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5dff-111">Return value</span></span>

<span data-ttu-id="b5dff-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b5dff-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5dff-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5dff-113">Remarks</span></span>

<span data-ttu-id="b5dff-114">Implemente esse método em seu coletor de eventos para receber uma notificação de que o controle estabeleceu uma conexão com um servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="b5dff-114">Implement this method in your event sink to receive notification that the control has established a connection with an RD Session Host server.</span></span>

<span data-ttu-id="b5dff-115">Consulte o evento [**IMsTscAxEvents:: OnLoginComplete**](imstscaxevents-onlogincomplete.md) para obter mais informações sobre como chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="b5dff-115">Refer to the [**IMsTscAxEvents::OnLoginComplete**](imstscaxevents-onlogincomplete.md) event for more information on calling this method.</span></span>

<span data-ttu-id="b5dff-116">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b5dff-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5dff-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5dff-117">Requirements</span></span>



| <span data-ttu-id="b5dff-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5dff-118">Requirement</span></span> | <span data-ttu-id="b5dff-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b5dff-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5dff-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5dff-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b5dff-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5dff-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b5dff-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5dff-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b5dff-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5dff-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b5dff-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b5dff-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5dff-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5dff-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b5dff-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b5dff-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5dff-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5dff-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b5dff-128">IID</span><span class="sxs-lookup"><span data-stu-id="b5dff-128">IID</span></span><br/>                      | <span data-ttu-id="b5dff-129">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="b5dff-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="b5dff-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5dff-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5dff-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="b5dff-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





