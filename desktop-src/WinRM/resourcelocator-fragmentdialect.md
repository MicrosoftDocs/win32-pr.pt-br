---
title: Propriedade ResourceLocator. FragmentDialect (WSManDisp. h)
description: Obtém ou define o dialeto de idioma para um dialeto de fragmento de recurso quando ResourceLocator é usado em operações de objeto de sessão, como Session. Get, Session. Put ou Session. Enumerate.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows da propriedade FragmentDialect
- Propriedade FragmentDialect Gerenciamento Remoto do Windows, objeto ResourceLocator
- Objeto ResourceLocator Gerenciamento Remoto do Windows, Propriedade FragmentDialect
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentDialect
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1fe42c2bbe15c75d5f38ea47119f9649e678931
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455835"
---
# <a name="resourcelocatorfragmentdialect-property"></a><span data-ttu-id="94583-106">Propriedade ResourceLocator. FragmentDialect</span><span class="sxs-lookup"><span data-stu-id="94583-106">ResourceLocator.FragmentDialect property</span></span>

<span data-ttu-id="94583-107">Obtém ou define o dialeto de idioma para um *dialeto* de [*fragmento*](windows-remote-management-glossary.md) de [*recurso*](windows-remote-management-glossary.md) quando [**ResourceLocator**](resourcelocator.md) é usado em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="94583-107">Gets or sets the language dialect for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) *dialect* when [**ResourceLocator**](resourcelocator.md) is used in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="94583-108">Um fragmento representa uma propriedade ou parte de um recurso.</span><span class="sxs-lookup"><span data-stu-id="94583-108">A fragment represents one property or part of a resource.</span></span> <span data-ttu-id="94583-109">Você pode fornecer um objeto [**ResourceLocator**](resourcelocator.md) em vez de especificar um URI de recurso em operações de objeto de [**sessão**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="94583-109">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations.</span></span> <span data-ttu-id="94583-110">O dialeto indica qual linguagem XML descreve o fragmento para o serviço que implementa o [protocolo WS-Management](ws-management-protocol.md) e recebe a solicitação.</span><span class="sxs-lookup"><span data-stu-id="94583-110">The dialect indicates what XML language describes the fragment to the service that implements the [WS-Management Protocol](ws-management-protocol.md) and receives the request.</span></span>

<span data-ttu-id="94583-111">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="94583-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="94583-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="94583-112">Syntax</span></span>


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a><span data-ttu-id="94583-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="94583-113">Property value</span></span>

<span data-ttu-id="94583-114">Uma cadeia de caracteres XML que identifica o idioma usado na propriedade [**FragmentPath**](resourcelocator-fragmentpath.md) .</span><span class="sxs-lookup"><span data-stu-id="94583-114">An XML string that identifies the language used in the [**FragmentPath**](resourcelocator-fragmentpath.md) property.</span></span> <span data-ttu-id="94583-115">A cadeia de caracteres de dialeto usa como padrão a especificação XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="94583-115">The dialect string defaults to the XPath 1.0 specification.</span></span> <span data-ttu-id="94583-116">Para obter mais informações, confira [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="94583-116">For more information, see [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span></span>

## <a name="remarks"></a><span data-ttu-id="94583-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="94583-117">Remarks</span></span>

<span data-ttu-id="94583-118">[**IWSManResourceLocator:: FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) é a propriedade C++ correspondente.</span><span class="sxs-lookup"><span data-stu-id="94583-118">[**IWSManResourceLocator::FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) is the corresponding C++ property.</span></span>

## <a name="requirements"></a><span data-ttu-id="94583-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94583-119">Requirements</span></span>



| <span data-ttu-id="94583-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="94583-120">Requirement</span></span> | <span data-ttu-id="94583-121">Valor</span><span class="sxs-lookup"><span data-stu-id="94583-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="94583-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94583-122">Minimum supported client</span></span><br/> | <span data-ttu-id="94583-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94583-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="94583-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94583-124">Minimum supported server</span></span><br/> | <span data-ttu-id="94583-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94583-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="94583-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94583-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="94583-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="94583-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="94583-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="94583-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="94583-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="94583-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="94583-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94583-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="94583-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="94583-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="94583-132">DLL</span><span class="sxs-lookup"><span data-stu-id="94583-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94583-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94583-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="94583-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="94583-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94583-135">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="94583-135">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





