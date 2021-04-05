---
title: Método IMsRdpClient RequestClose
description: Solicita um desligamento normal do Área de Trabalho Remota controle ActiveX.
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RequestClose
- Método RequestClose Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, método RequestClose
- Método RequestClose Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, método RequestClose
- Método RequestClose Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, método RequestClose
- Método RequestClose Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, método RequestClose
- Método RequestClose Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, método RequestClose
- Método RequestClose Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, método RequestClose
- Método RequestClose Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, método RequestClose
- Método RequestClose Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método RequestClose
- Método RequestClose Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método RequestClose
- Método RequestClose Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método RequestClose
topic_type:
- apiref
api_name:
- IMsRdpClient.RequestClose
- IMsRdpClient2.RequestClose
- IMsRdpClient3.RequestClose
- IMsRdpClient4.RequestClose
- IMsRdpClient5.RequestClose
- IMsRdpClient6.RequestClose
- IMsRdpClient7.RequestClose
- IMsRdpClient8.RequestClose
- IMsRdpClient9.RequestClose
- IMsRdpClient10.RequestClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1679b08680b962cdbff57e9bbbd1c392607d8709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644418"
---
# <a name="imsrdpclientrequestclose-method"></a><span data-ttu-id="aa2f5-124">Método IMsRdpClient:: RequestClose</span><span class="sxs-lookup"><span data-stu-id="aa2f5-124">IMsRdpClient::RequestClose method</span></span>

<span data-ttu-id="aa2f5-125">Solicita um desligamento normal do Área de Trabalho Remota controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="aa2f5-125">Requests a graceful shutdown of the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="aa2f5-126">Um desligamento normal pode incluir a finalização da sessão de Serviços de Área de Trabalho Remota do usuário, mas ele não desliga o servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="aa2f5-126">A graceful shutdown can include ending the user's Remote Desktop Services session but it does not shut down the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa2f5-127">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa2f5-127">Syntax</span></span>


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a><span data-ttu-id="aa2f5-128">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa2f5-128">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa2f5-129">*pCloseStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="aa2f5-129">*pCloseStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa2f5-130">Valor da enumeração [**ControlCloseStatus**](controlclosestatus.md) que indica se o aplicativo pode fechar o controle imediatamente.</span><span class="sxs-lookup"><span data-stu-id="aa2f5-130">Value from the [**ControlCloseStatus**](controlclosestatus.md) enumeration that indicates whether the application can close the control immediately.</span></span> <span data-ttu-id="aa2f5-131">A seguir está uma lista de possíveis valores.</span><span class="sxs-lookup"><span data-stu-id="aa2f5-131">Following is a list of possible values.</span></span>

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span data-ttu-id="aa2f5-132"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)</span><span class="sxs-lookup"><span data-stu-id="aa2f5-132"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)</span></span>


</dt> <dd>

<span data-ttu-id="aa2f5-133">O aplicativo de contêiner pode continuar a fechar o controle imediatamente.</span><span class="sxs-lookup"><span data-stu-id="aa2f5-133">The container application can proceed to close the control immediately.</span></span> <span data-ttu-id="aa2f5-134">Esse valor também pode indicar que a conexão já foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="aa2f5-134">This value can also indicate that the connection has already terminated.</span></span>

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span data-ttu-id="aa2f5-135"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="aa2f5-135"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="aa2f5-136">O aplicativo de contêiner não deve fechar o controle imediatamente; o aplicativo deve aguardar um dos eventos descritos na seção comentários a seguir para ocorrer antes de fechar.</span><span class="sxs-lookup"><span data-stu-id="aa2f5-136">The container application should not close the control immediately; the application should wait for one of the events described in the following Remarks section to occur before closing.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa2f5-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa2f5-137">Return value</span></span>

<span data-ttu-id="aa2f5-138">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="aa2f5-138">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa2f5-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa2f5-139">Remarks</span></span>

<span data-ttu-id="aa2f5-140">Se o parâmetro *pCloseStatus* for igual a **controlCloseWaitForEvents**, o aplicativo deverá esperar que um dos seguintes eventos ocorra antes que o aplicativo feche o controle:</span><span class="sxs-lookup"><span data-stu-id="aa2f5-140">If the *pCloseStatus* parameter is equal to **controlCloseWaitForEvents**, the application should wait for one of the following events to occur before the application closes the control:</span></span>

