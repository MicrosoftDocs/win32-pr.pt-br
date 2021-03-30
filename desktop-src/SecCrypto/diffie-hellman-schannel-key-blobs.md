---
description: Os BLOBs são usados com o provedor Diffie-Hellman/Schannel para exportar chaves e importar chaves para o CSP (provedor de serviços de criptografia).
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: BLOBs de chave Diffie-Hellman/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a76869c6c6239e17a5ae14921805a076c9381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662167"
---
# <a name="diffie-hellmanschannel-key-blobs"></a><span data-ttu-id="e6f6a-103">BLOBs de chave Diffie-Hellman/Schannel</span><span class="sxs-lookup"><span data-stu-id="e6f6a-103">Diffie-Hellman/Schannel Key BLOBs</span></span>

<span data-ttu-id="e6f6a-104">Os [*BLOBs*](../secgloss/b-gly.md) são usados com o provedor Schannel [*Diffie-Hellman*](../secgloss/d-gly.md) / [](../secgloss/s-gly.md) para exportar chaves e importar chaves para o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="e6f6a-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Diffie-Hellman*](../secgloss/d-gly.md)/[*Schannel*](../secgloss/s-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="e6f6a-105">BLOBs de chave pública</span><span class="sxs-lookup"><span data-stu-id="e6f6a-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="e6f6a-106">BLOBs de chave privada</span><span class="sxs-lookup"><span data-stu-id="e6f6a-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="e6f6a-107">BLOBs de chave pública</span><span class="sxs-lookup"><span data-stu-id="e6f6a-107">Public Key BLOBs</span></span>

<span data-ttu-id="e6f6a-108">Diffie-Hellman [*blobs de chave pública*](../secgloss/p-gly.md), digite **PublicKeyBlob**, são usados para trocar o valor (G ^ X) mod P em uma troca de chaves Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-108">Diffie-Hellman [*public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to exchange the (G^X) mod P value in a Diffie-Hellman key exchange.</span></span> <span data-ttu-id="e6f6a-109">Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-109">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

<span data-ttu-id="e6f6a-110">A tabela a seguir descreve cada componente do [*blob de chave*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e6f6a-110">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="e6f6a-111">Campo</span><span class="sxs-lookup"><span data-stu-id="e6f6a-111">Field</span></span>          | <span data-ttu-id="e6f6a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6f6a-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6f6a-113">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="e6f6a-113">dhpubkey</span></span>       | <span data-ttu-id="e6f6a-114">Uma estrutura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="e6f6a-114">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="e6f6a-115">O membro **mágico** deve ser definido como 0x31484400.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-115">The **magic** member must be set to 0x31484400.</span></span> <span data-ttu-id="e6f6a-116">Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de DH1.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-116">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of DH1.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="e6f6a-117">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="e6f6a-117">publickeystruc</span></span> | <span data-ttu-id="e6f6a-118">Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="e6f6a-118">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="e6f6a-119">a</span><span class="sxs-lookup"><span data-stu-id="e6f6a-119">y</span></span>              | <span data-ttu-id="e6f6a-120">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="e6f6a-120">A **BYTE** sequence.</span></span> <span data-ttu-id="e6f6a-121">O valor y, (G ^ X) mod P, está localizado diretamente após a estrutura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="e6f6a-121">The y value, (G^X) mod P, is located directly after the [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="e6f6a-122">O comprimento, em bytes, da sequência é o membro **bitlen** de **DHPUBKEY** dividido por oito.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-122">The length, in bytes, of the sequence is the **bitlen** member of **DHPUBKEY** divided by eight.</span></span> <span data-ttu-id="e6f6a-123">Se o comprimento dos dados que resulta do cálculo de (G ^ X) mod P for um ou mais bytes menores que P dividido por oito, os dados deverão ser preenchidos com os bytes necessários (de valor zero) para tornar os dados o comprimento desejado ([*little-endian*](../secgloss/l-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="e6f6a-123">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by eight, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |



 

## <a name="private-key-blobs"></a><span data-ttu-id="e6f6a-124">BLOBs de chave privada</span><span class="sxs-lookup"><span data-stu-id="e6f6a-124">Private Key BLOBs</span></span>

<span data-ttu-id="e6f6a-125">Os [*blobs de chave privada*](../secgloss/p-gly.md)D-H, digite **PRIVATEKEYBLOB**, são usados para exportar e importar informações privadas de uma chave D-h.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-125">D-H [*private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to export and import private information of a D-H key.</span></span> <span data-ttu-id="e6f6a-126">Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-126">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

<span data-ttu-id="e6f6a-127">A tabela a seguir descreve cada componente do BLOB de chave.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-127">The following table describes each component of the key BLOB.</span></span>



| <span data-ttu-id="e6f6a-128">Campo</span><span class="sxs-lookup"><span data-stu-id="e6f6a-128">Field</span></span>          | <span data-ttu-id="e6f6a-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6f6a-129">Description</span></span>                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6f6a-130">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="e6f6a-130">dhpubkey</span></span>       | <span data-ttu-id="e6f6a-131">Uma estrutura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="e6f6a-131">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="e6f6a-132">O membro **mágico** deve ser definido como 0x32484400.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-132">The **magic** member must be set to 0x32484400.</span></span> <span data-ttu-id="e6f6a-133">Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de DH2.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-133">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of DH2.</span></span> |
| <span data-ttu-id="e6f6a-134">gerador</span><span class="sxs-lookup"><span data-stu-id="e6f6a-134">generator</span></span>      | <span data-ttu-id="e6f6a-135">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="e6f6a-135">A **BYTE** sequence.</span></span> <span data-ttu-id="e6f6a-136">O gerador G.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-136">The generator G.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="e6f6a-137">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="e6f6a-137">publickeystruc</span></span> | <span data-ttu-id="e6f6a-138">Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="e6f6a-138">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                      |
| <span data-ttu-id="e6f6a-139">Trata</span><span class="sxs-lookup"><span data-stu-id="e6f6a-139">prime</span></span>          | <span data-ttu-id="e6f6a-140">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="e6f6a-140">A **BYTE** sequence.</span></span> <span data-ttu-id="e6f6a-141">O principal módulo, P. Esses dados devem sempre ter o bit mais significativo do conjunto de bytes mais significativo para um.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-141">The prime modulus, P. This data must always have the most significant bit of the most significant byte set to one.</span></span>                                                                    |
| <span data-ttu-id="e6f6a-142">segredo</span><span class="sxs-lookup"><span data-stu-id="e6f6a-142">secret</span></span>         | <span data-ttu-id="e6f6a-143">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="e6f6a-143">A **BYTE** sequence.</span></span> <span data-ttu-id="e6f6a-144">O expoente X do segredo.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-144">The secret exponent X.</span></span>                                                                                                                                                                |



 

> [!Note]  
> <span data-ttu-id="e6f6a-145">Os valores primo, Generator e Secret devem sempre ter o mesmo comprimento, em bytes.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-145">The prime, generator, and secret values must always have the same length, in bytes.</span></span> <span data-ttu-id="e6f6a-146">Se qualquer valor for um byte ou mais curto do que os outros, ele deverá ser preenchido com o número necessário de zero bytes para torná-los iguais.</span><span class="sxs-lookup"><span data-stu-id="e6f6a-146">If any value is one byte or more shorter than the others, it must be padded with the necessary number of zero bytes to make them the same.</span></span> <span data-ttu-id="e6f6a-147">O primo, o gerador e o segredo estão no formato [*little-endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e6f6a-147">The prime, generator, and secret are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>

 

 

 
