---
title: Propriedade IMsRdpClientAdvancedSettings5 RedirectDevices
description: Define ou recupera a configuração para o redirecionamento de dispositivo.
ms.assetid: bf989ca0-5c79-4a73-a32b-51ef97ca0dff
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RedirectDevices
- Propriedade RedirectDevices Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade RedirectDevices
- Propriedade RedirectDevices Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade RedirectDevices
- Propriedade RedirectDevices Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade RedirectDevices
- Propriedade RedirectDevices Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade RedirectDevices
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectDevices
- IMsRdpClientAdvancedSettings5.get_RedirectDevices
- IMsRdpClientAdvancedSettings5.put_RedirectDevices
- IMsRdpClientAdvancedSettings6.RedirectDevices
- IMsRdpClientAdvancedSettings6.get_RedirectDevices
- IMsRdpClientAdvancedSettings6.put_RedirectDevices
- IMsRdpClientAdvancedSettings7.RedirectDevices
- IMsRdpClientAdvancedSettings7.get_RedirectDevices
- IMsRdpClientAdvancedSettings7.put_RedirectDevices
- IMsRdpClientAdvancedSettings8.RedirectDevices
- IMsRdpClientAdvancedSettings8.get_RedirectDevices
- IMsRdpClientAdvancedSettings8.put_RedirectDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab1eec96b5d4fde20add891cc742c76c14ebe7ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755161"
---
# <a name="imsrdpclientadvancedsettings5redirectdevices-property"></a><span data-ttu-id="71a2f-112">Propriedade IMsRdpClientAdvancedSettings5:: RedirectDevices</span><span class="sxs-lookup"><span data-stu-id="71a2f-112">IMsRdpClientAdvancedSettings5::RedirectDevices property</span></span>

<span data-ttu-id="71a2f-113">Define ou recupera a configuração para o redirecionamento de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71a2f-113">Sets or retrieves the configuration for device redirection.</span></span>

<span data-ttu-id="71a2f-114">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="71a2f-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="71a2f-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="71a2f-115">Syntax</span></span>


```C++
HRESULT put_RedirectDevices(
  [in]  VARIANT_BOOL fRedirectPnPDevices
);

HRESULT get_RedirectDevices(
  [out] VARIANT_BOOL *pfRedirectPnPDevices
);
```



## <a name="property-value"></a><span data-ttu-id="71a2f-116">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="71a2f-116">Property value</span></span>

<span data-ttu-id="71a2f-117">Define o modo de redirecionamento de dispositivo como **verdadeiro** ou **falso**.</span><span class="sxs-lookup"><span data-stu-id="71a2f-117">Sets the device redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="71a2f-118">Se definido como **true**, o modo de redirecionamento de dispositivo será habilitado.</span><span class="sxs-lookup"><span data-stu-id="71a2f-118">If set to **TRUE**, device redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="71a2f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71a2f-119">Requirements</span></span>



| <span data-ttu-id="71a2f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="71a2f-120">Requirement</span></span> | <span data-ttu-id="71a2f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="71a2f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71a2f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71a2f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="71a2f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71a2f-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="71a2f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71a2f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="71a2f-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71a2f-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="71a2f-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="71a2f-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="71a2f-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71a2f-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="71a2f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="71a2f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71a2f-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71a2f-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="71a2f-130">IID</span><span class="sxs-lookup"><span data-stu-id="71a2f-130">IID</span></span><br/>                      | <span data-ttu-id="71a2f-131">IID \_ IMsRdpClientAdvancedSettings5 é definido como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="71a2f-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71a2f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="71a2f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71a2f-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="71a2f-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="71a2f-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="71a2f-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="71a2f-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="71a2f-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="71a2f-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="71a2f-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





