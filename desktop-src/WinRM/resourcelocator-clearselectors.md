---
title: Método ResourceLocator. ClearSelectors (WSManDisp. h)
description: Remove todos os seletores de um objeto ResourceLocator.
ms.assetid: 759880e6-5026-45de-b7e1-a4f5a16c32a0
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método ClearSelectors
- Método ClearSelectors Gerenciamento Remoto do Windows, objeto ResourceLocator
- Objeto ResourceLocator Gerenciamento Remoto do Windows, método ClearSelectors
topic_type:
- apiref
api_name:
- ResourceLocator.ClearSelectors
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5dbf1322a5e0c36a1383581e2822fbd00a00e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086205"
---
# <a name="resourcelocatorclearselectors-method"></a><span data-ttu-id="022d9-106">Método ResourceLocator. ClearSelectors</span><span class="sxs-lookup"><span data-stu-id="022d9-106">ResourceLocator.ClearSelectors method</span></span>

<span data-ttu-id="022d9-107">Remove todos os [*seletores*](windows-remote-management-glossary.md) de um objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="022d9-107">Removes all of the [*selectors*](windows-remote-management-glossary.md) from a [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="022d9-108">Você pode fornecer um objeto [**ResourceLocator**](resourcelocator.md) em vez de especificar um URI de recurso em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="022d9-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="022d9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="022d9-109">Syntax</span></span>


```VB
ResourceLocator.ClearSelectors()
```



## <a name="parameters"></a><span data-ttu-id="022d9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="022d9-110">Parameters</span></span>

<span data-ttu-id="022d9-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="022d9-111">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="022d9-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="022d9-112">Remarks</span></span>

<span data-ttu-id="022d9-113">**IWSManResourceLocator:: ClearSelectors** é o método C++ correspondente.</span><span class="sxs-lookup"><span data-stu-id="022d9-113">**IWSManResourceLocator::ClearSelectors** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="022d9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="022d9-114">Requirements</span></span>



| <span data-ttu-id="022d9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="022d9-115">Requirement</span></span> | <span data-ttu-id="022d9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="022d9-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="022d9-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="022d9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="022d9-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="022d9-118">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="022d9-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="022d9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="022d9-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="022d9-120">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="022d9-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="022d9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="022d9-122"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="022d9-122"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="022d9-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="022d9-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="022d9-124"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="022d9-124"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="022d9-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="022d9-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="022d9-126"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="022d9-126"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="022d9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="022d9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="022d9-128"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="022d9-128"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="022d9-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="022d9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="022d9-130">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="022d9-130">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





