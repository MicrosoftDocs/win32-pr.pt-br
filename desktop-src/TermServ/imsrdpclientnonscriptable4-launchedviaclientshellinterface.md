---
title: Propriedade IMsRdpClientNonScriptable4 LaunchedViaClientShellInterface
description: Especifica se o usuário iniciou o controle de cliente usando a interface Acesso via Web à Área de Trabalho Remota (RD Acesso via Web).
ms.assetid: bf72c375-0eec-49c7-9f9a-c7545a95bdce
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade LaunchedViaClientShellInterface
- Propriedade LaunchedViaClientShellInterface Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade LaunchedViaClientShellInterface
- Propriedade LaunchedViaClientShellInterface Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade LaunchedViaClientShellInterface
- Propriedade LaunchedViaClientShellInterface Serviços de Área de Trabalho Remota, objeto MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota, Propriedade LaunchedViaClientShellInterface
- Propriedade LaunchedViaClientShellInterface Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade LaunchedViaClientShellInterface
- Propriedade LaunchedViaClientShellInterface Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade LaunchedViaClientShellInterface
- Propriedade LaunchedViaClientShellInterface Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade LaunchedViaClientShellInterface
- Propriedade LaunchedViaClientShellInterface Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade LaunchedViaClientShellInterface
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.put_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.put_LaunchedViaClientShellInterface
- MsRdpClient5.LaunchedViaClientShellInterface
- MsRdpClient6.LaunchedViaClientShellInterface
- MsRdpClient7.LaunchedViaClientShellInterface
- MsRdpClient8.LaunchedViaClientShellInterface
- MsRdpClient9.LaunchedViaClientShellInterface
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d5854a4e75be455035fd9a123418bd486932379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918653"
---
# <a name="imsrdpclientnonscriptable4launchedviaclientshellinterface-property"></a><span data-ttu-id="4fe12-118">Propriedade IMsRdpClientNonScriptable4:: LaunchedViaClientShellInterface</span><span class="sxs-lookup"><span data-stu-id="4fe12-118">IMsRdpClientNonScriptable4::LaunchedViaClientShellInterface property</span></span>

<span data-ttu-id="4fe12-119">Especifica se o usuário iniciou o controle de cliente usando a interface Acesso via Web à Área de Trabalho Remota (RD Acesso via Web).</span><span class="sxs-lookup"><span data-stu-id="4fe12-119">Specifies whether the user launched the client control by using the Remote Desktop Web Access (RD Web Access) interface.</span></span>

<span data-ttu-id="4fe12-120">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4fe12-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fe12-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fe12-121">Syntax</span></span>


```C++
HRESULT put_LaunchedViaClientShellInterface(
  [in]  VARIANT_BOOL fLaunchedViaClientShellInterface
);

HRESULT get_LaunchedViaClientShellInterface(
  [out]  VARIANT_BOOL *pfLaunchedViaClientShellInterface
);
```



## <a name="property-value"></a><span data-ttu-id="4fe12-122">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4fe12-122">Property value</span></span>

<span data-ttu-id="4fe12-123">Define a propriedade **LaunchedViaClientShellInterface** .</span><span class="sxs-lookup"><span data-stu-id="4fe12-123">Sets the **LaunchedViaClientShellInterface** property.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4fe12-124">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4fe12-124">Error codes</span></span>

<span data-ttu-id="4fe12-125">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4fe12-125">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fe12-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fe12-126">Requirements</span></span>



| <span data-ttu-id="4fe12-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fe12-127">Requirement</span></span> | <span data-ttu-id="4fe12-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4fe12-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe12-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4fe12-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4fe12-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4fe12-130">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="4fe12-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4fe12-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4fe12-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fe12-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4fe12-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4fe12-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="4fe12-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fe12-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="4fe12-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4fe12-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fe12-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fe12-136"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="4fe12-137">IID</span><span class="sxs-lookup"><span data-stu-id="4fe12-137">IID</span></span><br/>                      | <span data-ttu-id="4fe12-138">IMsRdpClientNonScriptable4 é definido como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="4fe12-138">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4fe12-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fe12-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fe12-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="4fe12-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="4fe12-141">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="4fe12-141">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





