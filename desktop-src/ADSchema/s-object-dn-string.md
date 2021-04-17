---
title: Sintaxe de objeto (DN-String)
description: Uma cadeia de caracteres de octeto que contém um valor de cadeia de caracteres e um DN.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- Esquema de sintaxe de objeto (DN-String) do AD
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823da21325abdc426d5f58df4cdf04de19fc68b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105769092"
---
# <a name="objectdn-string-syntax"></a><span data-ttu-id="19ad4-104">Sintaxe de objeto (DN-String)</span><span class="sxs-lookup"><span data-stu-id="19ad4-104">Object(DN-String) syntax</span></span>

<span data-ttu-id="19ad4-105">Uma cadeia de caracteres de octeto que contém um valor de cadeia de caracteres e um DN.</span><span class="sxs-lookup"><span data-stu-id="19ad4-105">An octet string that contains a string value and a DN.</span></span>



| <span data-ttu-id="19ad4-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="19ad4-106">Entry</span></span> | <span data-ttu-id="19ad4-107">Valor</span><span class="sxs-lookup"><span data-stu-id="19ad4-107">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="19ad4-108">Nome</span><span class="sxs-lookup"><span data-stu-id="19ad4-108">Name</span></span>         | <span data-ttu-id="19ad4-109">Objeto (DN-String)</span><span class="sxs-lookup"><span data-stu-id="19ad4-109">Object(DN-String)</span></span>                                                                  |
| <span data-ttu-id="19ad4-110">ID da sintaxe</span><span class="sxs-lookup"><span data-stu-id="19ad4-110">Syntax ID</span></span>    | <span data-ttu-id="19ad4-111">2.5.5.14</span><span class="sxs-lookup"><span data-stu-id="19ad4-111">2.5.5.14</span></span>                                                                           |
| <span data-ttu-id="19ad4-112">ID DO OM</span><span class="sxs-lookup"><span data-stu-id="19ad4-112">OM ID</span></span>        | <span data-ttu-id="19ad4-113">127</span><span class="sxs-lookup"><span data-stu-id="19ad4-113">127</span></span>                                                                                |
| <span data-ttu-id="19ad4-114">Tipo de MAPI</span><span class="sxs-lookup"><span data-stu-id="19ad4-114">MAPI Type</span></span>    | \-                                                                                 |
| <span data-ttu-id="19ad4-115">Tipo de ADS</span><span class="sxs-lookup"><span data-stu-id="19ad4-115">ADS Type</span></span>     | <span data-ttu-id="19ad4-116">\_DN ADSTYPE \_ com \_ cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="19ad4-116">ADSTYPE\_DN\_WITH\_STRING</span></span>                                                          |
| <span data-ttu-id="19ad4-117">Tipo de variante</span><span class="sxs-lookup"><span data-stu-id="19ad4-117">Variant Type</span></span> | <span data-ttu-id="19ad4-118">expedição de VT \_</span><span class="sxs-lookup"><span data-stu-id="19ad4-118">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="19ad4-119">Tipo SDS</span><span class="sxs-lookup"><span data-stu-id="19ad4-119">SDS Type</span></span>     | <span data-ttu-id="19ad4-120">Um objeto COM que pode ser convertido em um [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring).</span><span class="sxs-lookup"><span data-stu-id="19ad4-120">A COM object that can be cast to an [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring).</span></span> |



## <a name="remarks"></a><span data-ttu-id="19ad4-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="19ad4-121">Remarks</span></span>

<span data-ttu-id="19ad4-122">Um valor com essa sintaxe tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="19ad4-122">A value with this syntax has the following format:</span></span>

``` syntax
S:<char count>:<string value>:<object DN>
```

<span data-ttu-id="19ad4-123">onde " &lt; contagem &gt; de caracteres" é o número de caracteres na cadeia de caracteres "valor da cadeia de caracteres &lt; &gt; " e " &lt; DN &gt; do objeto" é um nome distinto de um objeto em Active Directory.</span><span class="sxs-lookup"><span data-stu-id="19ad4-123">where "&lt;char count&gt;" is the number of characters in the "&lt;string value&gt;" string, and "&lt;object DN&gt;" is a distinguished name of an object in Active Directory.</span></span> <span data-ttu-id="19ad4-124">Active Directory atualizará o DN se o objeto ao qual ele se refere for movido ou renomeado.</span><span class="sxs-lookup"><span data-stu-id="19ad4-124">Active Directory updates the DN if the object that it refers to is moved or renamed.</span></span>

## <a name="see-also"></a><span data-ttu-id="19ad4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="19ad4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ad4-126">**IADsDNWithString**</span><span class="sxs-lookup"><span data-stu-id="19ad4-126">**IADsDNWithString**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
