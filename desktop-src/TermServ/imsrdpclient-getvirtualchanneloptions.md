---
title: Método IMsRdpClient GetVirtualChannelOptions
description: Recupera as opções definidas para um canal virtual.
ms.assetid: d2ec9fb2-c0dc-49f1-a86b-d7abca13a322
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método GetVirtualChannelOptions
topic_type:
- apiref
api_name:
- IMsRdpClient.GetVirtualChannelOptions
- IMsRdpClient2.GetVirtualChannelOptions
- IMsRdpClient3.GetVirtualChannelOptions
- IMsRdpClient4.GetVirtualChannelOptions
- IMsRdpClient5.GetVirtualChannelOptions
- IMsRdpClient6.GetVirtualChannelOptions
- IMsRdpClient7.GetVirtualChannelOptions
- IMsRdpClient8.GetVirtualChannelOptions
- IMsRdpClient9.GetVirtualChannelOptions
- IMsRdpClient10.GetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71548002ebc67dae8dc1a49e8144da3de608afb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780576"
---
# <a name="imsrdpclientgetvirtualchanneloptions-method"></a><span data-ttu-id="9e822-124">Método IMsRdpClient:: GetVirtualChannelOptions</span><span class="sxs-lookup"><span data-stu-id="9e822-124">IMsRdpClient::GetVirtualChannelOptions method</span></span>

<span data-ttu-id="9e822-125">Recupera as opções definidas para um canal virtual.</span><span class="sxs-lookup"><span data-stu-id="9e822-125">Retrieves the options set for a virtual channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e822-126">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e822-126">Syntax</span></span>


```C++
HRESULT GetVirtualChannelOptions(
  [in]  BSTR ChanName,
  [out] LONG *pChanOptions
);
```



## <a name="parameters"></a><span data-ttu-id="9e822-127">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e822-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e822-128">*Canalname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e822-128">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e822-129">O nome de um canal virtual que foi especificado na chamada para o método [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="9e822-129">The name of a virtual channel that was specified in the call to [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="9e822-130">*pChanOptions* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9e822-130">*pChanOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e822-131">As opções definidas para o canal virtual especificado pelo parâmetro *canalname* .</span><span class="sxs-lookup"><span data-stu-id="9e822-131">The options set for the virtual channel specified by the *ChanName* parameter.</span></span> <span data-ttu-id="9e822-132">Para obter uma descrição das opções possíveis, confira [**\_ definição de canal**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span><span class="sxs-lookup"><span data-stu-id="9e822-132">For a description of possible options, see [**CHANNEL\_DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e822-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e822-133">Return value</span></span>

<span data-ttu-id="9e822-134">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9e822-134">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e822-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e822-135">Remarks</span></span>

<span data-ttu-id="9e822-136">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9e822-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e822-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e822-137">Requirements</span></span>



| <span data-ttu-id="9e822-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e822-138">Requirement</span></span> | <span data-ttu-id="9e822-139">Valor</span><span class="sxs-lookup"><span data-stu-id="9e822-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e822-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e822-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9e822-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e822-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9e822-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e822-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9e822-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e822-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9e822-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9e822-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="9e822-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e822-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e822-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9e822-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e822-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e822-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e822-148">IID</span><span class="sxs-lookup"><span data-stu-id="9e822-148">IID</span></span><br/>                      | <span data-ttu-id="9e822-149">IID \_ IMsRdpClient é definido como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="9e822-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="9e822-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e822-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e822-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="9e822-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="9e822-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="9e822-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="9e822-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="9e822-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="9e822-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="9e822-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="9e822-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="9e822-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="9e822-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="9e822-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="9e822-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="9e822-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="9e822-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="9e822-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="9e822-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="9e822-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="9e822-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="9e822-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="9e822-161">**DEF. de canal \_**</span><span class="sxs-lookup"><span data-stu-id="9e822-161">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[<span data-ttu-id="9e822-162">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="9e822-162">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="9e822-163">**SetVirtualChannelOptions**</span><span class="sxs-lookup"><span data-stu-id="9e822-163">**SetVirtualChannelOptions**</span></span>](imsrdpclient-setvirtualchanneloptions.md)
</dt> </dl>

 

 





