---
title: Propriedade IMsRdpClientAdvancedSettings7 EnableSuperPan
description: Especifica ou recupera um valor booliano que indica se SuperPan está habilitado ou desabilitado.
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade EnableSuperPan
- Propriedade EnableSuperPan Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade EnableSuperPan
- Propriedade EnableSuperPan Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade EnableSuperPan
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.EnableSuperPan
- IMsRdpClientAdvancedSettings7.get_EnableSuperPan
- IMsRdpClientAdvancedSettings7.put_EnableSuperPan
- IMsRdpClientAdvancedSettings8.EnableSuperPan
- IMsRdpClientAdvancedSettings8.get_EnableSuperPan
- IMsRdpClientAdvancedSettings8.put_EnableSuperPan
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21ac0664b99dc0533d3e26840445ef22c8c08385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644808"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a><span data-ttu-id="63aab-108">Propriedade IMsRdpClientAdvancedSettings7:: EnableSuperPan</span><span class="sxs-lookup"><span data-stu-id="63aab-108">IMsRdpClientAdvancedSettings7::EnableSuperPan property</span></span>

<span data-ttu-id="63aab-109">Especifica ou recupera um valor booliano que indica se SuperPan está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="63aab-109">Specifies or retrieves a Boolean value that indicates whether SuperPan is enabled or disabled.</span></span> <span data-ttu-id="63aab-110">SuperPan é um recurso que permite que um usuário navegue facilmente por uma área de trabalho remota no modo de tela inteira, quando as dimensões da área de trabalho remota são maiores do que as dimensões da janela do cliente atual.</span><span class="sxs-lookup"><span data-stu-id="63aab-110">SuperPan is a feature that allows a user to easily navigate a remote desktop in full-screen mode, when the dimensions of the remote desktop are larger than the dimensions of the current client window.</span></span> <span data-ttu-id="63aab-111">Em vez de usar barras de rolagem para navegar na área de trabalho, o usuário pode apontar para a borda da janela e a área de trabalho remota será rolada automaticamente nessa direção.</span><span class="sxs-lookup"><span data-stu-id="63aab-111">Instead of using scroll bars to navigate the desktop, the user can point to the window border, and the remote desktop will scroll automatically in that direction.</span></span> <span data-ttu-id="63aab-112">SuperPan não dá suporte a mais de um monitor.</span><span class="sxs-lookup"><span data-stu-id="63aab-112">SuperPan does not support more than one monitor.</span></span>

<span data-ttu-id="63aab-113">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="63aab-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="63aab-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63aab-114">Syntax</span></span>


```C++
HRESULT put_EnableSuperPan(
  [in]          VARIANT_BOOL fEnableSuperPan
);

HRESULT get_EnableSuperPan(
  [out, retval] VARIANT_BOOL *pfEnableSuperPan
);
```



## <a name="property-value"></a><span data-ttu-id="63aab-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="63aab-115">Property value</span></span>

<span data-ttu-id="63aab-116">Um **valor \_ bool de variante** que especifica se SuperPan está habilitado.</span><span class="sxs-lookup"><span data-stu-id="63aab-116">A **VARIANT\_BOOL** value that specifies whether SuperPan is enabled.</span></span> <span data-ttu-id="63aab-117">Um valor de **Variant \_ true** especifica que SuperPan está habilitado.</span><span class="sxs-lookup"><span data-stu-id="63aab-117">A value of **VARIANT\_TRUE** specifies that SuperPan is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="63aab-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63aab-118">Requirements</span></span>



| <span data-ttu-id="63aab-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="63aab-119">Requirement</span></span> | <span data-ttu-id="63aab-120">Valor</span><span class="sxs-lookup"><span data-stu-id="63aab-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63aab-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63aab-121">Minimum supported client</span></span><br/> | <span data-ttu-id="63aab-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="63aab-122">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="63aab-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63aab-123">Minimum supported server</span></span><br/> | <span data-ttu-id="63aab-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="63aab-124">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="63aab-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="63aab-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="63aab-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63aab-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="63aab-127">DLL</span><span class="sxs-lookup"><span data-stu-id="63aab-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63aab-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63aab-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="63aab-129">IID</span><span class="sxs-lookup"><span data-stu-id="63aab-129">IID</span></span><br/>                      | <span data-ttu-id="63aab-130">IID \_ IMsRdpClientAdvancedSettings7 é definido como 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="63aab-130">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63aab-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="63aab-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63aab-132">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="63aab-132">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="63aab-133">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="63aab-133">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





