---
description: Os BLOBs são usados com o provedor de Diffie-Hellman para exportar chaves e importar chaves para o CSP (provedor de serviços de criptografia).
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: BLOBs de chave de Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9194a9c12542fc0acf36aa0064a2f3e304e25f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757475"
---
# <a name="diffie-hellman-key-blobs"></a><span data-ttu-id="0c452-103">BLOBs de chave de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="0c452-103">Diffie-Hellman Key BLOBs</span></span>

<span data-ttu-id="0c452-104">Os [*BLOBs*](../secgloss/b-gly.md) são usados com o provedor [*Diffie-Hellman*](../secgloss/d-gly.md) para exportar chaves e importar chaves para o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="0c452-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Diffie-Hellman*](../secgloss/d-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="0c452-105">BLOBs de chave pública</span><span class="sxs-lookup"><span data-stu-id="0c452-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="0c452-106">BLOBs de chave privada</span><span class="sxs-lookup"><span data-stu-id="0c452-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="0c452-107">BLOBs de chave pública</span><span class="sxs-lookup"><span data-stu-id="0c452-107">Public Key BLOBs</span></span>

<span data-ttu-id="0c452-108">Diffie-Hellman [*blobs de chave pública*](../secgloss/p-gly.md), digite **PublicKeyBlob**, são usados para trocar o valor (G ^ X) mod P em uma troca de chaves Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="0c452-108">Diffie-Hellman [*public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to exchange the (G^X) mod P value in a Diffie-Hellman key exchange.</span></span> <span data-ttu-id="0c452-109">Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="0c452-109">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

<span data-ttu-id="0c452-110">A tabela a seguir descreve cada componente do [*blob de chave*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0c452-110">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="0c452-111">Campo</span><span class="sxs-lookup"><span data-stu-id="0c452-111">Field</span></span>          | <span data-ttu-id="0c452-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c452-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c452-113">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="0c452-113">dhpubkey</span></span>       | <span data-ttu-id="0c452-114">Uma estrutura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="0c452-114">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="0c452-115">O membro **mágico** deve ser definido como 0x31484400.</span><span class="sxs-lookup"><span data-stu-id="0c452-115">The **magic** member should be set to 0x31484400.</span></span> <span data-ttu-id="0c452-116">Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de "DH1".</span><span class="sxs-lookup"><span data-stu-id="0c452-116">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of "DH1".</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="0c452-117">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="0c452-117">publickeystruc</span></span> | <span data-ttu-id="0c452-118">Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="0c452-118">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="0c452-119">a</span><span class="sxs-lookup"><span data-stu-id="0c452-119">y</span></span>              | <span data-ttu-id="0c452-120">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="0c452-120">A **BYTE** sequence.</span></span> <span data-ttu-id="0c452-121">O valor Y, (G ^ X) mod P, está localizado diretamente após a estrutura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) e deve ser sempre o comprimento, em bytes, do campo **DHPUBKEY bitlen** (tamanho de bit P) dividido por oito.</span><span class="sxs-lookup"><span data-stu-id="0c452-121">The Y value, (G^X) mod P, is located directly after the [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure, and should always be the length, in bytes, of the **DHPUBKEY bitlen** field (bit length of P) divided by eight.</span></span> <span data-ttu-id="0c452-122">Se o comprimento dos dados que resulta do cálculo de (G ^ X) mod P for um ou mais bytes menores que P dividido por oito, os dados deverão ser preenchidos com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado ([*little-endian*](../secgloss/l-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="0c452-122">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by eight, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |



 

## <a name="private-key-blobs"></a><span data-ttu-id="0c452-123">BLOBs de chave privada</span><span class="sxs-lookup"><span data-stu-id="0c452-123">Private Key BLOBs</span></span>

<span data-ttu-id="0c452-124">Diffie-Hellman [*blobs de chave privada*](../secgloss/p-gly.md), digite **PRIVATEKEYBLOB**, são usados para armazenar as informações públicas/privadas de uma chave de Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="0c452-124">Diffie-Hellman [*private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store the public/private information of a Diffie-Hellman key.</span></span> <span data-ttu-id="0c452-125">Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="0c452-125">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

<span data-ttu-id="0c452-126">A tabela a seguir descreve cada componente do BLOB de chave.</span><span class="sxs-lookup"><span data-stu-id="0c452-126">The following table describes each component of the key BLOB.</span></span>



| <span data-ttu-id="0c452-127">Campo</span><span class="sxs-lookup"><span data-stu-id="0c452-127">Field</span></span>          | <span data-ttu-id="0c452-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c452-128">Description</span></span>                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c452-129">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="0c452-129">dhpubkey</span></span>       | <span data-ttu-id="0c452-130">Uma estrutura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="0c452-130">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="0c452-131">O membro **mágico** deve ser definido como 0x32484400.</span><span class="sxs-lookup"><span data-stu-id="0c452-131">The **magic** member must be set to 0x32484400.</span></span> <span data-ttu-id="0c452-132">Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de "DH2".</span><span class="sxs-lookup"><span data-stu-id="0c452-132">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of "DH2".</span></span> |
| <span data-ttu-id="0c452-133">gerador</span><span class="sxs-lookup"><span data-stu-id="0c452-133">generator</span></span>      | <span data-ttu-id="0c452-134">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="0c452-134">A **BYTE** sequence.</span></span> <span data-ttu-id="0c452-135">O gerador, G.</span><span class="sxs-lookup"><span data-stu-id="0c452-135">The generator, G.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="0c452-136">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="0c452-136">publickeystruc</span></span> | <span data-ttu-id="0c452-137">Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="0c452-137">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                        |
| <span data-ttu-id="0c452-138">Trata</span><span class="sxs-lookup"><span data-stu-id="0c452-138">prime</span></span>          | <span data-ttu-id="0c452-139">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="0c452-139">A **BYTE** sequence.</span></span> <span data-ttu-id="0c452-140">O principal módulo, P. Esses dados devem sempre ter o bit mais significativo do conjunto de bytes mais significativo para um.</span><span class="sxs-lookup"><span data-stu-id="0c452-140">The prime modulus, P. This data must always have the most significant bit of the most significant byte set to one.</span></span>                                                                      |
| <span data-ttu-id="0c452-141">segredo</span><span class="sxs-lookup"><span data-stu-id="0c452-141">secret</span></span>         | <span data-ttu-id="0c452-142">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="0c452-142">A **BYTE** sequence.</span></span> <span data-ttu-id="0c452-143">O expoente secreto, X.</span><span class="sxs-lookup"><span data-stu-id="0c452-143">The secret exponent, X.</span></span>                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="0c452-144">O gerador e o segredo devem sempre ter o mesmo comprimento, em bytes.</span><span class="sxs-lookup"><span data-stu-id="0c452-144">The generator and secret must always have the same length, in bytes.</span></span> <span data-ttu-id="0c452-145">Se for um byte ou mais curto do que o outro, ele deverá ser preenchido com o número necessário de bytes de valor zero para torná-los os mesmos.</span><span class="sxs-lookup"><span data-stu-id="0c452-145">If either is one byte or more shorter than the other, it must be padded with the necessary number of zero value bytes to make them the same.</span></span> <span data-ttu-id="0c452-146">O gerador e o segredo estão no formato [*little-endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="0c452-146">Both the generator and the secret are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>

 

 

 
