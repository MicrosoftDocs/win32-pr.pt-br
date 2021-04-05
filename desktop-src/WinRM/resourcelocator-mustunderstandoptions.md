---
title: Propriedade ResourceLocator. MustUnderstandoptions (WSManDisp. h)
description: Obtém ou define o valor MustUnderstandoptions para o objeto ResourceLocator.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- Propriedade MustUnderstandoptions Gerenciamento Remoto do Windows
- Propriedade MustUnderstandoptions Gerenciamento Remoto do Windows, objeto ResourceLocator
- Objeto ResourceLocator Gerenciamento Remoto do Windows, Propriedade MustUnderstandoptions
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2945efd1a224c333f45956a29df779efc98e944f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919032"
---
# <a name="resourcelocatormustunderstandoptions-property"></a><span data-ttu-id="2a9cc-106">Propriedade ResourceLocator. MustUnderstandoptions</span><span class="sxs-lookup"><span data-stu-id="2a9cc-106">ResourceLocator.MustUnderstandOptions property</span></span>

<span data-ttu-id="2a9cc-107">Obtém ou define o valor **mustunderstandoptions** para o objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="2a9cc-107">Gets or sets the **MustUnderstandOptions** value for the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="2a9cc-108">Você pode fornecer um objeto [**ResourceLocator**](resourcelocator.md) em vez de especificar um URI de recurso em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="2a9cc-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="2a9cc-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2a9cc-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a9cc-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a9cc-110">Syntax</span></span>


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a><span data-ttu-id="2a9cc-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2a9cc-111">Property value</span></span>

<span data-ttu-id="2a9cc-112">Indica, quando **true**, que o serviço que implementa a [protocolo WS-Management](ws-management-protocol.md) deve retornar um erro se não for capaz de processar a opção.</span><span class="sxs-lookup"><span data-stu-id="2a9cc-112">Indicates, when **True**, that the service which implements the [WS-Management Protocol](ws-management-protocol.md) must return an error if it is not capable of processing the option.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a9cc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a9cc-113">Remarks</span></span>

<span data-ttu-id="2a9cc-114">**IWSManResourceLocator:: mustunderstandoptions** é a propriedade C++ correspondente.</span><span class="sxs-lookup"><span data-stu-id="2a9cc-114">**IWSManResourceLocator::MustUnderstandOptions** is the corresponding C++ property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a9cc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a9cc-115">Requirements</span></span>



| <span data-ttu-id="2a9cc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a9cc-116">Requirement</span></span> | <span data-ttu-id="2a9cc-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2a9cc-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a9cc-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a9cc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2a9cc-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a9cc-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2a9cc-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a9cc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2a9cc-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a9cc-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2a9cc-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a9cc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a9cc-123"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a9cc-123"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a9cc-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="2a9cc-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2a9cc-125"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2a9cc-125"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2a9cc-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2a9cc-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="2a9cc-127"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2a9cc-127"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2a9cc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2a9cc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a9cc-129"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a9cc-129"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a9cc-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a9cc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a9cc-131">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="2a9cc-131">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





