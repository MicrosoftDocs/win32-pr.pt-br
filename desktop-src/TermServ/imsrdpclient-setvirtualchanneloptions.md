---
title: Método IMsRdpClient SetVirtualChannelOptions
description: Define as opções de canal virtual para o controle ActiveX Área de Trabalho Remota.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método SetVirtualChannelOptions
topic_type:
- apiref
api_name:
- IMsRdpClient.SetVirtualChannelOptions
- IMsRdpClient2.SetVirtualChannelOptions
- IMsRdpClient3.SetVirtualChannelOptions
- IMsRdpClient4.SetVirtualChannelOptions
- IMsRdpClient5.SetVirtualChannelOptions
- IMsRdpClient6.SetVirtualChannelOptions
- IMsRdpClient7.SetVirtualChannelOptions
- IMsRdpClient8.SetVirtualChannelOptions
- IMsRdpClient9.SetVirtualChannelOptions
- IMsRdpClient10.SetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e727fd3486b9d1b31fb3a421ea6ff268949790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369388"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a><span data-ttu-id="ff1ff-124">Método IMsRdpClient:: SetVirtualChannelOptions</span><span class="sxs-lookup"><span data-stu-id="ff1ff-124">IMsRdpClient::SetVirtualChannelOptions method</span></span>

<span data-ttu-id="ff1ff-125">Define as opções de canal virtual para o controle ActiveX Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ff1ff-125">Sets the virtual channel options for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="ff1ff-126">Chame esse método depois de chamar o método [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) , mas antes de estabelecer uma conexão com o método [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="ff1ff-126">Call this method after calling the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method, but before establishing a connection with the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="ff1ff-127">Esse método define opções adicionais em canais virtuais que foram criados com **CreateVirtualChannels**.</span><span class="sxs-lookup"><span data-stu-id="ff1ff-127">This method sets additional options on virtual channels that have been created with **CreateVirtualChannels**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff1ff-128">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff1ff-128">Syntax</span></span>


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a><span data-ttu-id="ff1ff-129">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff1ff-129">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff1ff-130">*Canalname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff1ff-130">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff1ff-131">O nome do canal virtual que foi especificado na chamada para o método [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="ff1ff-131">The name of the virtual channel that was specified in the call to the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="ff1ff-132">*canal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff1ff-132">*chanOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff1ff-133">As opções a serem definidas para o canal virtual especificado pelo parâmetro de *canal* .</span><span class="sxs-lookup"><span data-stu-id="ff1ff-133">The options to set for the virtual channel specified by the *ChanName* parameter.</span></span> <span data-ttu-id="ff1ff-134">Para obter uma descrição das opções possíveis, confira [**\_ definição de canal**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span><span class="sxs-lookup"><span data-stu-id="ff1ff-134">For a description of possible options, see [**CHANNEL\_DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span></span> <span data-ttu-id="ff1ff-135">Para obter mais informações, consulte a seção Comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff1ff-135">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff1ff-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff1ff-136">Return value</span></span>

<span data-ttu-id="ff1ff-137">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ff1ff-137">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff1ff-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff1ff-138">Remarks</span></span>

<span data-ttu-id="ff1ff-139">Um exemplo de como usar esse método seria declarar o canal como controle remoto persistente, definindo a **opção de canal sinalizador \_ \_ \_ \_ persistente de controle remoto** .</span><span class="sxs-lookup"><span data-stu-id="ff1ff-139">An example of using this method would be to declare the channel as remote control persistent by setting the **CHANNEL\_OPTION\_REMOTE\_CONTROL\_PERSISTENT** flag.</span></span> <span data-ttu-id="ff1ff-140">Isso significa que o canal não seria fechado quando um controle remoto se conecta ou desconecta da sessão conectada ao cliente.</span><span class="sxs-lookup"><span data-stu-id="ff1ff-140">This means that the channel would not be closed when a remote control connects to or disconnects from the session connected to the client.</span></span> <span data-ttu-id="ff1ff-141">Para obter mais informações, consulte [controle remoto de canais virtuais persistentes](remote-control-persistent-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="ff1ff-141">For more information, see [Remote Control Persistent Virtual Channels](remote-control-persistent-virtual-channels.md).</span></span>

<span data-ttu-id="ff1ff-142">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ff1ff-142">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff1ff-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff1ff-143">Requirements</span></span>



| <span data-ttu-id="ff1ff-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff1ff-144">Requirement</span></span> | <span data-ttu-id="ff1ff-145">Valor</span><span class="sxs-lookup"><span data-stu-id="ff1ff-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1ff-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff1ff-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ff1ff-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff1ff-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ff1ff-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff1ff-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ff1ff-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff1ff-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ff1ff-150">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ff1ff-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="ff1ff-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff1ff-151"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ff1ff-152">DLL</span><span class="sxs-lookup"><span data-stu-id="ff1ff-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff1ff-153"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff1ff-153"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ff1ff-154">IID</span><span class="sxs-lookup"><span data-stu-id="ff1ff-154">IID</span></span><br/>                      | <span data-ttu-id="ff1ff-155">IID \_ IMsRdpClient é definido como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="ff1ff-155">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="ff1ff-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff1ff-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff1ff-157">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="ff1ff-157">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="ff1ff-158">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="ff1ff-158">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="ff1ff-159">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="ff1ff-159">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="ff1ff-160">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="ff1ff-160">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="ff1ff-161">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="ff1ff-161">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="ff1ff-162">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="ff1ff-162">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="ff1ff-163">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="ff1ff-163">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="ff1ff-164">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ff1ff-164">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ff1ff-165">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ff1ff-165">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ff1ff-166">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="ff1ff-166">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="ff1ff-167">**DEF. de canal \_**</span><span class="sxs-lookup"><span data-stu-id="ff1ff-167">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[<span data-ttu-id="ff1ff-168">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="ff1ff-168">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="ff1ff-169">**GetVirtualChannelOptions**</span><span class="sxs-lookup"><span data-stu-id="ff1ff-169">**GetVirtualChannelOptions**</span></span>](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





