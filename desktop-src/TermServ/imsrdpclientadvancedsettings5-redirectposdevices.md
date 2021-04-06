---
title: Propriedade IMsRdpClientAdvancedSettings5 RedirectPOSDevices
description: Define ou recupera a configuração para o redirecionamento de dispositivo de ponto de serviço.
ms.assetid: 2614048e-244d-4dea-96fb-bb8c563a29f9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RedirectPOSDevices
- Propriedade RedirectPOSDevices Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade RedirectPOSDevices
- Propriedade RedirectPOSDevices Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade RedirectPOSDevices
- Propriedade RedirectPOSDevices Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade RedirectPOSDevices
- Propriedade RedirectPOSDevices Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade RedirectPOSDevices
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.put_RedirectPOSDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5ceb0c1fb9751b137b5791ce9c8da1bd0cdbb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085871"
---
# <a name="imsrdpclientadvancedsettings5redirectposdevices-property"></a><span data-ttu-id="1d35f-112">Propriedade IMsRdpClientAdvancedSettings5:: RedirectPOSDevices</span><span class="sxs-lookup"><span data-stu-id="1d35f-112">IMsRdpClientAdvancedSettings5::RedirectPOSDevices property</span></span>

<span data-ttu-id="1d35f-113">Define ou recupera a configuração para o redirecionamento de dispositivo de ponto de serviço.</span><span class="sxs-lookup"><span data-stu-id="1d35f-113">Sets or retrieves the configuration for Point of Service device redirection.</span></span>

<span data-ttu-id="1d35f-114">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1d35f-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d35f-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d35f-115">Syntax</span></span>


```C++
HRESULT put_RedirectPOSDevices(
  [in]  VARIANT_BOOL fRedirectPOSDevices
);

HRESULT get_RedirectPOSDevices(
  [out] VARIANT_BOOL *pfRedirectPOSDevices
);
```



## <a name="property-value"></a><span data-ttu-id="1d35f-116">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1d35f-116">Property value</span></span>

<span data-ttu-id="1d35f-117">Define o modo de redirecionamento de dispositivo de ponto de serviço como **verdadeiro** ou **falso**.</span><span class="sxs-lookup"><span data-stu-id="1d35f-117">Sets Point of Service device redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="1d35f-118">Se definido como **true**, o modo de redirecionamento de dispositivo do ponto de serviço está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1d35f-118">If set to **TRUE**, Point of Service device redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d35f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d35f-119">Requirements</span></span>



| <span data-ttu-id="1d35f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d35f-120">Requirement</span></span> | <span data-ttu-id="1d35f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1d35f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d35f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d35f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1d35f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d35f-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="1d35f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d35f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1d35f-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d35f-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="1d35f-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1d35f-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="1d35f-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d35f-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1d35f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1d35f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d35f-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d35f-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1d35f-130">IID</span><span class="sxs-lookup"><span data-stu-id="1d35f-130">IID</span></span><br/>                      | <span data-ttu-id="1d35f-131">IID \_ IMsRdpClientAdvancedSettings5 é definido como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="1d35f-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d35f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d35f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d35f-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1d35f-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="1d35f-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1d35f-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1d35f-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1d35f-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1d35f-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="1d35f-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





