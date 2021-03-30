---
title: Propriedade ResourceLocator. ResourceURI (WSManDisp. h)
description: Obtém ou define o URI do recurso em um objeto ResourceLocator.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows da propriedade ResourceURI
- Propriedade ResourceURI Gerenciamento Remoto do Windows, objeto ResourceLocator
- Objeto ResourceLocator Gerenciamento Remoto do Windows, Propriedade ResourceURI
topic_type:
- apiref
api_name:
- ResourceLocator.ResourceURI
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f804835b5445c32f74094e8280a598785d1526
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455470"
---
# <a name="resourcelocatorresourceuri-property"></a><span data-ttu-id="72bc0-106">Propriedade ResourceLocator. ResourceURI</span><span class="sxs-lookup"><span data-stu-id="72bc0-106">ResourceLocator.ResourceURI property</span></span>

<span data-ttu-id="72bc0-107">Obtém ou define o [*URI do recurso*](windows-remote-management-glossary.md) em um objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="72bc0-107">Gets or sets the [*resource URI*](windows-remote-management-glossary.md) in a [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="72bc0-108">Você pode fornecer um objeto [**ResourceLocator**](resourcelocator.md) em vez de especificar um URI de recurso em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="72bc0-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="72bc0-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="72bc0-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="72bc0-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72bc0-110">Syntax</span></span>


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a><span data-ttu-id="72bc0-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="72bc0-111">Property value</span></span>

<span data-ttu-id="72bc0-112">Uma cadeia de caracteres que identifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="72bc0-112">A string that identifies the resource.</span></span> <span data-ttu-id="72bc0-113">Ao definir o URI de recurso para um objeto [**ResourceLocator**](resourcelocator.md) , o URI deve conter apenas o caminho.</span><span class="sxs-lookup"><span data-stu-id="72bc0-113">When setting the resource URI for a [**ResourceLocator**](resourcelocator.md) object, the URI must contain only the path.</span></span>

## <a name="remarks"></a><span data-ttu-id="72bc0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="72bc0-114">Remarks</span></span>

<span data-ttu-id="72bc0-115">Veja a seguir um exemplo de um caminho apropriado para [**ResourceURI**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).</span><span class="sxs-lookup"><span data-stu-id="72bc0-115">The following is an example of a proper path for [**ResourceURI**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).</span></span>

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

<span data-ttu-id="72bc0-116">O caminho a seguir não funciona porque ele contém uma chave para uma instância específica.</span><span class="sxs-lookup"><span data-stu-id="72bc0-116">The following path does not work because it contains a key for a specific instance.</span></span> <span data-ttu-id="72bc0-117">Use o método [**ResourceLocator. Addseletor**](resourcelocator-addselector.md) para especificar uma instância específica.</span><span class="sxs-lookup"><span data-stu-id="72bc0-117">Use the [**ResourceLocator.AddSelector**](resourcelocator-addselector.md) method to specify a particular instance.</span></span>

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

<span data-ttu-id="72bc0-118">**IWSManResourceLocator:: ResourceURI** é o método C++ correspondente.</span><span class="sxs-lookup"><span data-stu-id="72bc0-118">**IWSManResourceLocator::ResourceURI** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="72bc0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72bc0-119">Requirements</span></span>



| <span data-ttu-id="72bc0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="72bc0-120">Requirement</span></span> | <span data-ttu-id="72bc0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="72bc0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="72bc0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72bc0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="72bc0-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72bc0-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="72bc0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72bc0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="72bc0-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72bc0-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="72bc0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72bc0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="72bc0-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72bc0-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="72bc0-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="72bc0-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72bc0-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72bc0-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="72bc0-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72bc0-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="72bc0-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="72bc0-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="72bc0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="72bc0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72bc0-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72bc0-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="72bc0-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="72bc0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72bc0-135">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="72bc0-135">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





