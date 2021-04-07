---
title: atributo ms-DS-egresso-Claims-Transformation-Policy
description: Este é um link para um objeto de política de transformação de declarações para as declarações de saída (declarações que saem dessa floresta) para o domínio confiável.
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- Esquema do AD do MS-DS-egresso-Claims-Transformation-Policy
- atributo msDS-EgressClaimsTransformationPolicy do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3978944b6ae85fcc5fd33682abec7dd3fff0057
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919497"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a><span data-ttu-id="a74c0-105">atributo ms-DS-egresso-Claims-Transformation-Policy</span><span class="sxs-lookup"><span data-stu-id="a74c0-105">ms-DS-Egress-Claims-Transformation-Policy attribute</span></span>

<span data-ttu-id="a74c0-106">Este é um link para um objeto de política de transformação de declarações para as declarações de saída (declarações que saem dessa floresta) para o domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="a74c0-106">This is a link to a Claims Transformation Policy Object for the egress claims (claims leaving this forest) to the Trusted Domain.</span></span> <span data-ttu-id="a74c0-107">Isso é aplicável somente a uma relação de confiança entre florestas de entrada ou bidirecional.</span><span class="sxs-lookup"><span data-stu-id="a74c0-107">This is applicable only for an incoming or bidirectional Cross-Forest Trust.</span></span> <span data-ttu-id="a74c0-108">Quando esse link não está presente, todas as declarações têm permissão para saída no estado em que se encontram.</span><span class="sxs-lookup"><span data-stu-id="a74c0-108">When this link is not present, all claims are allowed to egress as-is.</span></span>



| <span data-ttu-id="a74c0-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a74c0-109">Entry</span></span> | <span data-ttu-id="a74c0-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a74c0-110">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="a74c0-111">CN</span><span class="sxs-lookup"><span data-stu-id="a74c0-111">CN</span></span>                | <span data-ttu-id="a74c0-112">ms-DS-egresso-Claims-Transformation-Policy</span><span class="sxs-lookup"><span data-stu-id="a74c0-112">ms-DS-Egress-Claims-Transformation-Policy</span></span> |
| <span data-ttu-id="a74c0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a74c0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a74c0-114">msDS-EgressClaimsTransformationPolicy</span><span class="sxs-lookup"><span data-stu-id="a74c0-114">msDS-EgressClaimsTransformationPolicy</span></span>     |
| <span data-ttu-id="a74c0-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a74c0-115">Size</span></span>              | \-                                        |
| <span data-ttu-id="a74c0-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a74c0-116">Update Privilege</span></span>  | \-                                        |
| <span data-ttu-id="a74c0-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a74c0-117">Update Frequency</span></span>  | \-                                        |
| <span data-ttu-id="a74c0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a74c0-118">Attribute-Id</span></span>      | <span data-ttu-id="a74c0-119">1.2.840.113556.1.4.2192</span><span class="sxs-lookup"><span data-stu-id="a74c0-119">1.2.840.113556.1.4.2192</span></span>                   |
| <span data-ttu-id="a74c0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a74c0-120">System-Id-Guid</span></span>    | <span data-ttu-id="a74c0-121">c137427e-9a73-b040-9190-1b095bb43288</span><span class="sxs-lookup"><span data-stu-id="a74c0-121">c137427e-9a73-b040-9190-1b095bb43288</span></span>      |
| <span data-ttu-id="a74c0-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="a74c0-122">Syntax</span></span>            | [<span data-ttu-id="a74c0-123">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a74c0-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)   |



## <a name="implementations"></a><span data-ttu-id="a74c0-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="a74c0-124">Implementations</span></span>

-   [<span data-ttu-id="a74c0-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a74c0-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="a74c0-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a74c0-126">Windows Server 2012</span></span>



| <span data-ttu-id="a74c0-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="a74c0-127">Entry</span></span> | <span data-ttu-id="a74c0-128">Valor</span><span class="sxs-lookup"><span data-stu-id="a74c0-128">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="a74c0-129">ID do link</span><span class="sxs-lookup"><span data-stu-id="a74c0-129">Link-Id</span></span>                | <span data-ttu-id="a74c0-130">2192</span><span class="sxs-lookup"><span data-stu-id="a74c0-130">2192</span></span>                                                 |
| <span data-ttu-id="a74c0-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a74c0-131">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="a74c0-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="a74c0-132">System-Only</span></span>            | <span data-ttu-id="a74c0-133">Falso</span><span class="sxs-lookup"><span data-stu-id="a74c0-133">False</span></span>                                                |
| <span data-ttu-id="a74c0-134">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a74c0-134">Is-Single-Valued</span></span>       | <span data-ttu-id="a74c0-135">True</span><span class="sxs-lookup"><span data-stu-id="a74c0-135">True</span></span>                                                 |
| <span data-ttu-id="a74c0-136">É indexado</span><span class="sxs-lookup"><span data-stu-id="a74c0-136">Is Indexed</span></span>             | <span data-ttu-id="a74c0-137">Falso</span><span class="sxs-lookup"><span data-stu-id="a74c0-137">False</span></span>                                                |
| <span data-ttu-id="a74c0-138">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a74c0-138">In Global Catalog</span></span>      | <span data-ttu-id="a74c0-139">Falso</span><span class="sxs-lookup"><span data-stu-id="a74c0-139">False</span></span>                                                |
| <span data-ttu-id="a74c0-140">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a74c0-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="a74c0-141">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a74c0-141">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="a74c0-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a74c0-142">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="a74c0-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a74c0-143">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="a74c0-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a74c0-144">Search-Flags</span></span>           | <span data-ttu-id="a74c0-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a74c0-145">0x00000000</span></span>                                           |
| <span data-ttu-id="a74c0-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a74c0-146">System-Flags</span></span>           | <span data-ttu-id="a74c0-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a74c0-147">0x00000010</span></span>                                           |
| <span data-ttu-id="a74c0-148">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a74c0-148">Classes used in</span></span>        | [<span data-ttu-id="a74c0-149">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="a74c0-149">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





