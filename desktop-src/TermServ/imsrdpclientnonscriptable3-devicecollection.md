---
title: Propriedade devicecollection IMsRdpClientNonScriptable3
description: Recupera a coleção de objetos de dispositivo Plug and Play (PnP) a serem redirecionados.
ms.assetid: dd5fe4c7-58bf-4e7a-b066-59278419ea6f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade devicecollection
- Propriedade devicecollection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade devicecollection
- Propriedade devicecollection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade devicecollection
- Propriedade devicecollection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade devicecollection
- Propriedade devicecollection Serviços de Área de Trabalho Remota, objeto MsRdpClient5
- Serviços de Área de Trabalho Remota de objeto MsRdpClient5, Propriedade devicecollection
- Propriedade devicecollection Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Serviços de Área de Trabalho Remota de objeto MsRdpClient6, Propriedade devicecollection
- Propriedade devicecollection Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Serviços de Área de Trabalho Remota de objeto MsRdpClient7, Propriedade devicecollection
- Propriedade devicecollection Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Serviços de Área de Trabalho Remota de objeto MsRdpClient8, Propriedade devicecollection
- Propriedade devicecollection Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Serviços de Área de Trabalho Remota de objeto MsRdpClient9, Propriedade devicecollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DeviceCollection
- IMsRdpClientNonScriptable3.get_DeviceCollection
- IMsRdpClientNonScriptable4.DeviceCollection
- IMsRdpClientNonScriptable4.get_DeviceCollection
- IMsRdpClientNonScriptable5.DeviceCollection
- IMsRdpClientNonScriptable5.get_DeviceCollection
- MsRdpClient5.DeviceCollection
- MsRdpClient6.DeviceCollection
- MsRdpClient7.DeviceCollection
- MsRdpClient8.DeviceCollection
- MsRdpClient9.DeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a545d2f4aaae2af68c14dd6531a2c57cf73711dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369376"
---
# <a name="imsrdpclientnonscriptable3devicecollection-property"></a><span data-ttu-id="55d07-120">IMsRdpClientNonScriptable3: Propriedade eviceCollection de:D</span><span class="sxs-lookup"><span data-stu-id="55d07-120">IMsRdpClientNonScriptable3::DeviceCollection property</span></span>

<span data-ttu-id="55d07-121">Recupera a coleção de objetos de dispositivo Plug and Play (PnP) a serem redirecionados.</span><span class="sxs-lookup"><span data-stu-id="55d07-121">Retrieves the collection of Plug and Play (PnP) device objects to be redirected.</span></span>

<span data-ttu-id="55d07-122">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="55d07-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="55d07-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55d07-123">Syntax</span></span>


```C++
HRESULT get_DeviceCollection(
  [out] IMSRdpDeviceCollection **ppDeviceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="55d07-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="55d07-124">Property value</span></span>

<span data-ttu-id="55d07-125">Recupera a coleção de objetos de dispositivo PnP do tipo [**IMSRdpDevice**](imsrdpdevice.md).</span><span class="sxs-lookup"><span data-stu-id="55d07-125">Retrieves the collection of PnP device objects of type [**IMSRdpDevice**](imsrdpdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55d07-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55d07-126">Requirements</span></span>



| <span data-ttu-id="55d07-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="55d07-127">Requirement</span></span> | <span data-ttu-id="55d07-128">Valor</span><span class="sxs-lookup"><span data-stu-id="55d07-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d07-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55d07-129">Minimum supported client</span></span><br/> | <span data-ttu-id="55d07-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55d07-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="55d07-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55d07-131">Minimum supported server</span></span><br/> | <span data-ttu-id="55d07-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55d07-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="55d07-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="55d07-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="55d07-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55d07-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="55d07-135">DLL</span><span class="sxs-lookup"><span data-stu-id="55d07-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55d07-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55d07-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="55d07-137">IID</span><span class="sxs-lookup"><span data-stu-id="55d07-137">IID</span></span><br/>                      | <span data-ttu-id="55d07-138">IID \_ IMsRdpClientNonScriptable3 é definido como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="55d07-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55d07-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="55d07-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55d07-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="55d07-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="55d07-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="55d07-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="55d07-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="55d07-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





