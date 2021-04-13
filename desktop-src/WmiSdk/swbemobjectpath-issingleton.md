---
description: A Propriedade IsSingleton do objeto SWbemObjectPath é um valor booliano que indica se esse caminho representa uma instância singleton. Uma instância singleton é uma instância de uma classe que nunca pode ter mais de uma instância. Esta propriedade é somente para leitura.
ms.assetid: 0d0533be-89fe-4ab6-bafa-2da6195ff02c
ms.tgt_platform: multiple
title: Propriedade SWbemObjectPath. IsSingleton (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.IsSingleton
- ISWbemObjectPath.IsSingleton
- ISWbemObjectPath.get_IsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bd267c3d8ad36459a04b835cb2f130c3e98420a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171786"
---
# <a name="swbemobjectpathissingleton-property"></a><span data-ttu-id="3a85f-105">Propriedade SWbemObjectPath. IsSingleton</span><span class="sxs-lookup"><span data-stu-id="3a85f-105">SWbemObjectPath.IsSingleton property</span></span>

<span data-ttu-id="3a85f-106">A propriedade **IsSingleton** do objeto [**SWbemObjectPath**](swbemobjectpath.md) é um valor booliano que indica se esse caminho representa uma instância singleton.</span><span class="sxs-lookup"><span data-stu-id="3a85f-106">The **IsSingleton** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is a Boolean value that indicates if this path represents a singleton instance.</span></span> <span data-ttu-id="3a85f-107">Uma instância singleton é uma instância de uma classe que nunca pode ter mais de uma instância.</span><span class="sxs-lookup"><span data-stu-id="3a85f-107">A singleton instance is an instance of a class that can never have more than one instance.</span></span> <span data-ttu-id="3a85f-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3a85f-108">This property is read-only.</span></span>

<span data-ttu-id="3a85f-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3a85f-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3a85f-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3a85f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a85f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a85f-111">Syntax</span></span>


```VB
SWbemObjectPath.IsSingleton As Boolean
```



## <a name="property-value"></a><span data-ttu-id="3a85f-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3a85f-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="3a85f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a85f-113">Requirements</span></span>



| <span data-ttu-id="3a85f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a85f-114">Requirement</span></span> | <span data-ttu-id="3a85f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3a85f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a85f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a85f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3a85f-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a85f-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a85f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a85f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3a85f-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a85f-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a85f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a85f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a85f-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a85f-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a85f-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3a85f-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="3a85f-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3a85f-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3a85f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3a85f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a85f-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a85f-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3a85f-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="3a85f-126">CLSID</span></span><br/>                    | <span data-ttu-id="3a85f-127">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="3a85f-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="3a85f-128">IID</span><span class="sxs-lookup"><span data-stu-id="3a85f-128">IID</span></span><br/>                      | <span data-ttu-id="3a85f-129">ISWbemObjectPath de IID \_</span><span class="sxs-lookup"><span data-stu-id="3a85f-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




