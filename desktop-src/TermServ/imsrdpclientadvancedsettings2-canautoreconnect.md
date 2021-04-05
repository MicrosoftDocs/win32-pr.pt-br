---
title: Propriedade IMsRdpClientAdvancedSettings2 CanAutoReconnect
description: Especifica se o controle de cliente é capaz de se reconectar automaticamente à sessão atual no caso de uma desconexão de rede.
ms.assetid: 0a7ecf90-832b-4ec1-990b-7fe26ff134b1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade CanAutoReconnect
- Propriedade CanAutoReconnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade CanAutoReconnect
- Propriedade CanAutoReconnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade CanAutoReconnect
- Propriedade CanAutoReconnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade CanAutoReconnect
- Propriedade CanAutoReconnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade CanAutoReconnect
- Propriedade CanAutoReconnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade CanAutoReconnect
- Propriedade CanAutoReconnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade CanAutoReconnect
- Propriedade CanAutoReconnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade CanAutoReconnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.CanAutoReconnect
- IMsRdpClientAdvancedSettings2.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings3.CanAutoReconnect
- IMsRdpClientAdvancedSettings3.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings4.CanAutoReconnect
- IMsRdpClientAdvancedSettings4.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings5.CanAutoReconnect
- IMsRdpClientAdvancedSettings5.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings6.CanAutoReconnect
- IMsRdpClientAdvancedSettings6.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings7.CanAutoReconnect
- IMsRdpClientAdvancedSettings7.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings8.CanAutoReconnect
- IMsRdpClientAdvancedSettings8.get_CanAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8c8f4113c39b79783978252136c50d2111ed0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824176"
---
# <a name="imsrdpclientadvancedsettings2canautoreconnect-property"></a><span data-ttu-id="6e1e8-118">Propriedade IMsRdpClientAdvancedSettings2:: CanAutoReconnect</span><span class="sxs-lookup"><span data-stu-id="6e1e8-118">IMsRdpClientAdvancedSettings2::CanAutoReconnect property</span></span>

<span data-ttu-id="6e1e8-119">Especifica se o controle de cliente é capaz de se reconectar automaticamente à sessão atual no caso de uma desconexão de rede.</span><span class="sxs-lookup"><span data-stu-id="6e1e8-119">Specifies whether the client control is able to reconnect automatically to the current session in the event of a network disconnection.</span></span>

<span data-ttu-id="6e1e8-120">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="6e1e8-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e1e8-121">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e1e8-121">Syntax</span></span>


```C++
HRESULT get_CanAutoReconnect(
  [out] VARIANT_BOOL *pfCanAutoReconnect
);
```



## <a name="property-value"></a><span data-ttu-id="6e1e8-122">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6e1e8-122">Property value</span></span>

<span data-ttu-id="6e1e8-123">Receberá **Variant \_ true** se o controle for capaz de se reconectar automaticamente e **Variant \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6e1e8-123">Receives **VARIANT\_TRUE** if the control is able to automatically reconnect, and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6e1e8-124">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6e1e8-124">Error codes</span></span>

<span data-ttu-id="6e1e8-125">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6e1e8-125">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e1e8-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e1e8-126">Remarks</span></span>

<span data-ttu-id="6e1e8-127">As situações em que a reconexão automática pode não estar habilitada incluem aquelas em que um administrador usa a diretiva de grupo para desabilitar Autoreconnection e ambientes herdados que não dão suporte à reconexão automática.</span><span class="sxs-lookup"><span data-stu-id="6e1e8-127">Situations in which automatic reconnection might not be enabled include those in which an administrator uses group policy to disable autoreconnection, and legacy environments that do not support automatic reconnection.</span></span>

<span data-ttu-id="6e1e8-128">Esta propriedade não pode ser definida quando o controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="6e1e8-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="6e1e8-129">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6e1e8-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e1e8-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e1e8-130">Requirements</span></span>



| <span data-ttu-id="6e1e8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e1e8-131">Requirement</span></span> | <span data-ttu-id="6e1e8-132">Valor</span><span class="sxs-lookup"><span data-stu-id="6e1e8-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e1e8-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e1e8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6e1e8-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e1e8-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="6e1e8-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e1e8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6e1e8-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e1e8-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="6e1e8-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6e1e8-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="6e1e8-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e1e8-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="6e1e8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6e1e8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e1e8-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e1e8-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="6e1e8-141">IID</span><span class="sxs-lookup"><span data-stu-id="6e1e8-141">IID</span></span><br/>                      | <span data-ttu-id="6e1e8-142">IID \_ IMsRdpClientAdvancedSettings2 é definido como 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="6e1e8-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e1e8-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e1e8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e1e8-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="6e1e8-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="6e1e8-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="6e1e8-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="6e1e8-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="6e1e8-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="6e1e8-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6e1e8-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="6e1e8-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6e1e8-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="6e1e8-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6e1e8-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="6e1e8-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="6e1e8-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





