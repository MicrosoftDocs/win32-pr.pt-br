---
title: Método ResourceLocator. Clearoptions (WSManDisp. h)
description: Remove todas as opções do objeto ResourceLocator.
ms.assetid: 1b4d7f15-c56f-4b0d-9614-8376012abca7
ms.tgt_platform: multiple
keywords:
- Método clearoptions Gerenciamento Remoto do Windows
- Método clearoptions Gerenciamento Remoto do Windows, objeto ResourceLocator
- Objeto ResourceLocator Gerenciamento Remoto do Windows, método Clearoptions
topic_type:
- apiref
api_name:
- ResourceLocator.ClearOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda4be766b65756a9bcf8de02a4417fd15a3e7f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824230"
---
# <a name="resourcelocatorclearoptions-method"></a><span data-ttu-id="12759-106">Método ResourceLocator. Clearoptions</span><span class="sxs-lookup"><span data-stu-id="12759-106">ResourceLocator.ClearOptions method</span></span>

<span data-ttu-id="12759-107">Remove todas [*as opções*](windows-remote-management-glossary.md) do objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="12759-107">Removes any [*options*](windows-remote-management-glossary.md) from the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="12759-108">Você pode fornecer um objeto [**ResourceLocator**](resourcelocator.md) em vez de especificar um URI de recurso em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="12759-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="12759-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12759-109">Syntax</span></span>


```VB
ResourceLocator.ClearOptions()
```



## <a name="parameters"></a><span data-ttu-id="12759-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12759-110">Parameters</span></span>

<span data-ttu-id="12759-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="12759-111">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="12759-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="12759-112">Remarks</span></span>

<span data-ttu-id="12759-113">**IWSManResourceLocator:: clearoptions** é o método C++ correspondente.</span><span class="sxs-lookup"><span data-stu-id="12759-113">**IWSManResourceLocator::ClearOptions** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="12759-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12759-114">Requirements</span></span>



| <span data-ttu-id="12759-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="12759-115">Requirement</span></span> | <span data-ttu-id="12759-116">Valor</span><span class="sxs-lookup"><span data-stu-id="12759-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="12759-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12759-117">Minimum supported client</span></span><br/> | <span data-ttu-id="12759-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12759-118">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="12759-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12759-119">Minimum supported server</span></span><br/> | <span data-ttu-id="12759-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12759-120">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="12759-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12759-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="12759-122"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="12759-122"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="12759-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="12759-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12759-124"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="12759-124"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="12759-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12759-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="12759-126"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="12759-126"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="12759-127">DLL</span><span class="sxs-lookup"><span data-stu-id="12759-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12759-128"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12759-128"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="12759-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="12759-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12759-130">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="12759-130">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





