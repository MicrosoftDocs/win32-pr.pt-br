---
title: Método IMsTscAxEvents OnAutoReconnecting
description: Chamado quando um cliente está no processo de reconexão automática de uma sessão com um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). | Método IMsTscAxEvents OnAutoReconnecting
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnAutoReconnecting
- Método OnAutoReconnecting Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnAutoReconnecting
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3435be46f2bb2c7bcf8ca662b039f3e5ef856d8b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298346"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a><span data-ttu-id="911ea-107">Método IMsTscAxEvents:: OnAutoReconnecting</span><span class="sxs-lookup"><span data-stu-id="911ea-107">IMsTscAxEvents::OnAutoReconnecting method</span></span>

<span data-ttu-id="911ea-108">Chamado quando um cliente está no processo de reconexão automática de uma sessão com um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="911ea-108">Called when a client is in the process of automatically reconnecting a session with a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="911ea-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="911ea-109">Syntax</span></span>


```C++
void OnAutoReconnecting(
  [in]  LONG                       disconnectReason,
  [in]  LONG                       attemptCount,
  [out] AutoReconnectContinueState *pArcContinueStatus
);
```



## <a name="parameters"></a><span data-ttu-id="911ea-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="911ea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="911ea-111">*disconnectReason* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="911ea-111">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="911ea-112">Código que descreve o motivo para a última desconexão da sessão.</span><span class="sxs-lookup"><span data-stu-id="911ea-112">Code describing the reason for the last session disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="911ea-113">*attemptCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="911ea-113">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="911ea-114">Número de tentativas que foram feitas no processo de reconexão automática atual.</span><span class="sxs-lookup"><span data-stu-id="911ea-114">Number of attempts that have been made in the current automatic reconnection process.</span></span> <span data-ttu-id="911ea-115">Essa contagem aumenta em uma para cada tentativa feita.</span><span class="sxs-lookup"><span data-stu-id="911ea-115">This count increases by one for each attempt made.</span></span>

</dd> <dt>

<span data-ttu-id="911ea-116">*pArcContinueStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="911ea-116">*pArcContinueStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="911ea-117">Ponteiro para um código retornado que especifica o estado do processo de reconexão automática.</span><span class="sxs-lookup"><span data-stu-id="911ea-117">Pointer to a returned code specifying the state of the automatic reconnection process.</span></span> <span data-ttu-id="911ea-118">Esse código pode ser redefinido para alterar o estado do processo de reconexão automática atual.</span><span class="sxs-lookup"><span data-stu-id="911ea-118">This code can be reset to change the state of the current automatic reconnection process.</span></span>

<span data-ttu-id="911ea-119">Para obter mais informações sobre como redefinir esse código, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="911ea-119">For more information about resetting this code, refer to the Remarks section.</span></span>

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span data-ttu-id="911ea-120"><span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoReconnectContinueAutomatic \* \* \* \* (0)</span><span class="sxs-lookup"><span data-stu-id="911ea-120"><span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>\*\*\*\*autoReconnectContinueAutomatic\*\*\*\* (0)</span></span>


</dt> <dd>

<span data-ttu-id="911ea-121">O processo de reconexão está ocorrendo automaticamente.</span><span class="sxs-lookup"><span data-stu-id="911ea-121">The reconnection process is occurring automatically.</span></span> <span data-ttu-id="911ea-122">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="911ea-122">This is the default value.</span></span>

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span data-ttu-id="911ea-123"><span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoReconnectContinueStop \* \* \* \* (1)</span><span class="sxs-lookup"><span data-stu-id="911ea-123"><span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>\*\*\*\*autoReconnectContinueStop\*\*\*\* (1)</span></span>


</dt> <dd>

<span data-ttu-id="911ea-124">O processo de reconexão foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="911ea-124">The reconnection process has been stopped.</span></span>

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span data-ttu-id="911ea-125"><span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoReconnectContinueManual \* \* \* \* (2)</span><span class="sxs-lookup"><span data-stu-id="911ea-125"><span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>\*\*\*\*autoReconnectContinueManual\*\*\*\* (2)</span></span>


</dt> <dd>

<span data-ttu-id="911ea-126">O processo de reconexão está ocorrendo manualmente.</span><span class="sxs-lookup"><span data-stu-id="911ea-126">The reconnection process is occurring manually.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="911ea-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="911ea-127">Return value</span></span>

<span data-ttu-id="911ea-128">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="911ea-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="911ea-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="911ea-129">Remarks</span></span>

<span data-ttu-id="911ea-130">Implemente esse método em seu coletor de eventos para receber uma notificação de que o controle está reestabelecendo uma conexão com um servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="911ea-130">Implement this method in your event sink to receive notification that the control is reestablishing a connection with an RD Session Host server.</span></span>

