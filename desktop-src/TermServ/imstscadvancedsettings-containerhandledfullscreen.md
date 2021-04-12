---
title: Propriedade IMsTscAdvancedSettings ContainerHandledFullScreen
description: Especifica se o modo de tela inteira manipulado por contêiner está habilitado.
ms.assetid: 67679323-4a74-4d91-abd0-607415295f3d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsTscAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsTscAdvancedSettings, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, propriedade ContainerHandledFullScreen
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.ContainerHandledFullScreen
- IMsTscAdvancedSettings.get_ContainerHandledFullScreen
- IMsTscAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.put_ContainerHandledFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7442ce16e2ff30ca2d9b3bd529d37382d1df41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369731"
---
# <a name="imstscadvancedsettingscontainerhandledfullscreen-property"></a><span data-ttu-id="6b93a-122">Propriedade IMsTscAdvancedSettings:: ContainerHandledFullScreen</span><span class="sxs-lookup"><span data-stu-id="6b93a-122">IMsTscAdvancedSettings::ContainerHandledFullScreen property</span></span>

<span data-ttu-id="6b93a-123">Especifica se o modo de tela inteira manipulado por contêiner está habilitado.</span><span class="sxs-lookup"><span data-stu-id="6b93a-123">Specifies whether the container-handled full-screen mode is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="6b93a-124">O valor da propriedade **ContainerHandledFullScreen** não tem efeito quando o controle ActiveX área de trabalho remota é seguro para script e retorna **S \_ false** quando é feita uma tentativa de alterar o valor.</span><span class="sxs-lookup"><span data-stu-id="6b93a-124">The value of the **ContainerHandledFullScreen** property has no effect when the Remote Desktop ActiveX control is safe for scripting, and returns **S\_FALSE** when an attempt is made to change the value.</span></span>

 

<span data-ttu-id="6b93a-125">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6b93a-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b93a-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b93a-126">Syntax</span></span>


```C++
HRESULT put_ContainerHandledFullScreen(
  [in]  BOOL ContainerHandledFullScreen
);

HRESULT get_ContainerHandledFullScreen(
  [out] BOOL *pContainerHandledFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="6b93a-127">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6b93a-127">Property value</span></span>

<span data-ttu-id="6b93a-128">Defina esse parâmetro como **true** para habilitar o modo ou outro valor para desabilitar o modo.</span><span class="sxs-lookup"><span data-stu-id="6b93a-128">Set this parameter to **TRUE** to enable the mode or another value to disable the mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6b93a-129">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6b93a-129">Error codes</span></span>

<span data-ttu-id="6b93a-130">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6b93a-130">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="6b93a-131">Retornará **S \_ false** se não houver suporte.</span><span class="sxs-lookup"><span data-stu-id="6b93a-131">Returns **S\_FALSE** if not supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b93a-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b93a-132">Remarks</span></span>

<span data-ttu-id="6b93a-133">Quando esse modo está habilitado, o contêiner atual processa o comutador para dentro e para fora do modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="6b93a-133">When this mode is enabled, the current container processes the switch into and out of full-screen mode.</span></span> <span data-ttu-id="6b93a-134">Esse método deve ser usado somente se o contêiner atual precisar de controle extensivo sobre o comportamento do modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="6b93a-134">This method should be used only if the current container needs extensive control over full-screen mode behavior.</span></span> <span data-ttu-id="6b93a-135">Quando essa propriedade é definida, o controle não entra nem sai do modo de tela inteira em resposta à combinação de teclas de atalho do modo de tela inteira (CTRL + ALT + BREAK); em vez disso, os eventos [**IMsTscAxEvents:: OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) e [**IMsTscAxEvents:: OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) são chamados.</span><span class="sxs-lookup"><span data-stu-id="6b93a-135">When this property is set, the control does not enter or leave full-screen mode in response to the full-screen mode shortcut key combination (CTRL+ALT+BREAK); instead, the [**IMsTscAxEvents::OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) and [**IMsTscAxEvents::OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) events are called.</span></span> <span data-ttu-id="6b93a-136">Consulte [**IMsTscAxEvents**](imstscaxevents-interface.md) para obter mais informações sobre esses eventos.</span><span class="sxs-lookup"><span data-stu-id="6b93a-136">See [**IMsTscAxEvents**](imstscaxevents-interface.md) for more information about these events.</span></span>

<span data-ttu-id="6b93a-137">A maioria dos aplicativos de contêiner não precisará usar o modo de tela inteira manipulado por contêiner.</span><span class="sxs-lookup"><span data-stu-id="6b93a-137">Most container applications will not need to use container-handled full-screen mode.</span></span>

<span data-ttu-id="6b93a-138">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6b93a-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b93a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b93a-139">Requirements</span></span>



| <span data-ttu-id="6b93a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b93a-140">Requirement</span></span> | <span data-ttu-id="6b93a-141">Valor</span><span class="sxs-lookup"><span data-stu-id="6b93a-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b93a-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b93a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6b93a-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b93a-143">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="6b93a-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b93a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6b93a-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b93a-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="6b93a-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6b93a-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="6b93a-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b93a-147"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="6b93a-148">DLL</span><span class="sxs-lookup"><span data-stu-id="6b93a-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b93a-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b93a-149"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="6b93a-150">IID</span><span class="sxs-lookup"><span data-stu-id="6b93a-150">IID</span></span><br/>                      | <span data-ttu-id="6b93a-151">IID \_ IMsTscAdvancedSettings é definido como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="6b93a-151">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6b93a-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b93a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b93a-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="6b93a-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="6b93a-154">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="6b93a-154">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="6b93a-155">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="6b93a-155">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="6b93a-156">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="6b93a-156">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="6b93a-157">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="6b93a-157">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="6b93a-158">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6b93a-158">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="6b93a-159">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6b93a-159">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="6b93a-160">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6b93a-160">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="6b93a-161">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="6b93a-161">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