-   <span data-ttu-id="aa2f5-141">[**IMsTscAxEvents:: OnDisconnect**](imstscaxevents-ondisconnected.md).</span><span class="sxs-lookup"><span data-stu-id="aa2f5-141">[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md).</span></span> <span data-ttu-id="aa2f5-142">Se o usuário não estiver conectado à sessão de Serviços de Área de Trabalho Remota, o aplicativo poderá chamar a função [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir todas as janelas e, em seguida, fechar o controle.</span><span class="sxs-lookup"><span data-stu-id="aa2f5-142">If the user is not logged on to the Remote Desktop Services session, the application can call the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function to destroy all windows and then close the control.</span></span>
-   <span data-ttu-id="aa2f5-143">[**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="aa2f5-143">[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span> <span data-ttu-id="aa2f5-144">Se o usuário estiver conectado à sessão de Serviços de Área de Trabalho Remota, o controle acionará um evento **OnConfirmClose** .</span><span class="sxs-lookup"><span data-stu-id="aa2f5-144">If the user is logged on to the Remote Desktop Services session, the control fires an **OnConfirmClose** event.</span></span> <span data-ttu-id="aa2f5-145">Esse evento permite que o aplicativo solicite ao usuário se deseja fechar a conexão.</span><span class="sxs-lookup"><span data-stu-id="aa2f5-145">This event allows the application to prompt the user about whether to close the connection.</span></span> <span data-ttu-id="aa2f5-146">Se o usuário responder sim para o prompt, o aplicativo de contêiner poderá chamar [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir todas as janelas e fechar o controle.</span><span class="sxs-lookup"><span data-stu-id="aa2f5-146">If the user replies yes to the prompt, the container application can call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) to destroy all windows, and close the control.</span></span>

<span data-ttu-id="aa2f5-147">O **RequestClose** permite que um aplicativo de contêiner solicite ao usuário se uma conexão deve ser fechada.</span><span class="sxs-lookup"><span data-stu-id="aa2f5-147">**RequestClose** allows a container application to prompt the user about whether to close a connection.</span></span> <span data-ttu-id="aa2f5-148">Para obter mais informações, consulte [**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="aa2f5-148">For more information, see [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span>

<span data-ttu-id="aa2f5-149">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="aa2f5-149">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa2f5-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa2f5-150">Requirements</span></span>



| <span data-ttu-id="aa2f5-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa2f5-151">Requirement</span></span> | <span data-ttu-id="aa2f5-152">Valor</span><span class="sxs-lookup"><span data-stu-id="aa2f5-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa2f5-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa2f5-153">Minimum supported client</span></span><br/> | <span data-ttu-id="aa2f5-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa2f5-154">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="aa2f5-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa2f5-155">Minimum supported server</span></span><br/> | <span data-ttu-id="aa2f5-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa2f5-156">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aa2f5-157">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="aa2f5-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa2f5-158"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa2f5-158"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa2f5-159">DLL</span><span class="sxs-lookup"><span data-stu-id="aa2f5-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa2f5-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa2f5-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa2f5-161">IID</span><span class="sxs-lookup"><span data-stu-id="aa2f5-161">IID</span></span><br/>                      | <span data-ttu-id="aa2f5-162">IID \_ IMsRdpClient é definido como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="aa2f5-162">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="aa2f5-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa2f5-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa2f5-164">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="aa2f5-164">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="aa2f5-165">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="aa2f5-165">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="aa2f5-166">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="aa2f5-166">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="aa2f5-167">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="aa2f5-167">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="aa2f5-168">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="aa2f5-168">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="aa2f5-169">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="aa2f5-169">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="aa2f5-170">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="aa2f5-170">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="aa2f5-171">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="aa2f5-171">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="aa2f5-172">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="aa2f5-172">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="aa2f5-173">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="aa2f5-173">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="aa2f5-174">**IMsTscAxEvents::OnConfirmClose**</span><span class="sxs-lookup"><span data-stu-id="aa2f5-174">**IMsTscAxEvents::OnConfirmClose**</span></span>](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[<span data-ttu-id="aa2f5-175">**IMsTscAxEvents:: ondisconnectd**</span><span class="sxs-lookup"><span data-stu-id="aa2f5-175">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

