---
title: Interface IRemoteDesktopClientEvents
description: Fornece métodos que recebem informações do servidor que estão relacionados a eventos de controle de cliente.
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientEvents
- Serviços de Área de Trabalho Remota da interface IRemoteDesktopClientEvents, descrita
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7533ee7fea7c522b6129bda06891630c3e5ad15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009371"
---
# <a name="iremotedesktopclientevents-interface"></a><span data-ttu-id="3a88c-105">Interface IRemoteDesktopClientEvents</span><span class="sxs-lookup"><span data-stu-id="3a88c-105">IRemoteDesktopClientEvents interface</span></span>

<span data-ttu-id="3a88c-106">Fornece métodos que recebem informações do servidor que estão relacionados a eventos de controle de cliente.</span><span class="sxs-lookup"><span data-stu-id="3a88c-106">Provides methods that receive information from the server that are related to client control events.</span></span> <span data-ttu-id="3a88c-107">Os eventos incluem conexão e desconexão, solicitações de modo de tela inteira, logon bem-sucedido e condições de erro.</span><span class="sxs-lookup"><span data-stu-id="3a88c-107">Events include connecting and disconnecting, full-screen mode requests, successful logon, and error conditions.</span></span>

## <a name="members"></a><span data-ttu-id="3a88c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3a88c-108">Members</span></span>

<span data-ttu-id="3a88c-109">A interface **IRemoteDesktopClientEvents** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3a88c-109">The **IRemoteDesktopClientEvents** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3a88c-110">**IRemoteDesktopClientEvents** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3a88c-110">**IRemoteDesktopClientEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="3a88c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3a88c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3a88c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3a88c-112">Methods</span></span>

<span data-ttu-id="3a88c-113">A interface **IRemoteDesktopClientEvents** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3a88c-113">The **IRemoteDesktopClientEvents** interface has these methods.</span></span>



