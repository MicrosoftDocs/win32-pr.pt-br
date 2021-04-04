---
title: Método ResourceLocator. addseletor (WSManDisp. h)
description: Adiciona um seletor ao objeto ResourceLocator. O seletor especifica uma instância específica de um recurso.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- Método addselecter Gerenciamento Remoto do Windows
- Método addselecter Gerenciamento Remoto do Windows, objeto ResourceLocator
- Objeto ResourceLocator Gerenciamento Remoto do Windows, método addseletor
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 064108f535c9f46dc074d1b37754e626dc3f1d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918497"
---
# <a name="resourcelocatoraddselector-method"></a><span data-ttu-id="afc58-107">Método ResourceLocator. addseletor</span><span class="sxs-lookup"><span data-stu-id="afc58-107">ResourceLocator.AddSelector method</span></span>

<span data-ttu-id="afc58-108">Adiciona um [*seletor*](windows-remote-management-glossary.md) ao objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="afc58-108">Adds a [*selector*](windows-remote-management-glossary.md) to the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="afc58-109">O seletor especifica uma instância específica de um *recurso*.</span><span class="sxs-lookup"><span data-stu-id="afc58-109">The selector specifies a particular instance of a *resource*.</span></span> <span data-ttu-id="afc58-110">Você pode fornecer um objeto [**ResourceLocator**](resourcelocator.md) em vez de especificar um URI de recurso em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="afc58-110">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="afc58-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afc58-111">Syntax</span></span>


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a><span data-ttu-id="afc58-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="afc58-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc58-113">*resourceSelName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="afc58-113">*resourceSelName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc58-114">O nome do seletor.</span><span class="sxs-lookup"><span data-stu-id="afc58-114">The selector name.</span></span> <span data-ttu-id="afc58-115">Por exemplo, ao solicitar dados WMI, esse parâmetro é a propriedade de chave para uma classe WMI.</span><span class="sxs-lookup"><span data-stu-id="afc58-115">For example, when requesting WMI data, this parameter is the key property for a WMI class.</span></span>

</dd> <dt>

<span data-ttu-id="afc58-116">*selValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="afc58-116">*selValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc58-117">O valor do seletor.</span><span class="sxs-lookup"><span data-stu-id="afc58-117">The selector value.</span></span> <span data-ttu-id="afc58-118">Por exemplo, para dados WMI, esse parâmetro contém um valor para uma propriedade de chave que identifica uma instância específica.</span><span class="sxs-lookup"><span data-stu-id="afc58-118">For example, for WMI data, this parameter contains a value for a key property that identifies a specific instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afc58-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="afc58-119">Remarks</span></span>

<span data-ttu-id="afc58-120">**IWSManResourceLocator:: Addseletor** é o método C++ correspondente.</span><span class="sxs-lookup"><span data-stu-id="afc58-120">**IWSManResourceLocator::AddSelector** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc58-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afc58-121">Requirements</span></span>



| <span data-ttu-id="afc58-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="afc58-122">Requirement</span></span> | <span data-ttu-id="afc58-123">Valor</span><span class="sxs-lookup"><span data-stu-id="afc58-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="afc58-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afc58-124">Minimum supported client</span></span><br/> | <span data-ttu-id="afc58-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afc58-125">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="afc58-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afc58-126">Minimum supported server</span></span><br/> | <span data-ttu-id="afc58-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afc58-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="afc58-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="afc58-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="afc58-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="afc58-129"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="afc58-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="afc58-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="afc58-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="afc58-131"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="afc58-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="afc58-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="afc58-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="afc58-133"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="afc58-134">DLL</span><span class="sxs-lookup"><span data-stu-id="afc58-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afc58-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afc58-135"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="afc58-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="afc58-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc58-137">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="afc58-137">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





