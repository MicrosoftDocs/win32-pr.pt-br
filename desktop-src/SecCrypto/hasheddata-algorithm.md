---
description: Define ou recupera o tipo de algoritmo de hash usado.
ms.assetid: 3f8e83f2-0e46-494b-ac63-658e663680ea
title: Propriedade HashedData. Algorithm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a27dc275ce900bfd6412599cb81ad14038f96405
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800084"
---
# <a name="hasheddataalgorithm-property"></a><span data-ttu-id="24930-103">Propriedade HashedData. Algorithm</span><span class="sxs-lookup"><span data-stu-id="24930-103">HashedData.Algorithm property</span></span>

<span data-ttu-id="24930-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="24930-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="24930-105">Em vez disso, use a [**classe HashAlgorithm**](/previous-versions/windows/) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="24930-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="24930-106">A propriedade de **algoritmo** define ou recupera o tipo de algoritmo de hash usado.</span><span class="sxs-lookup"><span data-stu-id="24930-106">The **Algorithm** property sets or retrieves the type of hashing algorithm used.</span></span>

## <a name="syntax"></a><span data-ttu-id="24930-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="24930-107">Syntax</span></span>


```VB
HashedData.Algorithm As CAPICOM_HASH_ALGORITHM
```



## <a name="property-value"></a><span data-ttu-id="24930-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="24930-108">Property value</span></span>

<span data-ttu-id="24930-109">Um valor da enumeração [**do \_ \_ algoritmo de hash capicor**](capicom-hash-algorithm.md) que define um algoritmo de hash.</span><span class="sxs-lookup"><span data-stu-id="24930-109">A value of the [**CAPICOM\_HASH\_ALGORITHM**](capicom-hash-algorithm.md) enumeration that defines a hash algorithm.</span></span> <span data-ttu-id="24930-110">O valor padrão é capicont \_ hash \_ Algorithm \_ SHA1.</span><span class="sxs-lookup"><span data-stu-id="24930-110">The default value is CAPICOM\_HASH\_ALGORITHM\_SHA1.</span></span> <span data-ttu-id="24930-111">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="24930-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="24930-112">Valor</span><span class="sxs-lookup"><span data-stu-id="24930-112">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="24930-113">Significado</span><span class="sxs-lookup"><span data-stu-id="24930-113">Meaning</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_HASH_ALGORITHM_SHA1"></span><span id="capicom_hash_algorithm_sha1"></span><dl> <span data-ttu-id="24930-114"><dt>**Algoritmo de hash de capico \_ \_ \_ SHA1**</dt></span><span class="sxs-lookup"><span data-stu-id="24930-114"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA1**</dt></span></span> </dl>           | <span data-ttu-id="24930-115">Algoritmo de hash SHA1.</span><span class="sxs-lookup"><span data-stu-id="24930-115">SHA1 hashing algorithm.</span></span><br/>                                                                          |
| <span id="CAPICOM_HASH_ALGORITHM_MD2"></span><span id="capicom_hash_algorithm_md2"></span><dl> <span data-ttu-id="24930-116"><dt>**Algoritmo de hash de CAPICOM \_ \_ \_ MD2**</dt></span><span class="sxs-lookup"><span data-stu-id="24930-116"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD2**</dt></span></span> </dl>              | <span data-ttu-id="24930-117">Algoritmo de hash MD2.</span><span class="sxs-lookup"><span data-stu-id="24930-117">MD2 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD4"></span><span id="capicom_hash_algorithm_md4"></span><dl> <span data-ttu-id="24930-118"><dt>**Algoritmo de hash de CAPICOM \_ \_ \_ MD4**</dt></span><span class="sxs-lookup"><span data-stu-id="24930-118"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD4**</dt></span></span> </dl>              | <span data-ttu-id="24930-119">Algoritmo de hash MD4.</span><span class="sxs-lookup"><span data-stu-id="24930-119">MD4 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD5"></span><span id="capicom_hash_algorithm_md5"></span><dl> <span data-ttu-id="24930-120"><dt>**Algoritmo de hash de capico \_ \_ \_ MD5**</dt></span><span class="sxs-lookup"><span data-stu-id="24930-120"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD5**</dt></span></span> </dl>              | <span data-ttu-id="24930-121">Algoritmo de hash MD5.</span><span class="sxs-lookup"><span data-stu-id="24930-121">MD5 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_256"></span><span id="capicom_hash_algorithm_sha_256"></span><dl> <span data-ttu-id="24930-122"><dt>**CAPICOM do \_ algoritmo de hash \_ \_ Sha \_ 256**</dt></span><span class="sxs-lookup"><span data-stu-id="24930-122"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_256**</dt></span></span> </dl> | <span data-ttu-id="24930-123">Algoritmo de hash SHA-256.</span><span class="sxs-lookup"><span data-stu-id="24930-123">SHA-256 hash algorithm.</span></span><br/> <span data-ttu-id="24930-124">**CAPICOM 2.0.0.3 e anteriores:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="24930-124">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_384"></span><span id="capicom_hash_algorithm_sha_384"></span><dl> <span data-ttu-id="24930-125"><dt>**CAPICOM do \_ algoritmo de hash \_ \_ Sha \_ 384**</dt></span><span class="sxs-lookup"><span data-stu-id="24930-125"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_384**</dt></span></span> </dl> | <span data-ttu-id="24930-126">Algoritmo de hash SHA-384.</span><span class="sxs-lookup"><span data-stu-id="24930-126">SHA-384 hash algorithm.</span></span><br/> <span data-ttu-id="24930-127">**CAPICOM 2.0.0.3 e anteriores:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="24930-127">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_512"></span><span id="capicom_hash_algorithm_sha_512"></span><dl> <span data-ttu-id="24930-128"><dt>**CAPICOM do \_ algoritmo de hash \_ \_ Sha \_ 512**</dt></span><span class="sxs-lookup"><span data-stu-id="24930-128"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_512**</dt></span></span> </dl> | <span data-ttu-id="24930-129">Algoritmo de hash SHA-512.</span><span class="sxs-lookup"><span data-stu-id="24930-129">SHA-512 hash algorithm.</span></span><br/> <span data-ttu-id="24930-130">**CAPICOM 2.0.0.3 e anteriores:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="24930-130">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="24930-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24930-131">Requirements</span></span>



| <span data-ttu-id="24930-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="24930-132">Requirement</span></span> | <span data-ttu-id="24930-133">Valor</span><span class="sxs-lookup"><span data-stu-id="24930-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24930-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="24930-134">End of client support</span></span><br/> | <span data-ttu-id="24930-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24930-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="24930-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="24930-136">End of server support</span></span><br/> | <span data-ttu-id="24930-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24930-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="24930-138">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="24930-138">Redistributable</span></span><br/>       | <span data-ttu-id="24930-139">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="24930-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="24930-140">DLL</span><span class="sxs-lookup"><span data-stu-id="24930-140">DLL</span></span><br/>                   | <dl> <span data-ttu-id="24930-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24930-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24930-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="24930-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24930-143">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="24930-143">**HashedData**</span></span>](hasheddata.md)
</dt> </dl>

 

 
