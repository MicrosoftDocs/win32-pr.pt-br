---
title: Método IMsRdpClientNonScriptable NotifyRedirectDeviceChange
description: Notifica o módulo de redirecionamento de dispositivo do Área de Trabalho Remota controle ActiveX que ocorreu uma alteração de dispositivo no sistema. Esse método passa \_ notificações do WM DEVICECHANGE para o controle.
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable2, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, método NotifyRedirectDeviceChange
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable2.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable3.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable4.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable5.NotifyRedirectDeviceChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7357fcb5e31eeeb0de5791425b8d9fada4365ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919112"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a><span data-ttu-id="ed03b-115">Método IMsRdpClientNonScriptable:: NotifyRedirectDeviceChange</span><span class="sxs-lookup"><span data-stu-id="ed03b-115">IMsRdpClientNonScriptable::NotifyRedirectDeviceChange method</span></span>

<span data-ttu-id="ed03b-116">Notifica o módulo de redirecionamento de dispositivo do Área de Trabalho Remota controle ActiveX que ocorreu uma alteração de dispositivo no sistema.</span><span class="sxs-lookup"><span data-stu-id="ed03b-116">Notifies the device redirection module of the Remote Desktop ActiveX control that a device change has occurred on the system.</span></span> <span data-ttu-id="ed03b-117">Esse método passa notificações do [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) para o controle.</span><span class="sxs-lookup"><span data-stu-id="ed03b-117">This method passes [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) notifications to the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed03b-118">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed03b-118">Syntax</span></span>


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="ed03b-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed03b-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed03b-120">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ed03b-120">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed03b-121">Especifica o evento do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed03b-121">Specifies the device event.</span></span> <span data-ttu-id="ed03b-122">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed03b-122">This parameter can be one of the following values.</span></span>

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span data-ttu-id="ed03b-123"><span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT \_ CONFIGCHANGECANCELED**</span><span class="sxs-lookup"><span data-stu-id="ed03b-123"><span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT\_CONFIGCHANGECANCELED**</span></span>


</dt> <dd>

<span data-ttu-id="ed03b-124">Uma solicitação para alterar a configuração atual (Dock ou Dock) foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="ed03b-124">A request to change the current configuration (dock or undock) has been canceled.</span></span>

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span data-ttu-id="ed03b-125"><span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT \_ ConfigChanged**</span><span class="sxs-lookup"><span data-stu-id="ed03b-125"><span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT\_CONFIGCHANGED**</span></span>


</dt> <dd>

<span data-ttu-id="ed03b-126">A configuração atual foi alterada devido a um encaixe ou desencaixe.</span><span class="sxs-lookup"><span data-stu-id="ed03b-126">The current configuration has changed due to a dock or undock.</span></span>

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span data-ttu-id="ed03b-127"><span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT \_ CUSTOMEVENT**</span><span class="sxs-lookup"><span data-stu-id="ed03b-127"><span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT\_CUSTOMEVENT**</span></span>


</dt> <dd>

<span data-ttu-id="ed03b-128">Ocorreu um evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="ed03b-128">A custom event has occurred.</span></span>

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span data-ttu-id="ed03b-129"><span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT \_ DEVICEARRIVAL**</span><span class="sxs-lookup"><span data-stu-id="ed03b-129"><span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT\_DEVICEARRIVAL**</span></span>


</dt> <dd>

<span data-ttu-id="ed03b-130">Um dispositivo foi inserido e agora está disponível.</span><span class="sxs-lookup"><span data-stu-id="ed03b-130">A device has been inserted and is now available.</span></span>

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span data-ttu-id="ed03b-131"><span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT \_ DEVICEQUERYREMOVE**</span><span class="sxs-lookup"><span data-stu-id="ed03b-131"><span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT\_DEVICEQUERYREMOVE**</span></span>


</dt> <dd>

<span data-ttu-id="ed03b-132">A permissão é solicitada para remover um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed03b-132">Permission is requested to remove a device.</span></span> <span data-ttu-id="ed03b-133">Qualquer aplicativo pode negar essa solicitação e cancelar a remoção.</span><span class="sxs-lookup"><span data-stu-id="ed03b-133">Any application can deny this request and cancel the removal.</span></span>

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span data-ttu-id="ed03b-134"><span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT \_ DEVICEQUERYREMOVEFAILED**</span><span class="sxs-lookup"><span data-stu-id="ed03b-134"><span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT\_DEVICEQUERYREMOVEFAILED**</span></span>


</dt> <dd>

<span data-ttu-id="ed03b-135">Uma solicitação para remover um dispositivo foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="ed03b-135">A request to remove a device has been canceled.</span></span>

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span data-ttu-id="ed03b-136"><span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT \_ DEVICEREMOVECOMPLETE**</span><span class="sxs-lookup"><span data-stu-id="ed03b-136"><span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT\_DEVICEREMOVECOMPLETE**</span></span>


</dt> <dd>

<span data-ttu-id="ed03b-137">Um dispositivo foi removido.</span><span class="sxs-lookup"><span data-stu-id="ed03b-137">A device has been removed.</span></span>

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span data-ttu-id="ed03b-138"><span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT \_ DEVICEREMOVEPENDING**</span><span class="sxs-lookup"><span data-stu-id="ed03b-138"><span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT\_DEVICEREMOVEPENDING**</span></span>


</dt> <dd>

