---
title: Método IMsTscAx SendOnVirtualChannel
description: Envia dados para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) por meio de um canal virtual que foi criado anteriormente usando o método CreateVirtualChannels.
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método SendOnVirtualChannel
- Método SendOnVirtualChannel Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método SendOnVirtualChannel
topic_type:
- apiref
api_name:
- IMsTscAx.SendOnVirtualChannel
- IMsRdpClient.SendOnVirtualChannel
- IMsRdpClient2.SendOnVirtualChannel
- IMsRdpClient3.SendOnVirtualChannel
- IMsRdpClient4.SendOnVirtualChannel
- IMsRdpClient5.SendOnVirtualChannel
- IMsRdpClient6.SendOnVirtualChannel
- IMsRdpClient7.SendOnVirtualChannel
- IMsRdpClient8.SendOnVirtualChannel
- IMsRdpClient9.SendOnVirtualChannel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1371ae17978601a3194f755dd364d9227b8fc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454778"
---
# <a name="imstscaxsendonvirtualchannel-method"></a><span data-ttu-id="e103e-124">Método IMsTscAx:: SendOnVirtualChannel</span><span class="sxs-lookup"><span data-stu-id="e103e-124">IMsTscAx::SendOnVirtualChannel method</span></span>

<span data-ttu-id="e103e-125">Envia dados para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) por meio de um canal virtual que foi criado anteriormente usando o método [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="e103e-125">Sends data to the Remote Desktop Session Host (RD Session Host) server over a virtual channel that was created previously by using the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e103e-126">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e103e-126">Syntax</span></span>


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a><span data-ttu-id="e103e-127">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e103e-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e103e-128">*Canalname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e103e-128">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e103e-129">O nome do canal virtual que foi especificado na chamada para [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span><span class="sxs-lookup"><span data-stu-id="e103e-129">The virtual channel name that was specified in the call to [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span></span>

</dd> <dt>

<span data-ttu-id="e103e-130">*ChanData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e103e-130">*ChanData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e103e-131">Os dados a serem enviados pelo canal virtual, na forma **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="e103e-131">The data to send over the virtual channel, in **BSTR** form.</span></span> <span data-ttu-id="e103e-132">Não há nenhuma restrição de que esses dados devem ser cadeias de caracteres terminadas em nulo.</span><span class="sxs-lookup"><span data-stu-id="e103e-132">There is no restriction that this data must be null-terminated strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e103e-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e103e-133">Return value</span></span>

<span data-ttu-id="e103e-134">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e103e-134">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e103e-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="e103e-135">Remarks</span></span>

<span data-ttu-id="e103e-136">Consulte [registro de cliente de canal virtual](virtual-channel-client-registration.md) para obter informações sobre restrições de nomenclatura de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="e103e-136">Refer to [Virtual Channel Client Registration](virtual-channel-client-registration.md) for information about virtual channel naming restrictions.</span></span>

<span data-ttu-id="e103e-137">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e103e-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e103e-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e103e-138">Requirements</span></span>



| <span data-ttu-id="e103e-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e103e-139">Requirement</span></span> | <span data-ttu-id="e103e-140">Valor</span><span class="sxs-lookup"><span data-stu-id="e103e-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e103e-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e103e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e103e-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e103e-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e103e-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e103e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e103e-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e103e-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e103e-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e103e-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="e103e-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e103e-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e103e-147">DLL</span><span class="sxs-lookup"><span data-stu-id="e103e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e103e-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e103e-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e103e-149">IID</span><span class="sxs-lookup"><span data-stu-id="e103e-149">IID</span></span><br/>                      | <span data-ttu-id="e103e-150">IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="e103e-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e103e-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="e103e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e103e-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="e103e-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="e103e-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="e103e-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="e103e-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="e103e-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="e103e-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e103e-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e103e-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e103e-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e103e-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e103e-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e103e-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e103e-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e103e-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e103e-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e103e-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e103e-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e103e-161">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="e103e-161">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="e103e-162">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="e103e-162">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





