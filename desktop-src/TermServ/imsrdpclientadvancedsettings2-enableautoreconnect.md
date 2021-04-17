---
title: Propriedade IMsRdpClientAdvancedSettings2 EnableAutoReconnect
description: Especifica se o controle de cliente deve ser habilitado para se reconectar automaticamente a uma sessão no caso de uma desconexão de rede.
ms.assetid: 9d820f78-bf7f-479a-ae6f-be0f0abe549c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade EnableAutoReconnect
- Propriedade EnableAutoReconnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade EnableAutoReconnect
- Propriedade EnableAutoReconnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade EnableAutoReconnect
- Propriedade EnableAutoReconnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade EnableAutoReconnect
- Propriedade EnableAutoReconnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade EnableAutoReconnect
- Propriedade EnableAutoReconnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade EnableAutoReconnect
- Propriedade EnableAutoReconnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade EnableAutoReconnect
- Propriedade EnableAutoReconnect Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade EnableAutoReconnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.put_EnableAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f8d4a1345395b5b5843872df256fe7a113094e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761937"
---
# <a name="imsrdpclientadvancedsettings2enableautoreconnect-property"></a><span data-ttu-id="e673b-118">Propriedade IMsRdpClientAdvancedSettings2:: EnableAutoReconnect</span><span class="sxs-lookup"><span data-stu-id="e673b-118">IMsRdpClientAdvancedSettings2::EnableAutoReconnect property</span></span>

<span data-ttu-id="e673b-119">Especifica se o controle de cliente deve ser habilitado para se reconectar automaticamente a uma sessão no caso de uma desconexão de rede.</span><span class="sxs-lookup"><span data-stu-id="e673b-119">Specifies whether to enable the client control to reconnect automatically to a session in the event of a network disconnection.</span></span>

<span data-ttu-id="e673b-120">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e673b-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e673b-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="e673b-121">Syntax</span></span>


```C++
HRESULT put_EnableAutoReconnect(
  [in]  VARIANT_BOOL fEnableAutoReconnect
);

HRESULT get_EnableAutoReconnect(
  [out] VARIANT_BOOL *pfEnableAutoReconnect
);
```



## <a name="property-value"></a><span data-ttu-id="e673b-122">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e673b-122">Property value</span></span>

<span data-ttu-id="e673b-123">Defina como **Variant \_ true** para habilitar a reconexão automática e para a **variante \_ false** para desabilitá-la.</span><span class="sxs-lookup"><span data-stu-id="e673b-123">Set to **VARIANT\_TRUE** to enable automatic reconnection, and to **VARIANT\_FALSE** to disable it.</span></span> <span data-ttu-id="e673b-124">O padrão é **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="e673b-124">The default is **VARIANT\_TRUE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e673b-125">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e673b-125">Error codes</span></span>

<span data-ttu-id="e673b-126">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e673b-126">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e673b-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="e673b-127">Remarks</span></span>

<span data-ttu-id="e673b-128">Esta propriedade não pode ser definida quando o controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="e673b-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="e673b-129">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e673b-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e673b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e673b-130">Requirements</span></span>



| <span data-ttu-id="e673b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e673b-131">Requirement</span></span> | <span data-ttu-id="e673b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e673b-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e673b-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e673b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e673b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e673b-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="e673b-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e673b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e673b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e673b-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="e673b-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e673b-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="e673b-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e673b-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e673b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e673b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e673b-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e673b-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e673b-141">IID</span><span class="sxs-lookup"><span data-stu-id="e673b-141">IID</span></span><br/>                      | <span data-ttu-id="e673b-142">IID \_ IMsRdpClientAdvancedSettings2 é definido como 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="e673b-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e673b-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e673b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e673b-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e673b-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e673b-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e673b-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e673b-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e673b-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e673b-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e673b-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e673b-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e673b-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e673b-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e673b-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e673b-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e673b-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





