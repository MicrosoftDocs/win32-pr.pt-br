---
title: Propriedade IMsRdpClient7 SecuredSettings3
description: Recupera um objeto que dá suporte à interface IMsRdpClientSecuredSettings2.
ms.assetid: 500ce7ed-bd86-434c-baf8-f30dd667dca3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade SecuredSettings3
- Propriedade SecuredSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade SecuredSettings3
- Propriedade SecuredSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade SecuredSettings3
- Propriedade SecuredSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade SecuredSettings3
- Propriedade SecuredSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade SecuredSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.SecuredSettings3
- IMsRdpClient7.get_SecuredSettings3
- IMsRdpClient8.SecuredSettings3
- IMsRdpClient8.get_SecuredSettings3
- IMsRdpClient9.SecuredSettings3
- IMsRdpClient9.get_SecuredSettings3
- IMsRdpClient10.SecuredSettings3
- IMsRdpClient10.get_SecuredSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 219e3373a6ecb2f5b963a82800f4415f7de64534
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369382"
---
# <a name="imsrdpclient7securedsettings3-property"></a><span data-ttu-id="b7679-112">Propriedade IMsRdpClient7:: SecuredSettings3</span><span class="sxs-lookup"><span data-stu-id="b7679-112">IMsRdpClient7::SecuredSettings3 property</span></span>

<span data-ttu-id="b7679-113">Recupera um objeto que dá suporte à interface [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="b7679-113">Retrieves an object that supports the [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) interface.</span></span>

<span data-ttu-id="b7679-114">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b7679-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7679-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7679-115">Syntax</span></span>


```C++
HRESULT get_SecuredSettings3(
  [out] IMsRdpClientSecuredSettings2 **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="b7679-116">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b7679-116">Property value</span></span>

<span data-ttu-id="b7679-117">O endereço de um ponteiro de interface [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) que recebe o objeto.</span><span class="sxs-lookup"><span data-stu-id="b7679-117">The address of an [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7679-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7679-118">Requirements</span></span>



| <span data-ttu-id="b7679-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7679-119">Requirement</span></span> | <span data-ttu-id="b7679-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b7679-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7679-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7679-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b7679-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b7679-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="b7679-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7679-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b7679-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7679-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="b7679-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b7679-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="b7679-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7679-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b7679-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b7679-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7679-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7679-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b7679-129">IID</span><span class="sxs-lookup"><span data-stu-id="b7679-129">IID</span></span><br/>                      | <span data-ttu-id="b7679-130">IID \_ IMsRdpClient7 é definido como b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="b7679-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b7679-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7679-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7679-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="b7679-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="b7679-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="b7679-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="b7679-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="b7679-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="b7679-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="b7679-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





