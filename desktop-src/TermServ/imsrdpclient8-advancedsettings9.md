---
title: Propriedade IMsRdpClient8 AdvancedSettings9
description: Contém um objeto que dá suporte à interface IMsRdpClientAdvancedSettings8.
ms.assetid: eb7bf118-15e7-4a11-91b1-e48f18afb436
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AdvancedSettings9
- Propriedade AdvancedSettings9 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade AdvancedSettings9
- Propriedade AdvancedSettings9 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade AdvancedSettings9
- Propriedade AdvancedSettings9 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade AdvancedSettings9
topic_type:
- apiref
api_name:
- IMsRdpClient8.AdvancedSettings9
- IMsRdpClient8.get_AdvancedSettings9
- IMsRdpClient9.AdvancedSettings9
- IMsRdpClient9.get_AdvancedSettings9
- IMsRdpClient10.AdvancedSettings9
- IMsRdpClient10.get_AdvancedSettings9
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fce4c6f07b0c6c798d613e5312b3ae2b258c9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761332"
---
# <a name="imsrdpclient8advancedsettings9-property"></a><span data-ttu-id="71b20-110">Propriedade IMsRdpClient8:: AdvancedSettings9</span><span class="sxs-lookup"><span data-stu-id="71b20-110">IMsRdpClient8::AdvancedSettings9 property</span></span>

<span data-ttu-id="71b20-111">Contém um objeto que dá suporte à interface [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) .</span><span class="sxs-lookup"><span data-stu-id="71b20-111">Contains an object that supports the [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) interface.</span></span>

<span data-ttu-id="71b20-112">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="71b20-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="71b20-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71b20-113">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings9(
  [out, retval] IMsRdpClientAdvancedSettings8 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="71b20-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="71b20-114">Property value</span></span>

<span data-ttu-id="71b20-115">Uma interface [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) que representa o objeto de configurações.</span><span class="sxs-lookup"><span data-stu-id="71b20-115">An [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) interface that represents the settings object.</span></span>

## <a name="requirements"></a><span data-ttu-id="71b20-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71b20-116">Requirements</span></span>



| <span data-ttu-id="71b20-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="71b20-117">Requirement</span></span> | <span data-ttu-id="71b20-118">Valor</span><span class="sxs-lookup"><span data-stu-id="71b20-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71b20-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71b20-119">Minimum supported client</span></span><br/> | <span data-ttu-id="71b20-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="71b20-120">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="71b20-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71b20-121">Minimum supported server</span></span><br/> | <span data-ttu-id="71b20-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="71b20-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="71b20-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="71b20-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="71b20-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71b20-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="71b20-125">DLL</span><span class="sxs-lookup"><span data-stu-id="71b20-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71b20-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71b20-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="71b20-127">IID</span><span class="sxs-lookup"><span data-stu-id="71b20-127">IID</span></span><br/>                      | <span data-ttu-id="71b20-128">IID \_ IMsRdpClient8 é definido como 4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="71b20-128">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="71b20-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="71b20-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b20-130">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="71b20-130">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="71b20-131">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="71b20-131">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="71b20-132">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="71b20-132">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





