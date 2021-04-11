---
title: atributo ms-AuthZ-Resource-Condition
description: Para uma regra de acesso central, esse atributo é uma expressão que identifica o escopo do recurso de destino ao qual a política se aplica.
ms.assetid: d3c1815e-3fa1-4106-82a1-74403f07fcde
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-AuthZ-Resource-Condition
- Esquema de AD do atributo msAuthz-ResourceCondition
topic_type:
- apiref
api_name:
- ms-Authz-Resource-Condition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3891e75763fd52d14d4ceaac560b33c824d06449
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087108"
---
# <a name="ms-authz-resource-condition-attribute"></a><span data-ttu-id="23551-105">atributo ms-AuthZ-Resource-Condition</span><span class="sxs-lookup"><span data-stu-id="23551-105">ms-Authz-Resource-Condition attribute</span></span>

<span data-ttu-id="23551-106">Para uma regra de acesso central, esse atributo é uma expressão que identifica o escopo do recurso de destino ao qual a política se aplica.</span><span class="sxs-lookup"><span data-stu-id="23551-106">For a central access rule, this attribute is an expression that identifies the scope of the target resource to which the policy applies.</span></span>



| <span data-ttu-id="23551-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="23551-107">Entry</span></span> | <span data-ttu-id="23551-108">Valor</span><span class="sxs-lookup"><span data-stu-id="23551-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="23551-109">CN</span><span class="sxs-lookup"><span data-stu-id="23551-109">CN</span></span>                | <span data-ttu-id="23551-110">MS-AuthZ-Resource-Condition</span><span class="sxs-lookup"><span data-stu-id="23551-110">ms-Authz-Resource-Condition</span></span>                 |
| <span data-ttu-id="23551-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="23551-111">Ldap-Display-Name</span></span> | <span data-ttu-id="23551-112">msAuthz-ResourceCondition</span><span class="sxs-lookup"><span data-stu-id="23551-112">msAuthz-ResourceCondition</span></span>                   |
| <span data-ttu-id="23551-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="23551-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="23551-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="23551-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="23551-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="23551-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="23551-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="23551-116">Attribute-Id</span></span>      | <span data-ttu-id="23551-117">1.2.840.113556.1.4.2153</span><span class="sxs-lookup"><span data-stu-id="23551-117">1.2.840.113556.1.4.2153</span></span>                     |
| <span data-ttu-id="23551-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="23551-118">System-Id-Guid</span></span>    | <span data-ttu-id="23551-119">80997877-f874-4c68-864d-6e508a83bdbd</span><span class="sxs-lookup"><span data-stu-id="23551-119">80997877-f874-4c68-864d-6e508a83bdbd</span></span>        |
| <span data-ttu-id="23551-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="23551-120">Syntax</span></span>            | [<span data-ttu-id="23551-121">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="23551-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="23551-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="23551-122">Implementations</span></span>

-   [<span data-ttu-id="23551-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="23551-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="23551-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="23551-124">Windows Server 2012</span></span>



| <span data-ttu-id="23551-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="23551-125">Entry</span></span> | <span data-ttu-id="23551-126">Valor</span><span class="sxs-lookup"><span data-stu-id="23551-126">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="23551-127">ID do link</span><span class="sxs-lookup"><span data-stu-id="23551-127">Link-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="23551-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23551-128">MAPI-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="23551-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="23551-129">System-Only</span></span>            | <span data-ttu-id="23551-130">Falso</span><span class="sxs-lookup"><span data-stu-id="23551-130">False</span></span>                                                                          |
| <span data-ttu-id="23551-131">É de valor único</span><span class="sxs-lookup"><span data-stu-id="23551-131">Is-Single-Valued</span></span>       | <span data-ttu-id="23551-132">True</span><span class="sxs-lookup"><span data-stu-id="23551-132">True</span></span>                                                                           |
| <span data-ttu-id="23551-133">É indexado</span><span class="sxs-lookup"><span data-stu-id="23551-133">Is Indexed</span></span>             | <span data-ttu-id="23551-134">Falso</span><span class="sxs-lookup"><span data-stu-id="23551-134">False</span></span>                                                                          |
| <span data-ttu-id="23551-135">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="23551-135">In Global Catalog</span></span>      | <span data-ttu-id="23551-136">Falso</span><span class="sxs-lookup"><span data-stu-id="23551-136">False</span></span>                                                                          |
| <span data-ttu-id="23551-137">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="23551-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="23551-138">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="23551-138">O:BAG:BAD:S:</span></span>                                                                   |
| <span data-ttu-id="23551-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23551-139">Range-Lower</span></span>            | \-                                                                             |
| <span data-ttu-id="23551-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23551-140">Range-Upper</span></span>            | \-                                                                             |
| <span data-ttu-id="23551-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23551-141">Search-Flags</span></span>           | <span data-ttu-id="23551-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23551-142">0x00000000</span></span>                                                                     |
| <span data-ttu-id="23551-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23551-143">System-Flags</span></span>           | <span data-ttu-id="23551-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23551-144">0x00000010</span></span>                                                                     |
| <span data-ttu-id="23551-145">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="23551-145">Classes used in</span></span>        | [<span data-ttu-id="23551-146">**MS-AuthZ-central-Access-Rule**</span><span class="sxs-lookup"><span data-stu-id="23551-146">**ms-Authz-Central-Access-Rule**</span></span>](c-msauthz-centralaccessrule.md)<br/> |



 

 