<span data-ttu-id="ed03b-139">Um dispositivo está prestes a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ed03b-139">A device is about to be removed.</span></span> <span data-ttu-id="ed03b-140">A remoção não pode ser negada.</span><span class="sxs-lookup"><span data-stu-id="ed03b-140">The removal cannot be denied.</span></span>

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span data-ttu-id="ed03b-141"><span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT \_ DEVICETYPESPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="ed03b-141"><span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT\_DEVICETYPESPECIFIC**</span></span>


</dt> <dd>

<span data-ttu-id="ed03b-142">Ocorreu um evento específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed03b-142">A device-specific event has occurred.</span></span>

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span data-ttu-id="ed03b-143"><span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT \_ DEVNODES \_ alterado**</span><span class="sxs-lookup"><span data-stu-id="ed03b-143"><span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT\_DEVNODES\_CHANGED**</span></span>


</dt> <dd>

<span data-ttu-id="ed03b-144">Um dispositivo foi adicionado ou removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="ed03b-144">A device has been added to or removed from the system.</span></span>

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span data-ttu-id="ed03b-145"><span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT \_ QUERYCHANGECONFIG**</span><span class="sxs-lookup"><span data-stu-id="ed03b-145"><span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT\_QUERYCHANGECONFIG**</span></span>


</dt> <dd>

<span data-ttu-id="ed03b-146">A permissão é solicitada para alterar a configuração atual (Dock ou desencaixar).</span><span class="sxs-lookup"><span data-stu-id="ed03b-146">Permission is requested to change the current configuration (dock or undock).</span></span>

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span data-ttu-id="ed03b-147"><span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT \_ USERdefined**</span><span class="sxs-lookup"><span data-stu-id="ed03b-147"><span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT\_USERDEFINED**</span></span>


</dt> <dd>

<span data-ttu-id="ed03b-148">O significado dessa mensagem é definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="ed03b-148">The meaning of this message is user-defined.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ed03b-149">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ed03b-149">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed03b-150">Ponteiro para uma estrutura que contém dados específicos do evento.</span><span class="sxs-lookup"><span data-stu-id="ed03b-150">Pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="ed03b-151">Seu formato depende do valor do parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="ed03b-151">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="ed03b-152">Para obter mais informações, consulte a documentação de cada evento.</span><span class="sxs-lookup"><span data-stu-id="ed03b-152">For more information, refer to the documentation for each event.</span></span> <span data-ttu-id="ed03b-153">Para obter mais informações, consulte [tipos de eventos de dispositivo](/windows/desktop/DevIO/device-event-types).</span><span class="sxs-lookup"><span data-stu-id="ed03b-153">For more information, see [Device Event Types](/windows/desktop/DevIO/device-event-types).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed03b-154">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed03b-154">Return value</span></span>

<span data-ttu-id="ed03b-155">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ed03b-155">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed03b-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed03b-156">Remarks</span></span>

<span data-ttu-id="ed03b-157">Um aplicativo de contêiner que permite a adição dinâmica ou remoção de dispositivos deve processar a mensagem do [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) em sua janela de nível superior e encaminhar a mensagem para o controle usando o método **NotifyRedirectDeviceChange** .</span><span class="sxs-lookup"><span data-stu-id="ed03b-157">A container application that allows dynamic addition or removal of devices should process the [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) message in its top level window and forward the message to the control using the **NotifyRedirectDeviceChange** method.</span></span> <span data-ttu-id="ed03b-158">Um exemplo de uma alteração dinâmica do dispositivo é quando uma unidade de disco redirecionada é adicionada ou removida enquanto o sistema está em execução.</span><span class="sxs-lookup"><span data-stu-id="ed03b-158">An example of a dynamic device change is when a redirected disk drive is added or removed while the system is running.</span></span>

<span data-ttu-id="ed03b-159">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ed03b-159">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed03b-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed03b-160">Requirements</span></span>



| <span data-ttu-id="ed03b-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed03b-161">Requirement</span></span> | <span data-ttu-id="ed03b-162">Valor</span><span class="sxs-lookup"><span data-stu-id="ed03b-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed03b-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed03b-163">Minimum supported client</span></span><br/> | <span data-ttu-id="ed03b-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed03b-164">Windows Vista</span></span><br/>                                                                     |
| <span data-ttu-id="ed03b-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed03b-165">Minimum supported server</span></span><br/> | <span data-ttu-id="ed03b-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed03b-166">Windows Server 2008</span></span><br/>                                                               |
| <span data-ttu-id="ed03b-167">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ed03b-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="ed03b-168"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed03b-168"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="ed03b-169">DLL</span><span class="sxs-lookup"><span data-stu-id="ed03b-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed03b-170"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed03b-170"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="ed03b-171">IID</span><span class="sxs-lookup"><span data-stu-id="ed03b-171">IID</span></span><br/>                      | <span data-ttu-id="ed03b-172">IID \_ IMsRdpClientNonScriptable é definido como 2f079c4c-87b2-4AFD-97ab-20cdb43038ae</span><span class="sxs-lookup"><span data-stu-id="ed03b-172">IID\_IMsRdpClientNonScriptable is defined as 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed03b-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed03b-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed03b-174">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="ed03b-174">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="ed03b-175">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="ed03b-175">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="ed03b-176">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="ed03b-176">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="ed03b-177">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="ed03b-177">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="ed03b-178">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="ed03b-178">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 

