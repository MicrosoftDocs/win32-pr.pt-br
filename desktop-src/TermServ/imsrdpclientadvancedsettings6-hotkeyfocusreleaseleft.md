---
title: Propriedade IMsRdpClientAdvancedSettings6 HotKeyFocusReleaseLeft
description: Especifica o código de chave virtual a ser adicionado a CTRL + ALT para determinar a substituição de tecla de atalho para Ctrl + Alt + seta para a esquerda.
ms.assetid: 9F2942BD-9F5C-4E02-A330-42C30C6C8F87
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade HotKeyFocusReleaseLeft
- Propriedade HotKeyFocusReleaseLeft Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade HotKeyFocusReleaseLeft
- Propriedade HotKeyFocusReleaseLeft Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade HotKeyFocusReleaseLeft
- Propriedade HotKeyFocusReleaseLeft Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade HotKeyFocusReleaseLeft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseLeft
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e0e6d4e334edeffbf0ef025e59454e0f26c34c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644276"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseleft-property"></a><span data-ttu-id="919a0-110">Propriedade IMsRdpClientAdvancedSettings6:: HotKeyFocusReleaseLeft</span><span class="sxs-lookup"><span data-stu-id="919a0-110">IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseLeft property</span></span>

<span data-ttu-id="919a0-111">Especifica o código de chave virtual a ser adicionado a CTRL + ALT para determinar a substituição de tecla de atalho para Ctrl + Alt + seta para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="919a0-111">Specifies the virtual-key code to add to Ctrl+Alt to determine the hotkey replacement for Ctrl+Alt+Left Arrow.</span></span>

<span data-ttu-id="919a0-112">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="919a0-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="919a0-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="919a0-113">Syntax</span></span>


```C++
HRESULT put_HotKeyFocusReleaseLeft(
  [in]  LONG hotKeyFocusReleaseLeft
);

HRESULT get_HotKeyFocusReleaseLeft(
  [out] LONG *hotKeyFocusReleaseLeft
);
```



## <a name="property-value"></a><span data-ttu-id="919a0-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="919a0-114">Property value</span></span>

<span data-ttu-id="919a0-115">O novo código de chave virtual.</span><span class="sxs-lookup"><span data-stu-id="919a0-115">The new virtual-key code.</span></span>

## <a name="remarks"></a><span data-ttu-id="919a0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="919a0-116">Remarks</span></span>

<span data-ttu-id="919a0-117">Essa propriedade só tem suporte nos clientes Conexão de Área de Trabalho Remota 6,1 e 7,0.</span><span class="sxs-lookup"><span data-stu-id="919a0-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="919a0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="919a0-118">Requirements</span></span>



| <span data-ttu-id="919a0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="919a0-119">Requirement</span></span> | <span data-ttu-id="919a0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="919a0-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="919a0-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="919a0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="919a0-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="919a0-122">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="919a0-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="919a0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="919a0-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="919a0-124">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="919a0-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="919a0-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="919a0-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="919a0-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="919a0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="919a0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="919a0-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="919a0-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="919a0-129">IID</span><span class="sxs-lookup"><span data-stu-id="919a0-129">IID</span></span><br/>                      | <span data-ttu-id="919a0-130">IID \_ IMsRdpClientAdvancedSettings6 é definido como 222c4b5d-45D9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="919a0-130">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="919a0-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="919a0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="919a0-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="919a0-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="919a0-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="919a0-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="919a0-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="919a0-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





