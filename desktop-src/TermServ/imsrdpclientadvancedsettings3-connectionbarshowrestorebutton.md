---
title: Propriedade IMsRdpClientAdvancedSettings3 ConnectionBarShowRestoreButton
description: Especifica se o botão de restauração deve ser exibido na barra de conexão.
ms.assetid: a56c3c05-d253-404a-bf49-9c1d804802e0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ConnectionBarShowRestoreButton
- Propriedade ConnectionBarShowRestoreButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade ConnectionBarShowRestoreButton
- Propriedade ConnectionBarShowRestoreButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade ConnectionBarShowRestoreButton
- Propriedade ConnectionBarShowRestoreButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade ConnectionBarShowRestoreButton
- Propriedade ConnectionBarShowRestoreButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade ConnectionBarShowRestoreButton
- Propriedade ConnectionBarShowRestoreButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade ConnectionBarShowRestoreButton
- Propriedade ConnectionBarShowRestoreButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade ConnectionBarShowRestoreButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowRestoreButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae83ecde31461eff9c553782b8bfa3ae760fb54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369306"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowrestorebutton-property"></a><span data-ttu-id="a7850-116">Propriedade IMsRdpClientAdvancedSettings3:: ConnectionBarShowRestoreButton</span><span class="sxs-lookup"><span data-stu-id="a7850-116">IMsRdpClientAdvancedSettings3::ConnectionBarShowRestoreButton property</span></span>

<span data-ttu-id="a7850-117">Especifica se o botão de **restauração** deve ser exibido na barra de conexão.</span><span class="sxs-lookup"><span data-stu-id="a7850-117">Specifies whether to display the **Restore** button on the connection bar.</span></span>

<span data-ttu-id="a7850-118">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a7850-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7850-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7850-119">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowRestoreButton(
  [in]  VARIANT_BOOL fShowRestore
);

HRESULT get_ConnectionBarShowRestoreButton(
  [out] VARIANT_BOOL *pfShowRestore
);
```



## <a name="property-value"></a><span data-ttu-id="a7850-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a7850-120">Property value</span></span>

<span data-ttu-id="a7850-121">Defina como **Variant \_ true** para exibir o botão de **restauração** e para a **variante \_ false** para desabilitar a exibição do botão **restaurar** .</span><span class="sxs-lookup"><span data-stu-id="a7850-121">Set to **VARIANT\_TRUE** to display the **Restore** button, and to **VARIANT\_FALSE** to disable the display of the **Restore** button.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a7850-122">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a7850-122">Error codes</span></span>

<span data-ttu-id="a7850-123">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a7850-123">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7850-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7850-124">Remarks</span></span>

<span data-ttu-id="a7850-125">Esta propriedade não pode ser definida enquanto o controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="a7850-125">This property cannot be set while the control is connected.</span></span>

<span data-ttu-id="a7850-126">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a7850-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7850-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7850-127">Requirements</span></span>



| <span data-ttu-id="a7850-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7850-128">Requirement</span></span> | <span data-ttu-id="a7850-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a7850-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7850-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7850-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a7850-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7850-131">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="a7850-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7850-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a7850-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7850-133">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="a7850-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a7850-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="a7850-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7850-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a7850-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a7850-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7850-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7850-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a7850-138">IID</span><span class="sxs-lookup"><span data-stu-id="a7850-138">IID</span></span><br/>                      | <span data-ttu-id="a7850-139">IID \_ IMsRdpClientAdvancedSettings3 é definido como 19cd856b-C542-4c53-ACEE-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="a7850-139">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7850-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7850-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7850-141">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a7850-141">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a7850-142">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a7850-142">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a7850-143">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a7850-143">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a7850-144">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a7850-144">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a7850-145">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a7850-145">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a7850-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a7850-146">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





