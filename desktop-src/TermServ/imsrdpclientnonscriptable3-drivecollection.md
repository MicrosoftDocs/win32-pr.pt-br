---
title: Propriedade IMsRdpClientNonScriptable3 da Unidadecollection
description: Recupera a coleção de objetos de unidade a ser redirecionada.
ms.assetid: 5aaac605-584b-442e-9d67-1cb8213a70b3
ms.tgt_platform: multiple
keywords:
- Propriedade drivecollection Serviços de Área de Trabalho Remota
- Propriedade drivecollection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade Drivecollection
- Propriedade drivecollection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade Drivecollection
- Propriedade drivecollection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade Drivecollection
- Propriedade drivecollection Serviços de Área de Trabalho Remota, objeto MsRdpClient5
- Serviços de Área de Trabalho Remota de objeto MsRdpClient5, Propriedade Drivecollection
- Propriedade drivecollection Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Serviços de Área de Trabalho Remota de objeto MsRdpClient6, Propriedade Drivecollection
- Propriedade drivecollection Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Serviços de Área de Trabalho Remota de objeto MsRdpClient7, Propriedade Drivecollection
- Propriedade drivecollection Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Serviços de Área de Trabalho Remota de objeto MsRdpClient8, Propriedade Drivecollection
- Propriedade drivecollection Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Serviços de Área de Trabalho Remota de objeto MsRdpClient9, Propriedade Drivecollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DriveCollection
- IMsRdpClientNonScriptable3.get_DriveCollection
- IMsRdpClientNonScriptable4.DriveCollection
- IMsRdpClientNonScriptable4.get_DriveCollection
- IMsRdpClientNonScriptable5.DriveCollection
- IMsRdpClientNonScriptable5.get_DriveCollection
- MsRdpClient5.DriveCollection
- MsRdpClient6.DriveCollection
- MsRdpClient7.DriveCollection
- MsRdpClient8.DriveCollection
- MsRdpClient9.DriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37d4bfcaa52d483adc8b0d0885d8316f10ce01d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454835"
---
# <a name="imsrdpclientnonscriptable3drivecollection-property"></a><span data-ttu-id="9113a-120">IMsRdpClientNonScriptable3::D Propriedade rivescollection</span><span class="sxs-lookup"><span data-stu-id="9113a-120">IMsRdpClientNonScriptable3::DriveCollection property</span></span>

<span data-ttu-id="9113a-121">Recupera a coleção de objetos de unidade a ser redirecionada.</span><span class="sxs-lookup"><span data-stu-id="9113a-121">Retrieves the collection of drive objects to be redirected.</span></span>

<span data-ttu-id="9113a-122">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="9113a-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9113a-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9113a-123">Syntax</span></span>


```C++
HRESULT get_DriveCollection(
  [out] IMsRdpDriveCollection **ppDriveCollection
);
```



## <a name="property-value"></a><span data-ttu-id="9113a-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9113a-124">Property value</span></span>

<span data-ttu-id="9113a-125">Recupera a coleção de objetos de unidade do tipo [**IMSRdpDrive**](imsrdpdrive.md).</span><span class="sxs-lookup"><span data-stu-id="9113a-125">Retrieves the collection of drive objects of type [**IMSRdpDrive**](imsrdpdrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9113a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9113a-126">Requirements</span></span>



| <span data-ttu-id="9113a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9113a-127">Requirement</span></span> | <span data-ttu-id="9113a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="9113a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9113a-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9113a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9113a-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9113a-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="9113a-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9113a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9113a-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9113a-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="9113a-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9113a-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="9113a-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9113a-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="9113a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9113a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9113a-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9113a-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="9113a-137">IID</span><span class="sxs-lookup"><span data-stu-id="9113a-137">IID</span></span><br/>                      | <span data-ttu-id="9113a-138">IID \_ IMsRdpClientNonScriptable3 é definido como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="9113a-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9113a-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="9113a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9113a-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="9113a-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="9113a-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="9113a-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="9113a-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="9113a-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





