---
description: A enumeração do algoritmo capicor \_ hash \_ define um algoritmo de hash.
ms.assetid: 5373b6cc-944a-4d83-ac71-59edcb2af94e
title: Enumeração de CAPICOM_HASH_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_HASH_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 14ee06437f7b6e32c58415e5b9d77a75929250a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758281"
---
# <a name="capicom_hash_algorithm-enumeration"></a><span data-ttu-id="ed9ec-103">Enumeração de algoritmo capicor \_ hash \_</span><span class="sxs-lookup"><span data-stu-id="ed9ec-103">CAPICOM\_HASH\_ALGORITHM enumeration</span></span>

<span data-ttu-id="ed9ec-104">A enumeração do **\_ \_ algoritmo capicor hash** define um algoritmo de hash.</span><span class="sxs-lookup"><span data-stu-id="ed9ec-104">The **CAPICOM\_HASH\_ALGORITHM** enumeration defines a hash algorithm.</span></span>

## <a name="members"></a><span data-ttu-id="ed9ec-105">Membros</span><span class="sxs-lookup"><span data-stu-id="ed9ec-105">Members</span></span>



| <span data-ttu-id="ed9ec-106">Membro</span><span class="sxs-lookup"><span data-stu-id="ed9ec-106">Member</span></span>                                 | <span data-ttu-id="ed9ec-107">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="ed9ec-107">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="ed9ec-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ed9ec-108">Value</span></span> |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="ed9ec-109">**Algoritmo de hash de capico \_ \_ \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="ed9ec-109">**CAPICOM\_HASH\_ALGORITHM\_SHA1**</span></span>     | <span data-ttu-id="ed9ec-110">Sha ( [*algoritmo de hash seguro*](../secgloss/s-gly.md) ) que gera um resumo de mensagens de 160 bits.</span><span class="sxs-lookup"><span data-stu-id="ed9ec-110">[*Secure Hash Algorithm*](../secgloss/s-gly.md) (SHA) that generates a 160-bit message digest.</span></span><br/> | <span data-ttu-id="ed9ec-111">0</span><span class="sxs-lookup"><span data-stu-id="ed9ec-111">0</span></span>     |
| <span data-ttu-id="ed9ec-112">**Algoritmo de hash de CAPICOM \_ \_ \_ MD2**</span><span class="sxs-lookup"><span data-stu-id="ed9ec-112">**CAPICOM\_HASH\_ALGORITHM\_MD2**</span></span>      | <span data-ttu-id="ed9ec-113">Algoritmo de hash MD2.</span><span class="sxs-lookup"><span data-stu-id="ed9ec-113">MD2 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="ed9ec-114">1</span><span class="sxs-lookup"><span data-stu-id="ed9ec-114">1</span></span>     |
| <span data-ttu-id="ed9ec-115">**Algoritmo de hash de CAPICOM \_ \_ \_ MD4**</span><span class="sxs-lookup"><span data-stu-id="ed9ec-115">**CAPICOM\_HASH\_ALGORITHM\_MD4**</span></span>      | <span data-ttu-id="ed9ec-116">Algoritmo de hash MD4.</span><span class="sxs-lookup"><span data-stu-id="ed9ec-116">MD4 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="ed9ec-117">2</span><span class="sxs-lookup"><span data-stu-id="ed9ec-117">2</span></span>     |
| <span data-ttu-id="ed9ec-118">**Algoritmo de hash de capico \_ \_ \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="ed9ec-118">**CAPICOM\_HASH\_ALGORITHM\_MD5**</span></span>      | <span data-ttu-id="ed9ec-119">Algoritmo de hash MD5.</span><span class="sxs-lookup"><span data-stu-id="ed9ec-119">MD5 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="ed9ec-120">3</span><span class="sxs-lookup"><span data-stu-id="ed9ec-120">3</span></span>     |
| <span data-ttu-id="ed9ec-121">**CAPICOM do \_ algoritmo de hash \_ \_ Sha \_ 256**</span><span class="sxs-lookup"><span data-stu-id="ed9ec-121">**CAPICOM\_HASH\_ALGORITHM\_SHA\_256**</span></span> | <span data-ttu-id="ed9ec-122">Algoritmo de hash SHA-256.</span><span class="sxs-lookup"><span data-stu-id="ed9ec-122">SHA-256 hash algorithm.</span></span><br/> <span data-ttu-id="ed9ec-123">**CAPICOM 2.0.0.3 e anteriores:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="ed9ec-123">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="ed9ec-124">4</span><span class="sxs-lookup"><span data-stu-id="ed9ec-124">4</span></span>     |
| <span data-ttu-id="ed9ec-125">**CAPICOM do \_ algoritmo de hash \_ \_ Sha \_ 384**</span><span class="sxs-lookup"><span data-stu-id="ed9ec-125">**CAPICOM\_HASH\_ALGORITHM\_SHA\_384**</span></span> | <span data-ttu-id="ed9ec-126">Algoritmo de hash SHA-384.</span><span class="sxs-lookup"><span data-stu-id="ed9ec-126">SHA-384 hash algorithm.</span></span><br/> <span data-ttu-id="ed9ec-127">**CAPICOM 2.0.0.3 e anteriores:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="ed9ec-127">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="ed9ec-128">5</span><span class="sxs-lookup"><span data-stu-id="ed9ec-128">5</span></span>     |
| <span data-ttu-id="ed9ec-129">**CAPICOM do \_ algoritmo de hash \_ \_ Sha \_ 512**</span><span class="sxs-lookup"><span data-stu-id="ed9ec-129">**CAPICOM\_HASH\_ALGORITHM\_SHA\_512**</span></span> | <span data-ttu-id="ed9ec-130">Algoritmo de hash SHA-512.</span><span class="sxs-lookup"><span data-stu-id="ed9ec-130">SHA-512 hash algorithm.</span></span><br/> <span data-ttu-id="ed9ec-131">**CAPICOM 2.0.0.3 e anteriores:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="ed9ec-131">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="ed9ec-132">6</span><span class="sxs-lookup"><span data-stu-id="ed9ec-132">6</span></span>     |



## <a name="remarks"></a><span data-ttu-id="ed9ec-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed9ec-133">Remarks</span></span>

<span data-ttu-id="ed9ec-134">A enumeração do **\_ \_ algoritmo de hash capicor** é usada pela propriedade [**HashedData. Algorithm**](hasheddata-algorithm.md) .</span><span class="sxs-lookup"><span data-stu-id="ed9ec-134">The **CAPICOM\_HASH\_ALGORITHM** enumeration is used by the [**HashedData.Algorithm**](hasheddata-algorithm.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed9ec-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed9ec-135">Requirements</span></span>



| <span data-ttu-id="ed9ec-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed9ec-136">Requirement</span></span> | <span data-ttu-id="ed9ec-137">Valor</span><span class="sxs-lookup"><span data-stu-id="ed9ec-137">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ed9ec-138">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ed9ec-138">Redistributable</span></span><br/> | <span data-ttu-id="ed9ec-139">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="ed9ec-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="ed9ec-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed9ec-140">Header</span></span><br/>          | <dl> <span data-ttu-id="ed9ec-141"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed9ec-141"><dt>Capicom.h</dt></span></span> </dl> |



 

 
