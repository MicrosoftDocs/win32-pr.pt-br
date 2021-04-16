---
title: Propriedade IMsRdpClientAdvancedSettings6 HotKeyFocusReleaseRight
description: Especifica o código de chave virtual a ser adicionado a CTRL + ALT para determinar a substituição de tecla de atalho para Ctrl + Alt + seta direita.
ms.assetid: 9AEEB712-E4C4-435E-A847-40C2B3A41C15
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade HotKeyFocusReleaseRight
- Propriedade HotKeyFocusReleaseRight Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade HotKeyFocusReleaseRight
- Propriedade HotKeyFocusReleaseRight Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade HotKeyFocusReleaseRight
- Propriedade HotKeyFocusReleaseRight Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade HotKeyFocusReleaseRight
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseRight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ce11df170b8b0a0a9a3f58a625955cecb41973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779275"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseright-property"></a><span data-ttu-id="25dcb-110">Propriedade IMsRdpClientAdvancedSettings6:: HotKeyFocusReleaseRight</span><span class="sxs-lookup"><span data-stu-id="25dcb-110">IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseRight property</span></span>

<span data-ttu-id="25dcb-111">Especifica o código de chave virtual a ser adicionado a CTRL + ALT para determinar a substituição de tecla de atalho para Ctrl + Alt + seta direita.</span><span class="sxs-lookup"><span data-stu-id="25dcb-111">Specifies the virtual-key code to add to Ctrl+Alt to determine the hotkey replacement for Ctrl+Alt+Right Arrow.</span></span>

<span data-ttu-id="25dcb-112">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="25dcb-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="25dcb-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25dcb-113">Syntax</span></span>


```C++
HRESULT put_HotKeyFocusReleaseRight(
  [in]  LONG hotKeyFocusReleaseRight
);

HRESULT get_HotKeyFocusReleaseRight(
  [out] LONG *hotKeyFocusReleaseRight
);
```



## <a name="property-value"></a><span data-ttu-id="25dcb-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="25dcb-114">Property value</span></span>

<span data-ttu-id="25dcb-115">O novo código de chave virtual.</span><span class="sxs-lookup"><span data-stu-id="25dcb-115">The new virtual-key code.</span></span>

## <a name="remarks"></a><span data-ttu-id="25dcb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="25dcb-116">Remarks</span></span>

<span data-ttu-id="25dcb-117">Essa propriedade só tem suporte nos clientes Conexão de Área de Trabalho Remota 6,1 e 7,0.</span><span class="sxs-lookup"><span data-stu-id="25dcb-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="25dcb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25dcb-118">Requirements</span></span>



| <span data-ttu-id="25dcb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="25dcb-119">Requirement</span></span> | <span data-ttu-id="25dcb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="25dcb-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25dcb-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25dcb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="25dcb-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25dcb-122">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="25dcb-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25dcb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="25dcb-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25dcb-124">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="25dcb-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="25dcb-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="25dcb-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25dcb-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="25dcb-127">DLL</span><span class="sxs-lookup"><span data-stu-id="25dcb-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25dcb-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25dcb-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="25dcb-129">IID</span><span class="sxs-lookup"><span data-stu-id="25dcb-129">IID</span></span><br/>                      | <span data-ttu-id="25dcb-130">IID \_ IMsRdpClientAdvancedSettings6 é definido como 222c4b5d-45D9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="25dcb-130">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25dcb-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="25dcb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25dcb-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="25dcb-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="25dcb-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="25dcb-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="25dcb-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="25dcb-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





