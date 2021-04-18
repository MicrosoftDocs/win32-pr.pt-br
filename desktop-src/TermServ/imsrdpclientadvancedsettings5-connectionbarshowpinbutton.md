---
title: Propriedade IMsRdpClientAdvancedSettings5 ConnectionBarShowPinButton
description: Define ou recupera a configuração do botão PIN na barra de conexão.
ms.assetid: fbb2c19b-88a7-435b-86ef-4856e194b383
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ConnectionBarShowPinButton
- Propriedade ConnectionBarShowPinButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade ConnectionBarShowPinButton
- Propriedade ConnectionBarShowPinButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade ConnectionBarShowPinButton
- Propriedade ConnectionBarShowPinButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade ConnectionBarShowPinButton
- Propriedade ConnectionBarShowPinButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade ConnectionBarShowPinButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowPinButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a766bc01bc5bf773fa03e788c3089441e6c3f6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761936"
---
# <a name="imsrdpclientadvancedsettings5connectionbarshowpinbutton-property"></a><span data-ttu-id="2b116-112">Propriedade IMsRdpClientAdvancedSettings5:: ConnectionBarShowPinButton</span><span class="sxs-lookup"><span data-stu-id="2b116-112">IMsRdpClientAdvancedSettings5::ConnectionBarShowPinButton property</span></span>

<span data-ttu-id="2b116-113">Define ou recupera a configuração do botão PIN na barra de conexão.</span><span class="sxs-lookup"><span data-stu-id="2b116-113">Sets or retrieves the configuration for the pin button in the connection bar.</span></span>

<span data-ttu-id="2b116-114">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2b116-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b116-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b116-115">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowPinButton(
  [in]  VARIANT_BOOL fShowPin
);

HRESULT get_ConnectionBarShowPinButton(
  [out] VARIANT_BOOL *pfShowPin
);
```



## <a name="property-value"></a><span data-ttu-id="2b116-116">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2b116-116">Property value</span></span>

<span data-ttu-id="2b116-117">Um valor booliano de **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="2b116-117">A Boolean value of **TRUE** or **FALSE**.</span></span> <span data-ttu-id="2b116-118">Um valor **true** mostra o botão PIN na barra de conexão.</span><span class="sxs-lookup"><span data-stu-id="2b116-118">A value of **TRUE** shows the pin button in the connection bar.</span></span> <span data-ttu-id="2b116-119">Um valor de **false** oculta o botão de PIN na barra de conexão.</span><span class="sxs-lookup"><span data-stu-id="2b116-119">A value of **FALSE** hides the pin button in the connection bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b116-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b116-120">Requirements</span></span>



| <span data-ttu-id="2b116-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b116-121">Requirement</span></span> | <span data-ttu-id="2b116-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2b116-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b116-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b116-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2b116-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b116-124">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="2b116-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b116-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2b116-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b116-126">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="2b116-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2b116-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b116-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b116-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="2b116-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2b116-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b116-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b116-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="2b116-131">IID</span><span class="sxs-lookup"><span data-stu-id="2b116-131">IID</span></span><br/>                      | <span data-ttu-id="2b116-132">IID \_ IMsRdpClientAdvancedSettings5 é definido como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="2b116-132">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b116-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b116-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b116-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="2b116-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="2b116-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="2b116-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="2b116-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="2b116-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="2b116-137">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="2b116-137">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





