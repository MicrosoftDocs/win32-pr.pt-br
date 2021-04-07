---
title: Propriedade IMsRdpClientNonScriptable5 UseMultimon
description: Especifica se o controle ActiveX Área de Trabalho Remota deve usar vários monitores.
ms.assetid: 7832E025-80F6-4B4B-9829-C2D2EF2D8C37
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade UseMultimon
- Propriedade UseMultimon Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade UseMultimon
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.UseMultimon
- IMsRdpClientNonScriptable5.get_UseMultimon
- IMsRdpClientNonScriptable5.put_UseMultimon
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 941a2991ef5591176cd2508bbb6a097fecabebf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918737"
---
# <a name="imsrdpclientnonscriptable5usemultimon-property"></a><span data-ttu-id="4c250-106">Propriedade IMsRdpClientNonScriptable5:: UseMultimon</span><span class="sxs-lookup"><span data-stu-id="4c250-106">IMsRdpClientNonScriptable5::UseMultimon property</span></span>

<span data-ttu-id="4c250-107">Especifica se o controle ActiveX Área de Trabalho Remota deve usar vários monitores.</span><span class="sxs-lookup"><span data-stu-id="4c250-107">Specifies whether the Remote Desktop ActiveX control should use multiple monitors.</span></span> <span data-ttu-id="4c250-108">Se essa propriedade contiver **Variant \_ true**, o controle usará vários monitores.</span><span class="sxs-lookup"><span data-stu-id="4c250-108">If this property contains **VARIANT\_TRUE**, the control will use multiple monitors.</span></span> <span data-ttu-id="4c250-109">Se essa propriedade contiver a **variante \_ false**, o controle não usará vários monitores.</span><span class="sxs-lookup"><span data-stu-id="4c250-109">If this property contains **VARIANT\_FALSE**, the control will not use multiple monitors.</span></span>

<span data-ttu-id="4c250-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4c250-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c250-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c250-111">Syntax</span></span>


```C++
HRESULT put_UseMultimon(
  [in]          VARIANT_BOOL fUseMultimon
);

HRESULT get_UseMultimon(
  [out, retval] VARIANT_BOOL *pfUseMultimon
);
```



## <a name="property-value"></a><span data-ttu-id="4c250-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4c250-112">Property value</span></span>

<span data-ttu-id="4c250-113">Especifica o novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="4c250-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c250-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c250-114">Requirements</span></span>



| <span data-ttu-id="4c250-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c250-115">Requirement</span></span> | <span data-ttu-id="4c250-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4c250-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c250-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c250-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4c250-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c250-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4c250-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c250-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4c250-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4c250-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="4c250-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4c250-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="4c250-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c250-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="4c250-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4c250-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c250-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c250-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="4c250-125">IID</span><span class="sxs-lookup"><span data-stu-id="4c250-125">IID</span></span><br/>                      | <span data-ttu-id="4c250-126">IID \_ IMsRdpClientNonScriptable5 é definido como 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="4c250-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4c250-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c250-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c250-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="4c250-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





