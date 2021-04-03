---
title: Objeto de sintaxe LDAP
description: O provedor LDAP usa o mapeamento a seguir entre a sintaxe LDAP e a sintaxe ADSI.
ms.assetid: a82cf8ab-9591-4489-87a6-ccfab0e01d61
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, provedores de serviços, sintaxe de mapeamento para sintaxe LDAP
- mapeando a sintaxe ADSI para a sintaxe LDAP ADSI
- sintaxe e mapeamento de ADSI para LDAP ADSI
- ADSI do provedor de serviços LDAP, mapeando sintaxe ADSI para sintaxe LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2272a0805ec32fd7ade9c4584feefb64fb1467f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084007"
---
# <a name="ldap-syntax-object"></a><span data-ttu-id="16198-107">Objeto de sintaxe LDAP</span><span class="sxs-lookup"><span data-stu-id="16198-107">LDAP Syntax Object</span></span>

<span data-ttu-id="16198-108">O provedor LDAP usa o mapeamento a seguir entre a sintaxe LDAP e a sintaxe ADSI.</span><span class="sxs-lookup"><span data-stu-id="16198-108">The LDAP provider uses the following mapping between the LDAP syntax and ADSI syntax.</span></span>



| <span data-ttu-id="16198-109">Sintaxe LDAP</span><span class="sxs-lookup"><span data-stu-id="16198-109">LDAP Syntax</span></span>   | <span data-ttu-id="16198-110">Sintaxe ADSI (automação)</span><span class="sxs-lookup"><span data-stu-id="16198-110">ADSI Syntax (Automation)</span></span>            |
|---------------|-------------------------------------|
| <span data-ttu-id="16198-111">ADsPath</span><span class="sxs-lookup"><span data-stu-id="16198-111">ADsPath</span></span>       | <span data-ttu-id="16198-112">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="16198-112">VT\_BSTR</span></span>                            |
| <span data-ttu-id="16198-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="16198-113">Boolean</span></span>       | <span data-ttu-id="16198-114">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="16198-114">VT\_BOOL</span></span>                            |
| <span data-ttu-id="16198-115">Contador</span><span class="sxs-lookup"><span data-stu-id="16198-115">Counter</span></span>       | <span data-ttu-id="16198-116">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="16198-116">VT\_I4</span></span>                              |
| <span data-ttu-id="16198-117">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="16198-117">EmailAddress</span></span>  | <span data-ttu-id="16198-118">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="16198-118">VT\_BSTR</span></span>                            |
| <span data-ttu-id="16198-119">FaxNumber</span><span class="sxs-lookup"><span data-stu-id="16198-119">FaxNumber</span></span>     | <span data-ttu-id="16198-120">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="16198-120">VT\_BSTR</span></span>                            |
| <span data-ttu-id="16198-121">Integer</span><span class="sxs-lookup"><span data-stu-id="16198-121">Integer</span></span>       | <span data-ttu-id="16198-122">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="16198-122">VT\_I4</span></span>                              |
| <span data-ttu-id="16198-123">Intervalo</span><span class="sxs-lookup"><span data-stu-id="16198-123">Interval</span></span>      | <span data-ttu-id="16198-124">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="16198-124">VT\_I4</span></span>                              |
| <span data-ttu-id="16198-125">Lista</span><span class="sxs-lookup"><span data-stu-id="16198-125">List</span></span>          | <span data-ttu-id="16198-126">VT \_ Variant ( \_ matriz VT BSTR \| VT \_ )</span><span class="sxs-lookup"><span data-stu-id="16198-126">VT\_VARIANT (VT\_BSTR \| VT\_ARRAY)</span></span> |
| <span data-ttu-id="16198-127">Endereço</span><span class="sxs-lookup"><span data-stu-id="16198-127">NetAddress</span></span>    | <span data-ttu-id="16198-128">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="16198-128">VT\_BSTR</span></span>                            |
| <span data-ttu-id="16198-129">Octetstring</span><span class="sxs-lookup"><span data-stu-id="16198-129">OctetString</span></span>   | <span data-ttu-id="16198-130">variante do VT \_</span><span class="sxs-lookup"><span data-stu-id="16198-130">VT\_VARIANT</span></span>                         |
| <span data-ttu-id="16198-131">Caminho</span><span class="sxs-lookup"><span data-stu-id="16198-131">Path</span></span>          | <span data-ttu-id="16198-132">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="16198-132">VT\_BSTR</span></span>                            |
| <span data-ttu-id="16198-133">PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="16198-133">PhoneNumber</span></span>   | <span data-ttu-id="16198-134">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="16198-134">VT\_BSTR</span></span>                            |
| <span data-ttu-id="16198-135">PostalAddress</span><span class="sxs-lookup"><span data-stu-id="16198-135">PostalAddress</span></span> | <span data-ttu-id="16198-136">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="16198-136">VT\_BSTR</span></span>                            |
| <span data-ttu-id="16198-137">SmallInterval</span><span class="sxs-lookup"><span data-stu-id="16198-137">SmallInterval</span></span> | <span data-ttu-id="16198-138">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="16198-138">VT\_I4</span></span>                              |
| <span data-ttu-id="16198-139">String</span><span class="sxs-lookup"><span data-stu-id="16198-139">String</span></span>        | <span data-ttu-id="16198-140">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="16198-140">VT\_BSTR</span></span>                            |
| <span data-ttu-id="16198-141">Hora</span><span class="sxs-lookup"><span data-stu-id="16198-141">Time</span></span>          | <span data-ttu-id="16198-142">Data de VT \_</span><span class="sxs-lookup"><span data-stu-id="16198-142">VT\_DATE</span></span>                            |



 

 

 




