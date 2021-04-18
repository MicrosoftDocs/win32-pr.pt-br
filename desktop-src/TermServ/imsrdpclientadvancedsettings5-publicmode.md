---
title: Propriedade IMsRdpClientAdvancedSettings5 Públicomode
description: Define ou recupera a configuração para o modo público. O modo público impede que o cliente Caching os dados do usuário para o sistema local.
ms.assetid: dff6121a-b69c-411f-832b-29f9609f4230
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade públicomode
- Propriedade publicmode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings5, Propriedade Publicmode
- Propriedade publicmode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings6, Propriedade Publicmode
- Propriedade publicmode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings7, Propriedade Publicmode
- Propriedade publicmode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings8, Propriedade Publicmode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.PublicMode
- IMsRdpClientAdvancedSettings5.get_PublicMode
- IMsRdpClientAdvancedSettings5.put_PublicMode
- IMsRdpClientAdvancedSettings6.PublicMode
- IMsRdpClientAdvancedSettings6.get_PublicMode
- IMsRdpClientAdvancedSettings6.put_PublicMode
- IMsRdpClientAdvancedSettings7.PublicMode
- IMsRdpClientAdvancedSettings7.get_PublicMode
- IMsRdpClientAdvancedSettings7.put_PublicMode
- IMsRdpClientAdvancedSettings8.PublicMode
- IMsRdpClientAdvancedSettings8.get_PublicMode
- IMsRdpClientAdvancedSettings8.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9173b7685e77984a28d65129c79c9d1a09cf1458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755162"
---
# <a name="imsrdpclientadvancedsettings5publicmode-property"></a><span data-ttu-id="ed7d4-113">IMsRdpClientAdvancedSettings5: Propriedade ublicMode de:P</span><span class="sxs-lookup"><span data-stu-id="ed7d4-113">IMsRdpClientAdvancedSettings5::PublicMode property</span></span>

<span data-ttu-id="ed7d4-114">Define ou recupera a configuração para o modo público.</span><span class="sxs-lookup"><span data-stu-id="ed7d4-114">Sets or retrieves the configuration for public mode.</span></span> <span data-ttu-id="ed7d4-115">O modo público impede que o cliente Caching os dados do usuário para o sistema local.</span><span class="sxs-lookup"><span data-stu-id="ed7d4-115">Public mode prevents the client from caching user data to the local system.</span></span>

<span data-ttu-id="ed7d4-116">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ed7d4-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed7d4-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed7d4-117">Syntax</span></span>


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a><span data-ttu-id="ed7d4-118">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ed7d4-118">Property value</span></span>

<span data-ttu-id="ed7d4-119">Define a configuração de modo público como **Variant \_ true** ou **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="ed7d4-119">Sets the public mode setting to **VARIANT\_TRUE** or **VARIANT\_FALSE**.</span></span> <span data-ttu-id="ed7d4-120">Se definido como **Variant \_ true**, a configuração de modo público será habilitada.</span><span class="sxs-lookup"><span data-stu-id="ed7d4-120">If set to **VARIANT\_TRUE**, the public mode setting is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed7d4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed7d4-121">Requirements</span></span>



| <span data-ttu-id="ed7d4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed7d4-122">Requirement</span></span> | <span data-ttu-id="ed7d4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ed7d4-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed7d4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed7d4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ed7d4-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed7d4-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="ed7d4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed7d4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ed7d4-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed7d4-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="ed7d4-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ed7d4-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="ed7d4-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed7d4-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ed7d4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ed7d4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed7d4-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed7d4-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ed7d4-132">IID</span><span class="sxs-lookup"><span data-stu-id="ed7d4-132">IID</span></span><br/>                      | <span data-ttu-id="ed7d4-133">IID \_ IMsRdpClientAdvancedSettings5 é definido como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="ed7d4-133">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed7d4-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed7d4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed7d4-135">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ed7d4-135">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ed7d4-136">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ed7d4-136">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ed7d4-137">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ed7d4-137">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ed7d4-138">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ed7d4-138">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





