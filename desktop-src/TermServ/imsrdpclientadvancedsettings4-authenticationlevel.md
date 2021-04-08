---
title: Propriedade IMsRdpClientAdvancedSettings4 AuthenticationLevel
description: Especifica o nível de autenticação a ser usado para a conexão.
ms.assetid: 09ff1508-f13d-4bb0-8458-6f5a5e099bae
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AuthenticationLevel
- Propriedade AuthenticationLevel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, propriedade AuthenticationLevel
- Propriedade AuthenticationLevel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, propriedade AuthenticationLevel
- Propriedade AuthenticationLevel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, propriedade AuthenticationLevel
- Propriedade AuthenticationLevel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, propriedade AuthenticationLevel
- Propriedade AuthenticationLevel Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, propriedade AuthenticationLevel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4.AuthenticationLevel
- IMsRdpClientAdvancedSettings4.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings4.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.AuthenticationLevel
- IMsRdpClientAdvancedSettings5.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.AuthenticationLevel
- IMsRdpClientAdvancedSettings6.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.AuthenticationLevel
- IMsRdpClientAdvancedSettings7.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.AuthenticationLevel
- IMsRdpClientAdvancedSettings8.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.put_AuthenticationLevel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c748416650ec7e6ec3d26fe6236a254eb012d67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824356"
---
# <a name="imsrdpclientadvancedsettings4authenticationlevel-property"></a><span data-ttu-id="77ea5-114">Propriedade IMsRdpClientAdvancedSettings4:: AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="77ea5-114">IMsRdpClientAdvancedSettings4::AuthenticationLevel property</span></span>

<span data-ttu-id="77ea5-115">Especifica o nível de autenticação a ser usado para a conexão.</span><span class="sxs-lookup"><span data-stu-id="77ea5-115">Specifies the authentication level to use for the connection.</span></span>

<span data-ttu-id="77ea5-116">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="77ea5-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ea5-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="77ea5-117">Syntax</span></span>


```C++
HRESULT put_AuthenticationLevel(
  [in]  UINT uiAuthLevel
);

HRESULT get_AuthenticationLevel(
  [out] UINT *puiAuthLevel
);
```



## <a name="property-value"></a><span data-ttu-id="77ea5-118">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="77ea5-118">Property value</span></span>

<span data-ttu-id="77ea5-119">O valor da propriedade **AuthenticationLevel** .</span><span class="sxs-lookup"><span data-stu-id="77ea5-119">The value of the **AuthenticationLevel** property.</span></span>

<dt>

<span data-ttu-id="77ea5-120">0</span><span class="sxs-lookup"><span data-stu-id="77ea5-120">0</span></span>
</dt> <dd>

<span data-ttu-id="77ea5-121">Nenhuma autenticação do servidor.</span><span class="sxs-lookup"><span data-stu-id="77ea5-121">No authentication of the server.</span></span>

</dd> <dt>

<span data-ttu-id="77ea5-122">1</span><span class="sxs-lookup"><span data-stu-id="77ea5-122">1</span></span>
</dt> <dd>

<span data-ttu-id="77ea5-123">A autenticação do servidor é necessária e deve ser concluída com êxito para que a conexão continue.</span><span class="sxs-lookup"><span data-stu-id="77ea5-123">Server authentication is required and must complete successfully for the connection to proceed.</span></span>

</dd> <dt>

<span data-ttu-id="77ea5-124">2</span><span class="sxs-lookup"><span data-stu-id="77ea5-124">2</span></span>
</dt> <dd>

<span data-ttu-id="77ea5-125">Tente a autenticação do servidor.</span><span class="sxs-lookup"><span data-stu-id="77ea5-125">Attempt authentication of the server.</span></span> <span data-ttu-id="77ea5-126">Se a autenticação falhar, o usuário será solicitado com a opção de cancelar a conexão ou continuar sem autenticação do servidor.</span><span class="sxs-lookup"><span data-stu-id="77ea5-126">If authentication fails, the user will be prompted with the option to cancel the connection or to proceed without server authentication.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="77ea5-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="77ea5-127">Error codes</span></span>

<span data-ttu-id="77ea5-128">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="77ea5-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="77ea5-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="77ea5-129">Remarks</span></span>

<span data-ttu-id="77ea5-130">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="77ea5-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77ea5-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77ea5-131">Requirements</span></span>



| <span data-ttu-id="77ea5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="77ea5-132">Requirement</span></span> | <span data-ttu-id="77ea5-133">Valor</span><span class="sxs-lookup"><span data-stu-id="77ea5-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77ea5-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77ea5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="77ea5-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77ea5-135">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="77ea5-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77ea5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="77ea5-137">Windows Server 2008, Windows Server 2008 com SP1</span><span class="sxs-lookup"><span data-stu-id="77ea5-137">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                     |
| <span data-ttu-id="77ea5-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="77ea5-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="77ea5-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77ea5-139"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="77ea5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="77ea5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77ea5-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77ea5-141"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="77ea5-142">IID</span><span class="sxs-lookup"><span data-stu-id="77ea5-142">IID</span></span><br/>                      | <span data-ttu-id="77ea5-143">IID \_ IMsRdpClientAdvancedSettings4 é definido como FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span><span class="sxs-lookup"><span data-stu-id="77ea5-143">IID\_IMsRdpClientAdvancedSettings4 is defined as FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77ea5-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="77ea5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77ea5-145">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="77ea5-145">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="77ea5-146">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="77ea5-146">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="77ea5-147">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="77ea5-147">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="77ea5-148">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="77ea5-148">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="77ea5-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="77ea5-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> </dl>

 

 





