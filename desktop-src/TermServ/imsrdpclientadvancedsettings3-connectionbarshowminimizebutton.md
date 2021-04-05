---
title: Propriedade IMsRdpClientAdvancedSettings3 ConnectionBarShowMinimizeButton
description: Especifica se o botão de minimização deve ser exibido na barra de conexão.
ms.assetid: 3ad89f25-f1ff-4bfc-ae86-09603058c9b5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ConnectionBarShowMinimizeButton
- Propriedade ConnectionBarShowMinimizeButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade ConnectionBarShowMinimizeButton
- Propriedade ConnectionBarShowMinimizeButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade ConnectionBarShowMinimizeButton
- Propriedade ConnectionBarShowMinimizeButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade ConnectionBarShowMinimizeButton
- Propriedade ConnectionBarShowMinimizeButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade ConnectionBarShowMinimizeButton
- Propriedade ConnectionBarShowMinimizeButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade ConnectionBarShowMinimizeButton
- Propriedade ConnectionBarShowMinimizeButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade ConnectionBarShowMinimizeButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowMinimizeButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3cb600a853e4bc2dea7c693e676f992db85f48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644277"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowminimizebutton-property"></a><span data-ttu-id="ca5a7-116">Propriedade IMsRdpClientAdvancedSettings3:: ConnectionBarShowMinimizeButton</span><span class="sxs-lookup"><span data-stu-id="ca5a7-116">IMsRdpClientAdvancedSettings3::ConnectionBarShowMinimizeButton property</span></span>

<span data-ttu-id="ca5a7-117">Especifica se o botão de **minimização** deve ser exibido na barra de conexão.</span><span class="sxs-lookup"><span data-stu-id="ca5a7-117">Specifies whether to display the **Minimize** button on the connection bar.</span></span>

<span data-ttu-id="ca5a7-118">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ca5a7-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca5a7-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca5a7-119">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowMinimizeButton(
  [in]  VARIANT_BOOL fShowMinimize
);

HRESULT get_ConnectionBarShowMinimizeButton(
  [out] VARIANT_BOOL *pfShowMinimize
);
```



## <a name="property-value"></a><span data-ttu-id="ca5a7-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ca5a7-120">Property value</span></span>

<span data-ttu-id="ca5a7-121">Defina esse parâmetro como **Variant \_ true** para exibir o botão **minimizar** e como **Variant \_ false** para desabilitar a exibição do botão **minimizar** .</span><span class="sxs-lookup"><span data-stu-id="ca5a7-121">Set this parameter to **VARIANT\_TRUE** to display the **Minimize** button, and to **VARIANT\_FALSE** to disable the display of the **Minimize** button.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ca5a7-122">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="ca5a7-122">Error codes</span></span>

<span data-ttu-id="ca5a7-123">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ca5a7-123">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca5a7-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca5a7-124">Remarks</span></span>

<span data-ttu-id="ca5a7-125">Esta propriedade não pode ser definida enquanto o controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="ca5a7-125">This property cannot be set while the control is connected.</span></span>

<span data-ttu-id="ca5a7-126">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ca5a7-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca5a7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca5a7-127">Requirements</span></span>



| <span data-ttu-id="ca5a7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca5a7-128">Requirement</span></span> | <span data-ttu-id="ca5a7-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ca5a7-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca5a7-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca5a7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ca5a7-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca5a7-131">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="ca5a7-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca5a7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ca5a7-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca5a7-133">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="ca5a7-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ca5a7-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="ca5a7-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca5a7-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ca5a7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ca5a7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca5a7-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca5a7-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ca5a7-138">IID</span><span class="sxs-lookup"><span data-stu-id="ca5a7-138">IID</span></span><br/>                      | <span data-ttu-id="ca5a7-139">IID \_ IMsRdpClientAdvancedSettings3 é definido como 19cd856b-C542-4c53-ACEE-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="ca5a7-139">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ca5a7-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca5a7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca5a7-141">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ca5a7-141">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ca5a7-142">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ca5a7-142">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ca5a7-143">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ca5a7-143">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ca5a7-144">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ca5a7-144">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ca5a7-145">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ca5a7-145">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ca5a7-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ca5a7-146">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





