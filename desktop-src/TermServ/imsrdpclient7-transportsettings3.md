---
title: Propriedade IMsRdpClient7 TransportSettings3
description: Recupera um objeto que dá suporte à interface IMsRdpClientTransportSettings3.
ms.assetid: d11f0943-241e-44cd-a98c-595916ab0718
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade TransportSettings3
- Propriedade TransportSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade TransportSettings3
- Propriedade TransportSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade TransportSettings3
- Propriedade TransportSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade TransportSettings3
- Propriedade TransportSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade TransportSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.TransportSettings3
- IMsRdpClient7.get_TransportSettings3
- IMsRdpClient8.TransportSettings3
- IMsRdpClient8.get_TransportSettings3
- IMsRdpClient9.TransportSettings3
- IMsRdpClient9.get_TransportSettings3
- IMsRdpClient10.TransportSettings3
- IMsRdpClient10.get_TransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c60b58f8f2438de0d43f69ce0b3bb73607e7551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644415"
---
# <a name="imsrdpclient7transportsettings3-property"></a><span data-ttu-id="6e1c9-112">Propriedade IMsRdpClient7:: TransportSettings3</span><span class="sxs-lookup"><span data-stu-id="6e1c9-112">IMsRdpClient7::TransportSettings3 property</span></span>

<span data-ttu-id="6e1c9-113">Recupera um objeto que dá suporte à interface [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="6e1c9-113">Retrieves an object that supports the [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) interface.</span></span>

<span data-ttu-id="6e1c9-114">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="6e1c9-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e1c9-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e1c9-115">Syntax</span></span>


```C++
HRESULT get_TransportSettings3(
  [out, retval] IMsRdpClientTransportSettings3 **ppXportSet3
);
```



## <a name="property-value"></a><span data-ttu-id="6e1c9-116">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6e1c9-116">Property value</span></span>

<span data-ttu-id="6e1c9-117">O endereço de um ponteiro de interface [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) que recebe o objeto.</span><span class="sxs-lookup"><span data-stu-id="6e1c9-117">The address of an [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e1c9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e1c9-118">Requirements</span></span>



| <span data-ttu-id="6e1c9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e1c9-119">Requirement</span></span> | <span data-ttu-id="6e1c9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6e1c9-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e1c9-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e1c9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e1c9-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6e1c9-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="6e1c9-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e1c9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e1c9-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6e1c9-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="6e1c9-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6e1c9-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="6e1c9-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e1c9-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6e1c9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6e1c9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e1c9-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e1c9-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6e1c9-129">IID</span><span class="sxs-lookup"><span data-stu-id="6e1c9-129">IID</span></span><br/>                      | <span data-ttu-id="6e1c9-130">IID \_ IMsRdpClient7 é definido como b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="6e1c9-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6e1c9-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e1c9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e1c9-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="6e1c9-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="6e1c9-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="6e1c9-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="6e1c9-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="6e1c9-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="6e1c9-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="6e1c9-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





