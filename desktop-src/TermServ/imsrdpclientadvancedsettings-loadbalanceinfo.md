---
title: Propriedade IMsRdpClientAdvancedSettings LoadBalanceInfo
description: Especifica o cookie de balanceamento de carga que será colocado no pacote de solicitação de conexão X. 224 na sequência de conexão do protocolo de servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade LoadBalanceInfo
- Propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade LoadBalanceInfo
- Propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade LoadBalanceInfo
- Propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade LoadBalanceInfo
- Propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade LoadBalanceInfo
- Propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade LoadBalanceInfo
- Propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade LoadBalanceInfo
- Propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade LoadBalanceInfo
- Propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade LoadBalanceInfo
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.LoadBalanceInfo
- IMsRdpClientAdvancedSettings.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.put_LoadBalanceInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12112eb2a18d38993e905f8d36175f1ab15f58a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369441"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a><span data-ttu-id="d746d-120">Propriedade IMsRdpClientAdvancedSettings:: LoadBalanceInfo</span><span class="sxs-lookup"><span data-stu-id="d746d-120">IMsRdpClientAdvancedSettings::LoadBalanceInfo property</span></span>

<span data-ttu-id="d746d-121">Especifica o cookie de balanceamento de carga que será colocado no pacote de solicitação de conexão X. 224 na sequência de conexão do protocolo de servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="d746d-121">Specifies the load balancing cookie that will be placed in the X.224 Connection Request packet in the Remote Desktop Session Host (RD Session Host) server protocol connection sequence.</span></span>

<span data-ttu-id="d746d-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d746d-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d746d-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="d746d-123">Syntax</span></span>


```C++
HRESULT put_LoadBalanceInfo(
  [in]  BSTR newLBInfo
);

HRESULT get_LoadBalanceInfo(
  [out] BSTR *pLBInfo
);
```



## <a name="property-value"></a><span data-ttu-id="d746d-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d746d-124">Property value</span></span>

<span data-ttu-id="d746d-125">Ponteiro para o novo cookie.</span><span class="sxs-lookup"><span data-stu-id="d746d-125">Pointer to the new cookie.</span></span> <span data-ttu-id="d746d-126">Para obter mais informações, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="d746d-126">For more information, see the remarks section.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d746d-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d746d-127">Error codes</span></span>

<span data-ttu-id="d746d-128">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d746d-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d746d-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="d746d-129">Remarks</span></span>

<span data-ttu-id="d746d-130">As informações de balanceamento de carga são usadas pelos roteadores de balanceamento de carga para escolher o melhor servidor para o cliente ao usar farms de servidores de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="d746d-130">The load balancing information is used by load balancing routers to choose the best server for the client when using farms of RD Session Host servers.</span></span> <span data-ttu-id="d746d-131">O próprio servidor Host da Sessão RD não usa essas informações e as descartará.</span><span class="sxs-lookup"><span data-stu-id="d746d-131">The RD Session Host server itself does not use this information and will discard it.</span></span>

<span data-ttu-id="d746d-132">O cookie usa o seguinte, diferencia maiúsculas de minúsculas, sintaxe:</span><span class="sxs-lookup"><span data-stu-id="d746d-132">The cookie uses the following, case-sensitive, syntax:</span></span>

<span data-ttu-id="d746d-133">**Cookie: MSTS =**_IpAddressAndPortNumber_*_\\ r \\ n_*</span><span class="sxs-lookup"><span data-stu-id="d746d-133">**Cookie: msts=**_IpAddressAndPortNumber_*_\\r\\n_*</span></span>

<span data-ttu-id="d746d-134">Em que *IpAddressAndPortNumber* é o endereço IP e o número da porta, em ordem de bytes de rede.</span><span class="sxs-lookup"><span data-stu-id="d746d-134">Where *IpAddressAndPortNumber* is the IP address and port number, in network byte order.</span></span>

<span data-ttu-id="d746d-135">Por exemplo, o cookie usado para acessar o endereço IP do 172.31.249.216, número da porta 3389, é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d746d-135">For example, the cookie used to access the IP address of 172.31.249.216, port number 3389 is as follows:</span></span>

<span data-ttu-id="d746d-136">**Cookie: MSTS = 3640205228.15629.0000 \\ r \\ n**</span><span class="sxs-lookup"><span data-stu-id="d746d-136">**Cookie: msts=3640205228.15629.0000\\r\\n**</span></span>

<span data-ttu-id="d746d-137">Os quatro últimos zeros são opcionais e são reservados.</span><span class="sxs-lookup"><span data-stu-id="d746d-137">The final four zeros are optional and are reserved.</span></span> <span data-ttu-id="d746d-138">O ponto decimal final é necessário, assim como o retorno de carro à direita e a alimentação de peso.</span><span class="sxs-lookup"><span data-stu-id="d746d-138">The final decimal point is required, as are the trailing carriage return and linefeed.</span></span> <span data-ttu-id="d746d-139">O comprimento da cadeia de caracteres, em caracteres, deve ser um múltiplo par de 2, portanto, adicione um espaço, se necessário.</span><span class="sxs-lookup"><span data-stu-id="d746d-139">The length of the string, in characters, must be an even multiple of 2, so add a space if necessary.</span></span>

<span data-ttu-id="d746d-140">Se nenhum cookie for fornecido, o padrão será **Cookie: mstshash =**_username_*_\\ r \\ n_*.</span><span class="sxs-lookup"><span data-stu-id="d746d-140">If no cookie is supplied, the default is **Cookie: mstshash=**_UserName_*_\\r\\n_*.</span></span>

<span data-ttu-id="d746d-141">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d746d-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d746d-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d746d-142">Requirements</span></span>



| <span data-ttu-id="d746d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="d746d-143">Requirement</span></span> | <span data-ttu-id="d746d-144">Valor</span><span class="sxs-lookup"><span data-stu-id="d746d-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d746d-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d746d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d746d-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d746d-146">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="d746d-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d746d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d746d-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d746d-148">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="d746d-149">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d746d-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="d746d-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d746d-150"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d746d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="d746d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d746d-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d746d-152"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d746d-153">IID</span><span class="sxs-lookup"><span data-stu-id="d746d-153">IID</span></span><br/>                      | <span data-ttu-id="d746d-154">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="d746d-154">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d746d-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="d746d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d746d-156">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d746d-156">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d746d-157">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d746d-157">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d746d-158">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d746d-158">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d746d-159">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d746d-159">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d746d-160">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d746d-160">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d746d-161">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d746d-161">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d746d-162">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d746d-162">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d746d-163">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="d746d-163">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





