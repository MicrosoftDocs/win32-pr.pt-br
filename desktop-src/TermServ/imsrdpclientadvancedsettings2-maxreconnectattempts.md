---
title: Propriedade IMsRdpClientAdvancedSettings2 MaxReconnectAttempts
description: Especifica o número de vezes para tentar se reconectar durante a reconexão automática.
ms.assetid: 24bfd3b6-d2de-4e46-8b5f-a4702c18a93c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade MaxReconnectAttempts
- Propriedade MaxReconnectAttempts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade MaxReconnectAttempts
- Propriedade MaxReconnectAttempts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade MaxReconnectAttempts
- Propriedade MaxReconnectAttempts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade MaxReconnectAttempts
- Propriedade MaxReconnectAttempts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade MaxReconnectAttempts
- Propriedade MaxReconnectAttempts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade MaxReconnectAttempts
- Propriedade MaxReconnectAttempts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade MaxReconnectAttempts
- Propriedade MaxReconnectAttempts Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade MaxReconnectAttempts
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.put_MaxReconnectAttempts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322796a2d6ca6a13476dad58af8c385b8bdfa1fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810442"
---
# <a name="imsrdpclientadvancedsettings2maxreconnectattempts-property"></a><span data-ttu-id="7edad-118">Propriedade IMsRdpClientAdvancedSettings2:: MaxReconnectAttempts</span><span class="sxs-lookup"><span data-stu-id="7edad-118">IMsRdpClientAdvancedSettings2::MaxReconnectAttempts property</span></span>

<span data-ttu-id="7edad-119">Especifica o número de vezes para tentar se reconectar durante a reconexão automática.</span><span class="sxs-lookup"><span data-stu-id="7edad-119">Specifies the number of times to try to reconnect during automatic reconnection.</span></span>

<span data-ttu-id="7edad-120">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7edad-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7edad-121">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7edad-121">Syntax</span></span>


```C++
HRESULT put_MaxReconnectAttempts(
  [in]  LONG MaxReconnectAttempts
);

HRESULT get_MaxReconnectAttempts(
  [out] LONG *pMaxReconnectAttempts
);
```



## <a name="property-value"></a><span data-ttu-id="7edad-122">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7edad-122">Property value</span></span>

<span data-ttu-id="7edad-123">O novo número de novas tentativas.</span><span class="sxs-lookup"><span data-stu-id="7edad-123">The new number of retries.</span></span> <span data-ttu-id="7edad-124">Os valores válidos são de 0 a 200, inclusive.</span><span class="sxs-lookup"><span data-stu-id="7edad-124">The valid values are 0 to 200, inclusive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7edad-125">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7edad-125">Error codes</span></span>

<span data-ttu-id="7edad-126">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7edad-126">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7edad-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="7edad-127">Remarks</span></span>

<span data-ttu-id="7edad-128">Esta propriedade não pode ser definida quando o controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="7edad-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="7edad-129">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7edad-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7edad-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7edad-130">Requirements</span></span>



| <span data-ttu-id="7edad-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7edad-131">Requirement</span></span> | <span data-ttu-id="7edad-132">Valor</span><span class="sxs-lookup"><span data-stu-id="7edad-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7edad-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7edad-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7edad-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7edad-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="7edad-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7edad-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7edad-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7edad-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="7edad-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7edad-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="7edad-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7edad-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7edad-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7edad-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7edad-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7edad-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="7edad-141">IID</span><span class="sxs-lookup"><span data-stu-id="7edad-141">IID</span></span><br/>                      | <span data-ttu-id="7edad-142">IID \_ IMsRdpClientAdvancedSettings2 é definido como 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="7edad-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7edad-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="7edad-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7edad-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="7edad-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7edad-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="7edad-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="7edad-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="7edad-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="7edad-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7edad-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="7edad-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7edad-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="7edad-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7edad-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7edad-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="7edad-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





