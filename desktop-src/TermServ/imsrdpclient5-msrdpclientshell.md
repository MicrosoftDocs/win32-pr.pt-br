---
title: Propriedade IMsRdpClient5 MsRdpClientShell
description: Recupera a interface de configuração de cliente programável IMsRdpClientShell.
ms.assetid: cc56cec4-779d-4b51-8e94-ae0dd9bae997
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade MsRdpClientShell
- Propriedade MsRdpClientShell Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade MsRdpClientShell
- Propriedade MsRdpClientShell Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade MsRdpClientShell
- Propriedade MsRdpClientShell Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade MsRdpClientShell
- Propriedade MsRdpClientShell Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade MsRdpClientShell
- Propriedade MsRdpClientShell Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade MsRdpClientShell
- Propriedade MsRdpClientShell Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade MsRdpClientShell
topic_type:
- apiref
api_name:
- IMsRdpClient5.MsRdpClientShell
- IMsRdpClient5.get_MsRdpClientShell
- IMsRdpClient6.MsRdpClientShell
- IMsRdpClient6.get_MsRdpClientShell
- IMsRdpClient7.MsRdpClientShell
- IMsRdpClient7.get_MsRdpClientShell
- IMsRdpClient8.MsRdpClientShell
- IMsRdpClient8.get_MsRdpClientShell
- IMsRdpClient9.MsRdpClientShell
- IMsRdpClient9.get_MsRdpClientShell
- IMsRdpClient10.MsRdpClientShell
- IMsRdpClient10.get_MsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46129dc4736b50e8b6a650cc7a59f9b238da56e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086388"
---
# <a name="imsrdpclient5msrdpclientshell-property"></a><span data-ttu-id="b9f17-116">Propriedade IMsRdpClient5:: MsRdpClientShell</span><span class="sxs-lookup"><span data-stu-id="b9f17-116">IMsRdpClient5::MsRdpClientShell property</span></span>

<span data-ttu-id="b9f17-117">Recupera a interface de configuração de cliente programável [**IMsRdpClientShell**](imsrdpclientshell.md).</span><span class="sxs-lookup"><span data-stu-id="b9f17-117">Retrieves the scriptable client setting interface [**IMsRdpClientShell**](imsrdpclientshell.md).</span></span>

<span data-ttu-id="b9f17-118">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b9f17-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9f17-119">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9f17-119">Syntax</span></span>


```C++
HRESULT get_MsRdpClientShell(
  [out] IMsRdpClientShell **ppLauncher
);
```



## <a name="property-value"></a><span data-ttu-id="b9f17-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b9f17-120">Property value</span></span>

<span data-ttu-id="b9f17-121">Um ponteiro de interface [**IMsRdpClientShell**](imsrdpclientshell.md) .</span><span class="sxs-lookup"><span data-stu-id="b9f17-121">An [**IMsRdpClientShell**](imsrdpclientshell.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9f17-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9f17-122">Requirements</span></span>



| <span data-ttu-id="b9f17-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9f17-123">Requirement</span></span> | <span data-ttu-id="b9f17-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b9f17-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9f17-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9f17-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b9f17-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9f17-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b9f17-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9f17-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b9f17-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9f17-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b9f17-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b9f17-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="b9f17-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9f17-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b9f17-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b9f17-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9f17-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9f17-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b9f17-133">IID</span><span class="sxs-lookup"><span data-stu-id="b9f17-133">IID</span></span><br/>                      | <span data-ttu-id="b9f17-134">IID \_ IMsRdpClient5 é definido como 4eb5335b-6429-477d-b922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="b9f17-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b9f17-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9f17-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9f17-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="b9f17-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="b9f17-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="b9f17-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="b9f17-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="b9f17-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="b9f17-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="b9f17-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="b9f17-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="b9f17-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="b9f17-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="b9f17-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