| <span data-ttu-id="3a88c-114">Método</span><span class="sxs-lookup"><span data-stu-id="3a88c-114">Method</span></span>                                                                                      | <span data-ttu-id="3a88c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a88c-115">Description</span></span>                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a88c-116">**OnAdminMessageReceived**</span><span class="sxs-lookup"><span data-stu-id="3a88c-116">**OnAdminMessageReceived**</span></span>](iremotedesktopclientevents-onadminmessagereceived.md)         | <span data-ttu-id="3a88c-117">Chamado quando o controle de cliente recebe uma mensagem administrativa.</span><span class="sxs-lookup"><span data-stu-id="3a88c-117">Called when the client control receives an administrative message.</span></span> <br/>                                                                                      |
| [<span data-ttu-id="3a88c-118">**OnAutoReconnected**</span><span class="sxs-lookup"><span data-stu-id="3a88c-118">**OnAutoReconnected**</span></span>](iremotedesktopclientevents-onautoreconnected.md)                   | <span data-ttu-id="3a88c-119">Chamado quando o controle de cliente é reconectado automaticamente a uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="3a88c-119">Called when the client control has automatically reconnected to a remote session.</span></span> <br/>                                                                       |
| [<span data-ttu-id="3a88c-120">**OnAutoReconnecting**</span><span class="sxs-lookup"><span data-stu-id="3a88c-120">**OnAutoReconnecting**</span></span>](iremotedesktopclientevents-onautoreconnecting.md)                 | <span data-ttu-id="3a88c-121">Chamado quando o controle de cliente tenta restabelecer automaticamente uma conexão com uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="3a88c-121">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span> <br/>                                                  |
| [<span data-ttu-id="3a88c-122">**Onconnected**</span><span class="sxs-lookup"><span data-stu-id="3a88c-122">**OnConnected**</span></span>](iremotedesktopclientevents-onconnected.md)                               | <span data-ttu-id="3a88c-123">Chamado quando o controle de cliente se conectou a uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="3a88c-123">Called when the client control has connected to a remote session.</span></span><br/>                                                                                        |
| [<span data-ttu-id="3a88c-124">**Desconectando**</span><span class="sxs-lookup"><span data-stu-id="3a88c-124">**OnConnecting**</span></span>](iremotedesktopclientevents-onconnecting.md)                             | <span data-ttu-id="3a88c-125">Chamado quando o controle de cliente tenta estabelecer uma conexão com uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="3a88c-125">Called when the client control attempts to establish a connection to a remote session.</span></span> <br/>                                                                  |
| [<span data-ttu-id="3a88c-126">**OnDialogDismissed**</span><span class="sxs-lookup"><span data-stu-id="3a88c-126">**OnDialogDismissed**</span></span>](iremotedesktopclientevents-ondialogdismissed.md)                   | <span data-ttu-id="3a88c-127">Chamado depois que uma caixa de diálogo exibida pelo controle de cliente é ignorada.</span><span class="sxs-lookup"><span data-stu-id="3a88c-127">Called after a dialog box displayed by the client control is dismissed.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="3a88c-128">**OnDialogDisplaying**</span><span class="sxs-lookup"><span data-stu-id="3a88c-128">**OnDialogDisplaying**</span></span>](iremotedesktopclientevents-ondialogdisplaying.md)                 | <span data-ttu-id="3a88c-129">Chamado antes de o controle exibir uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3a88c-129">Called before the control displays a dialog box.</span></span> <br/>                                                                                                        |
| [<span data-ttu-id="3a88c-130">**Desconectado**</span><span class="sxs-lookup"><span data-stu-id="3a88c-130">**OnDisconnected**</span></span>](iremotedesktopclientevents-ondisconnected.md)                         | <span data-ttu-id="3a88c-131">Chamado quando o controle de cliente foi desconectado de uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="3a88c-131">Called when the client control has been disconnected from a remote session.</span></span> <br/>                                                                             |
| [<span data-ttu-id="3a88c-132">**OnKeyCombinationPressed**</span><span class="sxs-lookup"><span data-stu-id="3a88c-132">**OnKeyCombinationPressed**</span></span>](iremotedesktopclientevents-onkeycombinationpressed.md)       | <span data-ttu-id="3a88c-133">Chamado quando as combinações de teclas especiais são pressionadas na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="3a88c-133">Called when special key combinations are pressed in the remote session.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="3a88c-134">**OnLoginCompleted**</span><span class="sxs-lookup"><span data-stu-id="3a88c-134">**OnLoginCompleted**</span></span>](iremotedesktopclientevents-onlogincompleted.md)                     | <span data-ttu-id="3a88c-135">Chamado quando o controle de cliente faz logon com êxito em uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="3a88c-135">Called when the client control has successfully logged on to a remote session.</span></span> <br/>                                                                          |
| [<span data-ttu-id="3a88c-136">**OnNetworkStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="3a88c-136">**OnNetworkStatusChanged**</span></span>](iremotedesktopclientevents-onnetworkstatuschanged.md)         | <span data-ttu-id="3a88c-137">Chamado quando o status da rede é alterado.</span><span class="sxs-lookup"><span data-stu-id="3a88c-137">Called when the network status has changed.</span></span> <br/>                                                                                                             |
| [<span data-ttu-id="3a88c-138">**OnRemoteDesktopSizeChanged**</span><span class="sxs-lookup"><span data-stu-id="3a88c-138">**OnRemoteDesktopSizeChanged**</span></span>](iremotedesktopclientevents-onremotedesktopsizechanged.md) | <span data-ttu-id="3a88c-139">Chamado quando o tamanho da área de trabalho remota é alterado.</span><span class="sxs-lookup"><span data-stu-id="3a88c-139">Called when the remote desktop size has changed.</span></span> <br/>                                                                                                        |
| [<span data-ttu-id="3a88c-140">**Onstatuschanged**</span><span class="sxs-lookup"><span data-stu-id="3a88c-140">**OnStatusChanged**</span></span>](iremotedesktopclientevents-onstatuschanged.md)                       | <span data-ttu-id="3a88c-141">Chamado quando o controle de cliente atualizou seu status.</span><span class="sxs-lookup"><span data-stu-id="3a88c-141">Called when the client control has updated its status.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="3a88c-142">**OnTouchPointerCursorMoved**</span><span class="sxs-lookup"><span data-stu-id="3a88c-142">**OnTouchPointerCursorMoved**</span></span>](iremotedesktopclientevents-ontouchpointercursormoved.md)   | <span data-ttu-id="3a88c-143">Chamado quando o cursor do ponteiro de toque foi movido e a propriedade [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) está definida como true.</span><span class="sxs-lookup"><span data-stu-id="3a88c-143">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="3a88c-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a88c-144">Requirements</span></span>



| <span data-ttu-id="3a88c-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a88c-145">Requirement</span></span> | <span data-ttu-id="3a88c-146">Valor</span><span class="sxs-lookup"><span data-stu-id="3a88c-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a88c-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a88c-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3a88c-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3a88c-148">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="3a88c-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a88c-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3a88c-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3a88c-150">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="3a88c-151">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3a88c-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="3a88c-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a88c-152"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="3a88c-153">DLL</span><span class="sxs-lookup"><span data-stu-id="3a88c-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a88c-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a88c-154"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="3a88c-155">CLSID</span><span class="sxs-lookup"><span data-stu-id="3a88c-155">CLSID</span></span><br/>                    | <span data-ttu-id="3a88c-156">CLSID \_ RemoteDesktopClient é definido como EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span><span class="sxs-lookup"><span data-stu-id="3a88c-156">CLSID\_RemoteDesktopClient is defined as EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span></span><br/>       |
| <span data-ttu-id="3a88c-157">IID</span><span class="sxs-lookup"><span data-stu-id="3a88c-157">IID</span></span><br/>                      | <span data-ttu-id="3a88c-158">DIID \_ IRemoteDesktopClientEvents é definido como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="3a88c-158">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a88c-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a88c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a88c-160">Área de Trabalho Remota referência de controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="3a88c-160">Remote Desktop ActiveX control reference</span></span>](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

