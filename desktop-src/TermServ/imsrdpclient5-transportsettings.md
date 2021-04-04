---
title: Propriedade IMsRdpClient5 TransportSettings
description: Recupera o que passou por um script para a interface IMsRdpClientTransportSettings.
ms.assetid: 38f5a735-55c7-425a-835b-22f6e0900d57
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade TransportSettings
- Propriedade TransportSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade TransportSettings
- Propriedade TransportSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade TransportSettings
- Propriedade TransportSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade TransportSettings
- Propriedade TransportSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade TransportSettings
- Propriedade TransportSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade TransportSettings
- Propriedade TransportSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade TransportSettings
topic_type:
- apiref
api_name:
- IMsRdpClient5.TransportSettings
- IMsRdpClient5.get_TransportSettings
- IMsRdpClient6.TransportSettings
- IMsRdpClient6.get_TransportSettings
- IMsRdpClient7.TransportSettings
- IMsRdpClient7.get_TransportSettings
- IMsRdpClient8.TransportSettings
- IMsRdpClient8.get_TransportSettings
- IMsRdpClient9.TransportSettings
- IMsRdpClient9.get_TransportSettings
- IMsRdpClient10.TransportSettings
- IMsRdpClient10.get_TransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077ed94253c0ebadeed775e54c4db2ae6cbacf13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085305"
---
# <a name="imsrdpclient5transportsettings-property"></a><span data-ttu-id="3ac5b-116">Propriedade IMsRdpClient5:: TransportSettings</span><span class="sxs-lookup"><span data-stu-id="3ac5b-116">IMsRdpClient5::TransportSettings property</span></span>

<span data-ttu-id="3ac5b-117">Recupera o que passou por um script para a interface [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="3ac5b-117">Retrieves what was passed through a script to the [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) interface.</span></span>

<span data-ttu-id="3ac5b-118">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3ac5b-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ac5b-119">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ac5b-119">Syntax</span></span>


```C++
HRESULT get_TransportSettings(
  [out] IMsRdpClientTransportSettings **ppXportSet
);
```



## <a name="property-value"></a><span data-ttu-id="3ac5b-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3ac5b-120">Property value</span></span>

<span data-ttu-id="3ac5b-121">Um ponteiro de interface [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="3ac5b-121">An [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ac5b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ac5b-122">Requirements</span></span>



| <span data-ttu-id="3ac5b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ac5b-123">Requirement</span></span> | <span data-ttu-id="3ac5b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3ac5b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac5b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ac5b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3ac5b-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ac5b-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3ac5b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ac5b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3ac5b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ac5b-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3ac5b-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3ac5b-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="3ac5b-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ac5b-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ac5b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3ac5b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ac5b-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ac5b-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ac5b-133">IID</span><span class="sxs-lookup"><span data-stu-id="3ac5b-133">IID</span></span><br/>                      | <span data-ttu-id="3ac5b-134">IID \_ IMsRdpClient5 é definido como 4eb5335b-6429-477d-b922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="3ac5b-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3ac5b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ac5b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ac5b-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="3ac5b-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="3ac5b-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="3ac5b-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="3ac5b-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="3ac5b-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="3ac5b-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="3ac5b-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="3ac5b-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="3ac5b-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="3ac5b-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="3ac5b-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





