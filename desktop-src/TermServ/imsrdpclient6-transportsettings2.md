---
title: Propriedade IMsRdpClient6 TransportSettings2
description: Recupera a interface IMsRdpClientTransportSettings2.
ms.assetid: 5cd3c745-b360-43fb-b780-c526ed539db0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade TransportSettings2
- Propriedade TransportSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade TransportSettings2
- Propriedade TransportSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade TransportSettings2
- Propriedade TransportSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade TransportSettings2
- Propriedade TransportSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade TransportSettings2
- Propriedade TransportSettings2 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade TransportSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient6.TransportSettings2
- IMsRdpClient6.get_TransportSettings2
- IMsRdpClient7.TransportSettings2
- IMsRdpClient7.get_TransportSettings2
- IMsRdpClient8.TransportSettings2
- IMsRdpClient8.get_TransportSettings2
- IMsRdpClient9.TransportSettings2
- IMsRdpClient9.get_TransportSettings2
- IMsRdpClient10.TransportSettings2
- IMsRdpClient10.get_TransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ba11975e0e065e0cfcce91eb22402153acf236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758098"
---
# <a name="imsrdpclient6transportsettings2-property"></a><span data-ttu-id="d2abd-114">Propriedade IMsRdpClient6:: TransportSettings2</span><span class="sxs-lookup"><span data-stu-id="d2abd-114">IMsRdpClient6::TransportSettings2 property</span></span>

<span data-ttu-id="d2abd-115">Recupera a interface [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="d2abd-115">Retrieves the [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) interface.</span></span>

<span data-ttu-id="d2abd-116">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="d2abd-116">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2abd-117">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2abd-117">Syntax</span></span>


```C++
HRESULT get_TransportSettings2(
  [out] IMsRdpClientTransportSettings2 **ppXportSet2
);
```



## <a name="property-value"></a><span data-ttu-id="d2abd-118">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d2abd-118">Property value</span></span>

<span data-ttu-id="d2abd-119">Um ponteiro de interface [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="d2abd-119">An [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2abd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2abd-120">Requirements</span></span>



| <span data-ttu-id="d2abd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2abd-121">Requirement</span></span> | <span data-ttu-id="d2abd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d2abd-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2abd-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2abd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d2abd-124">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="d2abd-124">Windows Vista with SP1</span></span><br/>                                                      |
| <span data-ttu-id="d2abd-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2abd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d2abd-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2abd-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d2abd-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d2abd-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="d2abd-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2abd-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d2abd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d2abd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2abd-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2abd-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d2abd-131">IID</span><span class="sxs-lookup"><span data-stu-id="d2abd-131">IID</span></span><br/>                      | <span data-ttu-id="d2abd-132">IID \_ IMsRdpClient6 é definido como d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span><span class="sxs-lookup"><span data-stu-id="d2abd-132">IID\_IMsRdpClient6 is defined as d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d2abd-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2abd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2abd-134">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="d2abd-134">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="d2abd-135">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="d2abd-135">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="d2abd-136">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="d2abd-136">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="d2abd-137">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="d2abd-137">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="d2abd-138">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="d2abd-138">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