<span data-ttu-id="911ea-131">Quando o estado do processo de reconexão automática é alterado definindo o valor do parâmetro *pArcContinueStatus* como **autoReconnectContinueAutomatic**, esse método funciona em um modo puramente Consultivo.</span><span class="sxs-lookup"><span data-stu-id="911ea-131">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueAutomatic**, this method functions in a purely advisory mode.</span></span> <span data-ttu-id="911ea-132">Os contêineres podem escutar esse evento em busca de notificações de que o processo de reconexão automática está prosseguindo.</span><span class="sxs-lookup"><span data-stu-id="911ea-132">Containers can listen to this event for notifications that the automatic reconnection process is proceeding.</span></span> <span data-ttu-id="911ea-133">O controle continuará a tentar restabelecer automaticamente uma conexão com base em seu próprio tempo interno e contagens de tentativas.</span><span class="sxs-lookup"><span data-stu-id="911ea-133">The control will automatically keep trying to re-establish a connection based on its own internal timing and attempt counts.</span></span> <span data-ttu-id="911ea-134">Esse método é chamado durante cada tentativa de reconexão automática a fim de notificar o contêiner.</span><span class="sxs-lookup"><span data-stu-id="911ea-134">This method is called during each automatic reconnection attempt in order to notify the container.</span></span>

<span data-ttu-id="911ea-135">Quando o estado do processo de reconexão automática for alterado definindo o valor do parâmetro *pArcContinueStatus* como **autoReconnectContinueStop**, a tentativa de reconexão automática atual será encerrada, uma notificação de desconexão será enviada ao contêiner e nenhuma outra notificação de reconexão automática será emitida.</span><span class="sxs-lookup"><span data-stu-id="911ea-135">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueStop**, the current automatic reconnection attempt will be terminated, a disconnect notification will be sent to the container, and no further automatic reconnect notifications will be issued.</span></span>

> [!Note]  
> <span data-ttu-id="911ea-136">Use a propriedade [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) para habilitar ou desabilitar a reconexão automática.</span><span class="sxs-lookup"><span data-stu-id="911ea-136">Use the [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) property to enable or disable automatic reconnection.</span></span>

 

<span data-ttu-id="911ea-137">Quando o estado do processo de reconexão automática for alterado definindo o valor do parâmetro *pArcContinueStatus* como **autoReconnectContinueManual**, o contêiner controlará manualmente o processo de reconexão automática chamando [**Connect**](imstscax-connect.md) para disparar uma tentativa de conexão ou [**Desconectar**](imstscax-disconnect.md) para cancelar o processo de reconexão automática.</span><span class="sxs-lookup"><span data-stu-id="911ea-137">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueManual**, the container will manually control the automatic reconnection process by calling [**Connect**](imstscax-connect.md) to trigger a connection attempt or [**Disconnect**](imstscax-disconnect.md) to cancel the automatic reconnection process.</span></span> <span data-ttu-id="911ea-138">Uma vez definido com esse valor, o controle irá parar de fazer tentativas de reconexão automática e se tornará a política do contêiner para fazer chamadas **Connect** para disparar tentativas de reconexão automática.</span><span class="sxs-lookup"><span data-stu-id="911ea-138">Once set to this value, the control will stop making automatic reconnection attempts and it becomes the policy of the container to make **Connect** calls to trigger automatic reconnection attempts.</span></span> <span data-ttu-id="911ea-139">Isso é feito quando o contêiner fornece o comportamento da interface do usuário personalizada para reconexão automática, como reiniciar uma conexão RAS ou VPN descartada antes do processo de reconexão automática.</span><span class="sxs-lookup"><span data-stu-id="911ea-139">This is done when the container provides customized UI behavior for automatic reconnection, such as restarting a dropped RAS or VPN connection before the automatic reconnection process.</span></span>

<span data-ttu-id="911ea-140">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="911ea-140">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="911ea-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="911ea-141">Requirements</span></span>



| <span data-ttu-id="911ea-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="911ea-142">Requirement</span></span> | <span data-ttu-id="911ea-143">Valor</span><span class="sxs-lookup"><span data-stu-id="911ea-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="911ea-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="911ea-144">Minimum supported client</span></span><br/> | <span data-ttu-id="911ea-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="911ea-145">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="911ea-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="911ea-146">Minimum supported server</span></span><br/> | <span data-ttu-id="911ea-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="911ea-147">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="911ea-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="911ea-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="911ea-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="911ea-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="911ea-150">DLL</span><span class="sxs-lookup"><span data-stu-id="911ea-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="911ea-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="911ea-151"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="911ea-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="911ea-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="911ea-153">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="911ea-153">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





