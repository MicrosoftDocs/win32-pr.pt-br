---
title: Propriedade IMsRdpClientAdvancedSettings6 RelativeMouseMode
description: Especifica se o mouse deve usar o modo relativo.
ms.assetid: 29ae9575-ce60-4999-9601-18413ae739e6
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RelativeMouseMode
- Propriedade RelativeMouseMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade RelativeMouseMode
- Propriedade RelativeMouseMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade RelativeMouseMode
- Propriedade RelativeMouseMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade RelativeMouseMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.RelativeMouseMode
- IMsRdpClientAdvancedSettings6.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings6.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.RelativeMouseMode
- IMsRdpClientAdvancedSettings7.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.RelativeMouseMode
- IMsRdpClientAdvancedSettings8.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.put_RelativeMouseMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31c575acefbfef54dc4c858f465f0cdde2ce8bc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757190"
---
# <a name="imsrdpclientadvancedsettings6relativemousemode-property"></a><span data-ttu-id="1fd7c-110">Propriedade IMsRdpClientAdvancedSettings6:: RelativeMouseMode</span><span class="sxs-lookup"><span data-stu-id="1fd7c-110">IMsRdpClientAdvancedSettings6::RelativeMouseMode property</span></span>

<span data-ttu-id="1fd7c-111">Especifica se o mouse deve usar o modo relativo.</span><span class="sxs-lookup"><span data-stu-id="1fd7c-111">Specifies whether the mouse should use relative mode.</span></span> <span data-ttu-id="1fd7c-112">Contém **Variant \_ true** se o mouse estiver no modo relativo ou **Variant \_ false** se o mouse estiver no modo absoluto.</span><span class="sxs-lookup"><span data-stu-id="1fd7c-112">Contains **VARIANT\_TRUE** if the mouse is in relative mode or **VARIANT\_FALSE** if the mouse is in absolute mode.</span></span>

<span data-ttu-id="1fd7c-113">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1fd7c-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fd7c-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fd7c-114">Syntax</span></span>


```C++
HRESULT put_RelativeMouseMode(
  [in]          VARIANT_BOOL fRelativeMouseMode
);

HRESULT get_RelativeMouseMode(
  [out, retval] VARIANT_BOOL *pfRelativeMouseMode
);
```



## <a name="property-value"></a><span data-ttu-id="1fd7c-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1fd7c-115">Property value</span></span>

<span data-ttu-id="1fd7c-116">Contém o novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="1fd7c-116">Contains the new property value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fd7c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fd7c-117">Remarks</span></span>

<span data-ttu-id="1fd7c-118">O modo de mouse indica como o controle ActiveX calcula as coordenadas do mouse que ele envia para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="1fd7c-118">The mouse mode indicates how the ActiveX control calculates the mouse coordinates that it sends to the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="1fd7c-119">Quando o mouse está no modo relativo, o controle ActiveX calcula as coordenadas do mouse em relação à última posição do mouse.</span><span class="sxs-lookup"><span data-stu-id="1fd7c-119">When the mouse is in relative mode, the ActiveX control calculates mouse coordinates relative to the mouse's last position.</span></span> <span data-ttu-id="1fd7c-120">Quando o mouse estiver no modo absoluto, o controle ActiveX calculará as coordenadas do mouse relativas à área de trabalho do servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="1fd7c-120">When the mouse is in absolute mode, the ActiveX control calculates mouse coordinates relative to the desktop of the RD Session Host server.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fd7c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fd7c-121">Requirements</span></span>



| <span data-ttu-id="1fd7c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fd7c-122">Requirement</span></span> | <span data-ttu-id="1fd7c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1fd7c-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fd7c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fd7c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1fd7c-125">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="1fd7c-125">Windows Vista with SP1</span></span><br/>                                                                |
| <span data-ttu-id="1fd7c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fd7c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1fd7c-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fd7c-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="1fd7c-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1fd7c-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="1fd7c-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fd7c-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1fd7c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1fd7c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fd7c-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fd7c-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1fd7c-132">IID</span><span class="sxs-lookup"><span data-stu-id="1fd7c-132">IID</span></span><br/>                      | <span data-ttu-id="1fd7c-133">IID \_ IMsRdpClientAdvancedSettings6 é definido como 222c4b5d-45D9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="1fd7c-133">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1fd7c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fd7c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fd7c-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1fd7c-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1fd7c-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1fd7c-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1fd7c-137">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1fd7c-137">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





