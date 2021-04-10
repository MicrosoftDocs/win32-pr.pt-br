---
description: A propriedade origin do objeto SWbemMethod retorna o nome da classe na qual esse método foi introduzido.
ms.assetid: da98393b-af95-47ad-b589-663063f65afb
ms.tgt_platform: multiple
title: Propriedade SWbemMethod. Origin (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.Origin
- ISWbemMethod.Origin
- ISWbemMethod.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c1b903a2c55bbd571a9cd1f36a51812a70c123cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165200"
---
# <a name="swbemmethodorigin-property"></a><span data-ttu-id="14900-103">Propriedade SWbemMethod. Origin</span><span class="sxs-lookup"><span data-stu-id="14900-103">SWbemMethod.Origin property</span></span>

<span data-ttu-id="14900-104">A propriedade **Origin** do objeto [**SWbemMethod**](swbemmethod.md) retorna o nome da classe na qual esse método foi introduzido.</span><span class="sxs-lookup"><span data-stu-id="14900-104">The **Origin** property of the [**SWbemMethod**](swbemmethod.md) object returns the name of the class in which this method was introduced.</span></span> <span data-ttu-id="14900-105">Para classes com hierarquias de herança profundas, geralmente é desejável saber quais métodos foram declarados em quais classes.</span><span class="sxs-lookup"><span data-stu-id="14900-105">For classes with deep inheritance hierarchies, it is often desirable to know which methods were declared in which classes.</span></span> <span data-ttu-id="14900-106">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="14900-106">This property is read-only.</span></span>

<span data-ttu-id="14900-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="14900-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="14900-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="14900-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="14900-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14900-109">Syntax</span></span>


```VB
SWbemMethod.Origin As String
```



## <a name="property-value"></a><span data-ttu-id="14900-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="14900-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="14900-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14900-111">Requirements</span></span>



| <span data-ttu-id="14900-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="14900-112">Requirement</span></span> | <span data-ttu-id="14900-113">Valor</span><span class="sxs-lookup"><span data-stu-id="14900-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14900-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14900-114">Minimum supported client</span></span><br/> | <span data-ttu-id="14900-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14900-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="14900-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14900-116">Minimum supported server</span></span><br/> | <span data-ttu-id="14900-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14900-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="14900-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14900-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="14900-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="14900-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="14900-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="14900-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="14900-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="14900-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="14900-122">DLL</span><span class="sxs-lookup"><span data-stu-id="14900-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14900-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14900-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="14900-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="14900-124">CLSID</span></span><br/>                    | <span data-ttu-id="14900-125">\_SWBEMMETHOD CLSID</span><span class="sxs-lookup"><span data-stu-id="14900-125">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="14900-126">IID</span><span class="sxs-lookup"><span data-stu-id="14900-126">IID</span></span><br/>                      | <span data-ttu-id="14900-127">ISWbemMethod de IID \_</span><span class="sxs-lookup"><span data-stu-id="14900-127">IID\_ISWbemMethod</span></span><br/>                                                            |



 

 




