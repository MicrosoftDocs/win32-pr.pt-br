---
title: Propriedade IMsRdpClient5 RemoteProgram
description: Recupera um objeto que dá suporte à interface ITSRemoteProgram.
ms.assetid: 013f613b-af7b-4cc5-be1f-d45833806e3b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RemoteProgram
- Propriedade RemoteProgram Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade RemoteProgram
- Propriedade RemoteProgram Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade RemoteProgram
- Propriedade RemoteProgram Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade RemoteProgram
- Propriedade RemoteProgram Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade RemoteProgram
- Propriedade RemoteProgram Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade RemoteProgram
- Propriedade RemoteProgram Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade RemoteProgram
topic_type:
- apiref
api_name:
- IMsRdpClient5.RemoteProgram
- IMsRdpClient5.get_RemoteProgram
- IMsRdpClient6.RemoteProgram
- IMsRdpClient6.get_RemoteProgram
- IMsRdpClient7.RemoteProgram
- IMsRdpClient7.get_RemoteProgram
- IMsRdpClient8.RemoteProgram
- IMsRdpClient8.get_RemoteProgram
- IMsRdpClient9.RemoteProgram
- IMsRdpClient9.get_RemoteProgram
- IMsRdpClient10.RemoteProgram
- IMsRdpClient10.get_RemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 267e367af090a7fd70e9482406104fd0403d63f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454837"
---
# <a name="imsrdpclient5remoteprogram-property"></a><span data-ttu-id="d0443-116">Propriedade IMsRdpClient5:: RemoteProgram</span><span class="sxs-lookup"><span data-stu-id="d0443-116">IMsRdpClient5::RemoteProgram property</span></span>

<span data-ttu-id="d0443-117">Recupera um objeto que dá suporte à interface [**ITSRemoteProgram**](itsremoteprogram.md) .</span><span class="sxs-lookup"><span data-stu-id="d0443-117">Retrieves an object that supports the [**ITSRemoteProgram**](itsremoteprogram.md) interface.</span></span>

<span data-ttu-id="d0443-118">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="d0443-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0443-119">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0443-119">Syntax</span></span>


```C++
HRESULT get_RemoteProgram(
  [out] ITSRemoteProgram **ppRemoteProgram
);
```



## <a name="property-value"></a><span data-ttu-id="d0443-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d0443-120">Property value</span></span>

<span data-ttu-id="d0443-121">Um ponteiro de interface [**ITSRemoteProgram**](itsremoteprogram.md) .</span><span class="sxs-lookup"><span data-stu-id="d0443-121">An [**ITSRemoteProgram**](itsremoteprogram.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0443-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0443-122">Requirements</span></span>



| <span data-ttu-id="d0443-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0443-123">Requirement</span></span> | <span data-ttu-id="d0443-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d0443-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0443-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0443-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d0443-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0443-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d0443-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0443-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d0443-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0443-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d0443-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d0443-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0443-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0443-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0443-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d0443-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0443-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0443-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0443-133">IID</span><span class="sxs-lookup"><span data-stu-id="d0443-133">IID</span></span><br/>                      | <span data-ttu-id="d0443-134">IID \_ IMsRdpClient5 é definido como 4eb5335b-6429-477d-b922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="d0443-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d0443-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0443-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0443-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="d0443-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="d0443-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="d0443-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="d0443-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="d0443-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="d0443-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="d0443-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="d0443-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="d0443-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="d0443-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="d0443-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





