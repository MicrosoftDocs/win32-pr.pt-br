---
title: atributo ms-DS-ingress-Claims-Transformation-Policy
description: Este é um link para um objeto de política de transformação de declarações para as declarações de entrada (declarações entrando nesta floresta) do domínio confiável.
ms.assetid: 67f87782-85ed-41bb-a60d-f6c11fcda80e
ms.tgt_platform: multiple
keywords:
- ms-DS-ingress-Claims-Transformation-atributo de política do AD Schema
- atributo msDS-IngressClaimsTransformationPolicy do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Ingress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50e3c187a4cb3b2a465257b408a1f5603c756ba
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499999"
---
# <a name="ms-ds-ingress-claims-transformation-policy-attribute"></a><span data-ttu-id="d1706-105">atributo ms-DS-ingress-Claims-Transformation-Policy</span><span class="sxs-lookup"><span data-stu-id="d1706-105">ms-DS-Ingress-Claims-Transformation-Policy attribute</span></span>

<span data-ttu-id="d1706-106">Este é um link para um objeto de política de transformação de declarações para as declarações de entrada (declarações entrando nesta floresta) do domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="d1706-106">This is a link to a Claims Transformation Policy Object for the ingress claims (claims entering this forest) from the Trusted Domain.</span></span> <span data-ttu-id="d1706-107">Isso é aplicável somente a uma relação de confiança entre florestas ou de saída bidirecional.</span><span class="sxs-lookup"><span data-stu-id="d1706-107">This is applicable only for an outgoing or bidirectional Cross-Forest Trust.</span></span> <span data-ttu-id="d1706-108">Se esse link estiver ausente, todas as declarações de entrada serão descartadas.</span><span class="sxs-lookup"><span data-stu-id="d1706-108">If this link is absent, all the ingress claims are dropped.</span></span>



| <span data-ttu-id="d1706-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1706-109">Entry</span></span> | <span data-ttu-id="d1706-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d1706-110">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="d1706-111">CN</span><span class="sxs-lookup"><span data-stu-id="d1706-111">CN</span></span>                | <span data-ttu-id="d1706-112">ms-DS-ingress-Claims-Transformation-Policy</span><span class="sxs-lookup"><span data-stu-id="d1706-112">ms-DS-Ingress-Claims-Transformation-Policy</span></span> |
| <span data-ttu-id="d1706-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d1706-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d1706-114">msDS-IngressClaimsTransformationPolicy</span><span class="sxs-lookup"><span data-stu-id="d1706-114">msDS-IngressClaimsTransformationPolicy</span></span>     |
| <span data-ttu-id="d1706-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d1706-115">Size</span></span>              | \-                                         |
| <span data-ttu-id="d1706-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="d1706-116">Update Privilege</span></span>  | \-                                         |
| <span data-ttu-id="d1706-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="d1706-117">Update Frequency</span></span>  | \-                                         |
| <span data-ttu-id="d1706-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d1706-118">Attribute-Id</span></span>      | <span data-ttu-id="d1706-119">1.2.840.113556.1.4.2191</span><span class="sxs-lookup"><span data-stu-id="d1706-119">1.2.840.113556.1.4.2191</span></span>                    |
| <span data-ttu-id="d1706-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d1706-120">System-Id-Guid</span></span>    | <span data-ttu-id="d1706-121">86284c08-0c6e-1540-8b15-75147d23d20d</span><span class="sxs-lookup"><span data-stu-id="d1706-121">86284c08-0c6e-1540-8b15-75147d23d20d</span></span>       |
| <span data-ttu-id="d1706-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1706-122">Syntax</span></span>            | [<span data-ttu-id="d1706-123">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="d1706-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)    |



## <a name="implementations"></a><span data-ttu-id="d1706-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="d1706-124">Implementations</span></span>

-   [<span data-ttu-id="d1706-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d1706-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="d1706-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1706-126">Windows Server 2012</span></span>



| <span data-ttu-id="d1706-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1706-127">Entry</span></span> | <span data-ttu-id="d1706-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d1706-128">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d1706-129">ID do link</span><span class="sxs-lookup"><span data-stu-id="d1706-129">Link-Id</span></span>                | <span data-ttu-id="d1706-130">2190</span><span class="sxs-lookup"><span data-stu-id="d1706-130">2190</span></span>                                                 |
| <span data-ttu-id="d1706-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1706-131">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="d1706-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1706-132">System-Only</span></span>            | <span data-ttu-id="d1706-133">Falso</span><span class="sxs-lookup"><span data-stu-id="d1706-133">False</span></span>                                                |
| <span data-ttu-id="d1706-134">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d1706-134">Is-Single-Valued</span></span>       | <span data-ttu-id="d1706-135">True</span><span class="sxs-lookup"><span data-stu-id="d1706-135">True</span></span>                                                 |
| <span data-ttu-id="d1706-136">É indexado</span><span class="sxs-lookup"><span data-stu-id="d1706-136">Is Indexed</span></span>             | <span data-ttu-id="d1706-137">Falso</span><span class="sxs-lookup"><span data-stu-id="d1706-137">False</span></span>                                                |
| <span data-ttu-id="d1706-138">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1706-138">In Global Catalog</span></span>      | <span data-ttu-id="d1706-139">Falso</span><span class="sxs-lookup"><span data-stu-id="d1706-139">False</span></span>                                                |
| <span data-ttu-id="d1706-140">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d1706-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1706-141">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d1706-141">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="d1706-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1706-142">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="d1706-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1706-143">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="d1706-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1706-144">Search-Flags</span></span>           | <span data-ttu-id="d1706-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1706-145">0x00000000</span></span>                                           |
| <span data-ttu-id="d1706-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1706-146">System-Flags</span></span>           | <span data-ttu-id="d1706-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1706-147">0x00000010</span></span>                                           |
| <span data-ttu-id="d1706-148">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d1706-148">Classes used in</span></span>        | [<span data-ttu-id="d1706-149">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="d1706-149">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





