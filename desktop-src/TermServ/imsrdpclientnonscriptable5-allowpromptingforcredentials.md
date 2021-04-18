---
title: Propriedade IMsRdpClientNonScriptable5 AllowPromptingForCredentials
description: Especifica se o controle ActiveX Área de Trabalho Remota pode solicitar credenciais ao usuário.
ms.assetid: 9a780886-39ee-4d3b-9a54-fa209708d9f8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AllowPromptingForCredentials
- Propriedade AllowPromptingForCredentials Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade AllowPromptingForCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.get_AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.put_AllowPromptingForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c326a83a46b41d3578c958e24fd901beb7c7b321
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759942"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a><span data-ttu-id="50551-106">Propriedade IMsRdpClientNonScriptable5:: AllowPromptingForCredentials</span><span class="sxs-lookup"><span data-stu-id="50551-106">IMsRdpClientNonScriptable5::AllowPromptingForCredentials property</span></span>

<span data-ttu-id="50551-107">Especifica se o controle ActiveX Área de Trabalho Remota pode solicitar credenciais ao usuário.</span><span class="sxs-lookup"><span data-stu-id="50551-107">Specifies whether the Remote Desktop ActiveX control can prompt the user for credentials.</span></span> <span data-ttu-id="50551-108">Se essa propriedade contiver a **variante \_ true**, as credenciais do usuário poderão ser solicitadas.</span><span class="sxs-lookup"><span data-stu-id="50551-108">If this property contains **VARIANT\_TRUE**, the user can be prompted for credentials.</span></span> <span data-ttu-id="50551-109">Se essa propriedade contiver a **variante \_ false**, o usuário não poderá ser solicitado a fornecer credenciais.</span><span class="sxs-lookup"><span data-stu-id="50551-109">If this property contains **VARIANT\_FALSE**, the user cannot be prompted for credentials.</span></span>

<span data-ttu-id="50551-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="50551-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="50551-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50551-111">Syntax</span></span>


```C++
HRESULT put_AllowPromptingForCredentials(
  [in]          VARIANT_BOOL fAllow
);

HRESULT get_AllowPromptingForCredentials(
  [out, retval] VARIANT_BOOL *pfAllow
);
```



## <a name="property-value"></a><span data-ttu-id="50551-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="50551-112">Property value</span></span>

<span data-ttu-id="50551-113">Especifica o novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="50551-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="50551-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50551-114">Requirements</span></span>



| <span data-ttu-id="50551-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="50551-115">Requirement</span></span> | <span data-ttu-id="50551-116">Valor</span><span class="sxs-lookup"><span data-stu-id="50551-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="50551-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50551-117">Minimum supported client</span></span><br/> | <span data-ttu-id="50551-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="50551-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="50551-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50551-119">Minimum supported server</span></span><br/> | <span data-ttu-id="50551-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50551-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="50551-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="50551-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="50551-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50551-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="50551-123">DLL</span><span class="sxs-lookup"><span data-stu-id="50551-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50551-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50551-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="50551-125">IID</span><span class="sxs-lookup"><span data-stu-id="50551-125">IID</span></span><br/>                      | <span data-ttu-id="50551-126">IID \_ IMsRdpClientNonScriptable5 é definido como 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="50551-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50551-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="50551-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50551-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="50551-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





