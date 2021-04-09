---
title: Propriedade ResourceLocator. FragmentPath (WSManDisp. h)
description: Obtém ou define o caminho para um fragmento de recurso ou propriedade quando ResourceLocator é usado em operações de objeto de sessão, como Session. Get, Session. Put ou Session. Enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows da propriedade FragmentPath
- Propriedade FragmentPath Gerenciamento Remoto do Windows, objeto ResourceLocator
- Objeto ResourceLocator Gerenciamento Remoto do Windows, Propriedade FragmentPath
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentPath
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e15fba102f9a7c8a2581271c575857b49bc5df1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009407"
---
# <a name="resourcelocatorfragmentpath-property"></a><span data-ttu-id="2317b-106">Propriedade ResourceLocator. FragmentPath</span><span class="sxs-lookup"><span data-stu-id="2317b-106">ResourceLocator.FragmentPath property</span></span>

<span data-ttu-id="2317b-107">Obtém ou define o caminho para um [](windows-remote-management-glossary.md) [*fragmento*](windows-remote-management-glossary.md) de recurso ou propriedade quando [**ResourceLocator**](resourcelocator.md) é usado em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="2317b-107">Gets or sets the path for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) or property when [**ResourceLocator**](resourcelocator.md) is used in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="2317b-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2317b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2317b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2317b-109">Syntax</span></span>


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a><span data-ttu-id="2317b-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2317b-110">Property value</span></span>

<span data-ttu-id="2317b-111">Cadeia de caracteres que identifica o fragmento ou a propriedade do recurso.</span><span class="sxs-lookup"><span data-stu-id="2317b-111">String that identifies the fragment or property of the resource.</span></span> <span data-ttu-id="2317b-112">Por exemplo, se o recurso for uma unidade de disco e a propriedade solicitada for fabricante, a cadeia de caracteres poderá conter `Diskdrive/Manufacturer` .</span><span class="sxs-lookup"><span data-stu-id="2317b-112">For example, if the resource is a disk drive and the requested property is Manufacturer, the string may contain `Diskdrive/Manufacturer`.</span></span> <span data-ttu-id="2317b-113">O texto do fragmento diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2317b-113">The fragment text is case-sensitive.</span></span> <span data-ttu-id="2317b-114">Nesse caso, você não pode usar `diskdrive/manufacturer` .</span><span class="sxs-lookup"><span data-stu-id="2317b-114">In this case, you cannot use `diskdrive/manufacturer`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2317b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2317b-115">Remarks</span></span>

<span data-ttu-id="2317b-116">**IWSManResourceLocator:: FragmentPath** é a propriedade C++ correspondente.</span><span class="sxs-lookup"><span data-stu-id="2317b-116">**IWSManResourceLocator::FragmentPath** is the corresponding C++ property.</span></span>

<span data-ttu-id="2317b-117">Você pode especificar um elemento de uma propriedade de matriz fornecendo o índice de matriz, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="2317b-117">You can specify one element of an array property by supplying the array index as shown in the following example.</span></span> <span data-ttu-id="2317b-118">Lembre-se de que a indexação de matriz começa com 1 em vez de 0.</span><span class="sxs-lookup"><span data-stu-id="2317b-118">Be aware that array indexing starts with 1 rather than 0.</span></span>


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



<span data-ttu-id="2317b-119">Para obter a matriz inteira, especifique o nome da propriedade de matriz, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="2317b-119">To get the whole array, specify the array property name as shown in the following example.</span></span>


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



## <a name="requirements"></a><span data-ttu-id="2317b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2317b-120">Requirements</span></span>



| <span data-ttu-id="2317b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2317b-121">Requirement</span></span> | <span data-ttu-id="2317b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2317b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2317b-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2317b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2317b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2317b-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2317b-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2317b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2317b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2317b-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2317b-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2317b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2317b-128"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2317b-128"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2317b-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="2317b-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2317b-130"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2317b-130"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2317b-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2317b-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="2317b-132"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2317b-132"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2317b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2317b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2317b-134"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2317b-134"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2317b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="2317b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2317b-136">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="2317b-136">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





