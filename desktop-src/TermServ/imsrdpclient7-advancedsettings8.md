---
title: Propriedade IMsRdpClient7 AdvancedSettings8
description: Recupera um objeto que dá suporte à interface IMsRdpClientAdvancedSettings7.
ms.assetid: e3bb3b74-52db-4ec2-999c-9d12c24f65be
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AdvancedSettings8
- Propriedade AdvancedSettings8 Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade AdvancedSettings8
- Propriedade AdvancedSettings8 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade AdvancedSettings8
- Propriedade AdvancedSettings8 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade AdvancedSettings8
- Propriedade AdvancedSettings8 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade AdvancedSettings8
topic_type:
- apiref
api_name:
- IMsRdpClient7.AdvancedSettings8
- IMsRdpClient7.get_AdvancedSettings8
- IMsRdpClient8.AdvancedSettings8
- IMsRdpClient8.get_AdvancedSettings8
- IMsRdpClient9.AdvancedSettings8
- IMsRdpClient9.get_AdvancedSettings8
- IMsRdpClient10.AdvancedSettings8
- IMsRdpClient10.get_AdvancedSettings8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 887306216682ba1555739a4258b8337694fabe0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085268"
---
# <a name="imsrdpclient7advancedsettings8-property"></a><span data-ttu-id="9f136-112">Propriedade IMsRdpClient7:: AdvancedSettings8</span><span class="sxs-lookup"><span data-stu-id="9f136-112">IMsRdpClient7::AdvancedSettings8 property</span></span>

<span data-ttu-id="9f136-113">Recupera um objeto que dá suporte à interface [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) .</span><span class="sxs-lookup"><span data-stu-id="9f136-113">Retrieves an object that supports the [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface.</span></span>

<span data-ttu-id="9f136-114">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="9f136-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f136-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f136-115">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings8(
  [out, retval] IMsRdpClientAdvancedSettings7 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="9f136-116">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9f136-116">Property value</span></span>

<span data-ttu-id="9f136-117">O endereço de um ponteiro de interface [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) que recebe o objeto.</span><span class="sxs-lookup"><span data-stu-id="9f136-117">The address of an [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f136-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f136-118">Requirements</span></span>



| <span data-ttu-id="9f136-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f136-119">Requirement</span></span> | <span data-ttu-id="9f136-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9f136-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f136-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f136-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9f136-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9f136-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="9f136-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f136-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9f136-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f136-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="9f136-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9f136-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="9f136-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f136-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9f136-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9f136-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f136-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f136-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9f136-129">IID</span><span class="sxs-lookup"><span data-stu-id="9f136-129">IID</span></span><br/>                      | <span data-ttu-id="9f136-130">IID \_ IMsRdpClient7 é definido como b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="9f136-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9f136-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f136-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f136-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="9f136-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="9f136-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="9f136-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="9f136-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="9f136-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="9f136-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="9f136-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





