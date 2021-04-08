---
description: Usado com o provedor DSS (padrão de assinatura digital) para exportar chaves e importar chaves para o CSP (provedor de serviços de criptografia).
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: BLOBs de chave do provedor DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27a73e35cccd6fad672f4c94d589d754f970c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920819"
---
# <a name="dss-provider-key-blobs"></a><span data-ttu-id="c84ac-103">BLOBs de chave do provedor DSS</span><span class="sxs-lookup"><span data-stu-id="c84ac-103">DSS Provider Key BLOBs</span></span>

<span data-ttu-id="c84ac-104">Os [*BLOBs*](../secgloss/b-gly.md) são usados com o provedor DSS ( [*padrão de assinatura digital*](../secgloss/d-gly.md) ) para exportar chaves e importar chaves para o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="c84ac-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Digital Signature Standard*](../secgloss/d-gly.md) (DSS) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="c84ac-105">BLOBs de chave pública</span><span class="sxs-lookup"><span data-stu-id="c84ac-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="c84ac-106">BLOBs de chave privada</span><span class="sxs-lookup"><span data-stu-id="c84ac-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="c84ac-107">BLOBs de chave pública</span><span class="sxs-lookup"><span data-stu-id="c84ac-107">Public Key BLOBs</span></span>

<span data-ttu-id="c84ac-108">Uma [*chave pública*](../secgloss/p-gly.md) DSS é exportada e importada como um blob, uma sequência de bytes estruturados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="c84ac-108">A DSS [*public key*](../secgloss/p-gly.md) is exported and imported as a BLOB, a sequence of bytes structured as follows.</span></span>

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

<span data-ttu-id="c84ac-109">A tabela a seguir descreve esses componentes.</span><span class="sxs-lookup"><span data-stu-id="c84ac-109">The following table describes these components.</span></span> <span data-ttu-id="c84ac-110">Todos os valores estão no formato [*little-endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c84ac-110">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="c84ac-111">Campo</span><span class="sxs-lookup"><span data-stu-id="c84ac-111">Field</span></span>          | <span data-ttu-id="c84ac-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c84ac-112">Description</span></span>                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c84ac-113">dsspubkey</span><span class="sxs-lookup"><span data-stu-id="c84ac-113">dsspubkey</span></span>      | <span data-ttu-id="c84ac-114">Uma estrutura [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c84ac-114">A [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) structure.</span></span> <span data-ttu-id="c84ac-115">O membro **mágico** deve ter um valor de 0x31535344.</span><span class="sxs-lookup"><span data-stu-id="c84ac-115">The **magic** member must have a value of 0x31535344.</span></span> <span data-ttu-id="c84ac-116">Esse número hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de DSS1.</span><span class="sxs-lookup"><span data-stu-id="c84ac-116">This hexadecimal number is the [*ASCII*](../secgloss/a-gly.md) encoding of DSS1.</span></span> |
| <span data-ttu-id="c84ac-117">g</span><span class="sxs-lookup"><span data-stu-id="c84ac-117">g</span></span>              | <span data-ttu-id="c84ac-118">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="c84ac-118">A **BYTE** sequence.</span></span> <span data-ttu-id="c84ac-119">O gerador, g.</span><span class="sxs-lookup"><span data-stu-id="c84ac-119">The generator, g.</span></span> <span data-ttu-id="c84ac-120">Deve ter o mesmo comprimento que p.</span><span class="sxs-lookup"><span data-stu-id="c84ac-120">Must be the same length as p.</span></span> <span data-ttu-id="c84ac-121">Se não tiver o mesmo comprimento que p, ele deverá ser preenchido com 0x00 bytes.</span><span class="sxs-lookup"><span data-stu-id="c84ac-121">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                      |
| <span data-ttu-id="c84ac-122">p</span><span class="sxs-lookup"><span data-stu-id="c84ac-122">p</span></span>              | <span data-ttu-id="c84ac-123">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="c84ac-123">A **BYTE** sequence.</span></span> <span data-ttu-id="c84ac-124">O principal módulo, p.</span><span class="sxs-lookup"><span data-stu-id="c84ac-124">The prime modulus, p.</span></span> <span data-ttu-id="c84ac-125">O bit mais significativo do byte mais significativo deve ser definido como um.</span><span class="sxs-lookup"><span data-stu-id="c84ac-125">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                                 |
| <span data-ttu-id="c84ac-126">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="c84ac-126">publickeystruc</span></span> | <span data-ttu-id="c84ac-127">Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="c84ac-127">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                |
| <span data-ttu-id="c84ac-128">q</span><span class="sxs-lookup"><span data-stu-id="c84ac-128">q</span></span>              | <span data-ttu-id="c84ac-129">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="c84ac-129">A **BYTE** sequence.</span></span> <span data-ttu-id="c84ac-130">A Prime, q, 20 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c84ac-130">The prime, q, 20 bytes in length.</span></span> <span data-ttu-id="c84ac-131">O bit mais significativo do byte mais significativo deve ser definido como um.</span><span class="sxs-lookup"><span data-stu-id="c84ac-131">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                     |
| <span data-ttu-id="c84ac-132">seedstruct</span><span class="sxs-lookup"><span data-stu-id="c84ac-132">seedstruct</span></span>     | <span data-ttu-id="c84ac-133">Uma estrutura [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) .</span><span class="sxs-lookup"><span data-stu-id="c84ac-133">A [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) structure.</span></span> <span data-ttu-id="c84ac-134">Valores de semente e Counter para verificar as Primes.</span><span class="sxs-lookup"><span data-stu-id="c84ac-134">Seed and counter values for verifying primes.</span></span>                                                                                                                                |
| <span data-ttu-id="c84ac-135">a</span><span class="sxs-lookup"><span data-stu-id="c84ac-135">y</span></span>              | <span data-ttu-id="c84ac-136">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="c84ac-136">A **BYTE** sequence.</span></span> <span data-ttu-id="c84ac-137">A chave pública, y.</span><span class="sxs-lookup"><span data-stu-id="c84ac-137">The public key, y.</span></span> <span data-ttu-id="c84ac-138">Deve ter o mesmo comprimento que p.</span><span class="sxs-lookup"><span data-stu-id="c84ac-138">Must be same length as p.</span></span> <span data-ttu-id="c84ac-139">Se não tiver o mesmo comprimento que p, ele deverá ser preenchido com 0x00 bytes.</span><span class="sxs-lookup"><span data-stu-id="c84ac-139">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                         |



 

> [!Note]  
> <span data-ttu-id="c84ac-140">Os [*blobs de chave pública*](../secgloss/p-gly.md) não são criptografados.</span><span class="sxs-lookup"><span data-stu-id="c84ac-140">[*Public key BLOBs*](../secgloss/p-gly.md) are not encrypted.</span></span> <span data-ttu-id="c84ac-141">Elas contêm chaves públicas em formato de [*texto sem formatação*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c84ac-141">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="c84ac-142">BLOBs de chave privada</span><span class="sxs-lookup"><span data-stu-id="c84ac-142">Private Key BLOBs</span></span>

<span data-ttu-id="c84ac-143">Uma [*chave privada*](../secgloss/p-gly.md) DSS é exportada e importada como uma sequência de bytes estruturados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="c84ac-143">A DSS [*private key*](../secgloss/p-gly.md) is exported and imported as a sequence of bytes structured as follows.</span></span>

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

<span data-ttu-id="c84ac-144">A tabela a seguir descreve cada componente.</span><span class="sxs-lookup"><span data-stu-id="c84ac-144">The following table describes each component.</span></span> <span data-ttu-id="c84ac-145">Todos os valores estão no formato [*little-endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c84ac-145">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="c84ac-146">Campo</span><span class="sxs-lookup"><span data-stu-id="c84ac-146">Field</span></span>          | <span data-ttu-id="c84ac-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="c84ac-147">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c84ac-148">dsspubkey</span><span class="sxs-lookup"><span data-stu-id="c84ac-148">dsspubkey</span></span>      | <span data-ttu-id="c84ac-149">Uma estrutura [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c84ac-149">A [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) structure.</span></span> <span data-ttu-id="c84ac-150">O membro **mágico** deve ser definido como 0x32535344.</span><span class="sxs-lookup"><span data-stu-id="c84ac-150">The **magic** member must be set to 0x32535344.</span></span> <span data-ttu-id="c84ac-151">Esse número hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de DSS2.</span><span class="sxs-lookup"><span data-stu-id="c84ac-151">This hexadecimal number is the [*ASCII*](../secgloss/a-gly.md) encoding of DSS2.</span></span> |
| <span data-ttu-id="c84ac-152">g</span><span class="sxs-lookup"><span data-stu-id="c84ac-152">g</span></span>              | <span data-ttu-id="c84ac-153">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="c84ac-153">A **BYTE** sequence.</span></span> <span data-ttu-id="c84ac-154">O gerador, g.</span><span class="sxs-lookup"><span data-stu-id="c84ac-154">The generator, g.</span></span> <span data-ttu-id="c84ac-155">Deve ter o mesmo comprimento que p.</span><span class="sxs-lookup"><span data-stu-id="c84ac-155">Must be the same length as p.</span></span> <span data-ttu-id="c84ac-156">Se não tiver o mesmo comprimento que p, ele deverá ser preenchido com 0x00 bytes.</span><span class="sxs-lookup"><span data-stu-id="c84ac-156">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                |
| <span data-ttu-id="c84ac-157">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="c84ac-157">publickeystruc</span></span> | <span data-ttu-id="c84ac-158">Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="c84ac-158">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                          |
| <span data-ttu-id="c84ac-159">p</span><span class="sxs-lookup"><span data-stu-id="c84ac-159">p</span></span>              | <span data-ttu-id="c84ac-160">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="c84ac-160">A **BYTE** sequence.</span></span> <span data-ttu-id="c84ac-161">O principal módulo, p.</span><span class="sxs-lookup"><span data-stu-id="c84ac-161">The prime modulus, p.</span></span> <span data-ttu-id="c84ac-162">O bit mais significativo do byte mais significativo deve ser definido como um.</span><span class="sxs-lookup"><span data-stu-id="c84ac-162">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                           |
| <span data-ttu-id="c84ac-163">q</span><span class="sxs-lookup"><span data-stu-id="c84ac-163">q</span></span>              | <span data-ttu-id="c84ac-164">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="c84ac-164">A **BYTE** sequence.</span></span> <span data-ttu-id="c84ac-165">O primo, q.</span><span class="sxs-lookup"><span data-stu-id="c84ac-165">The prime, q.</span></span> <span data-ttu-id="c84ac-166">q tem 20 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c84ac-166">q is 20 bytes in length.</span></span> <span data-ttu-id="c84ac-167">O bit mais significativo do byte mais significativo deve ser definido como um.</span><span class="sxs-lookup"><span data-stu-id="c84ac-167">The most significant bit of the most significant byte must be set to one.</span></span>                                                                          |
| <span data-ttu-id="c84ac-168">seedstruct</span><span class="sxs-lookup"><span data-stu-id="c84ac-168">seedstruct</span></span>     | <span data-ttu-id="c84ac-169">Uma estrutura [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) .</span><span class="sxs-lookup"><span data-stu-id="c84ac-169">A [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) structure.</span></span> <span data-ttu-id="c84ac-170">Valores de semente e Counter para verificar as Primes.</span><span class="sxs-lookup"><span data-stu-id="c84ac-170">Seed and counter values for verifying primes.</span></span>                                                                                                                          |
| <span data-ttu-id="c84ac-171">x</span><span class="sxs-lookup"><span data-stu-id="c84ac-171">x</span></span>              | <span data-ttu-id="c84ac-172">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="c84ac-172">A **BYTE** sequence.</span></span> <span data-ttu-id="c84ac-173">O expoente secreto, x.</span><span class="sxs-lookup"><span data-stu-id="c84ac-173">The secret exponent, x.</span></span> <span data-ttu-id="c84ac-174">Deve ter sempre 20 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c84ac-174">Must always be 20 bytes in length.</span></span> <span data-ttu-id="c84ac-175">Se x tiver um comprimento menor que 20 bytes, ele deverá ser preenchido com 0x00.</span><span class="sxs-lookup"><span data-stu-id="c84ac-175">If x is smaller than 20 bytes in length, then it must be padded with 0x00.</span></span>                                                     |



 

<span data-ttu-id="c84ac-176">Ao chamar [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), o desenvolvedor pode escolher se deseja criptografar a chave.</span><span class="sxs-lookup"><span data-stu-id="c84ac-176">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="c84ac-177">O **PRIVATEKEYBLOB** será criptografado se o parâmetro *hExpKey* contiver um identificador válido para uma chave de sessão.</span><span class="sxs-lookup"><span data-stu-id="c84ac-177">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="c84ac-178">Tudo menos a parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) do blob é criptografada.</span><span class="sxs-lookup"><span data-stu-id="c84ac-178">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="c84ac-179">Os parâmetros de algoritmo de criptografia e chave de criptografia não são armazenados junto com o BLOB de chave privada.</span><span class="sxs-lookup"><span data-stu-id="c84ac-179">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="c84ac-180">O aplicativo deve gerenciar e armazenar essas informações.</span><span class="sxs-lookup"><span data-stu-id="c84ac-180">The application must manage and store this information.</span></span> <span data-ttu-id="c84ac-181">Se zero for passado para *hExpKey*, a chave privada será exportada sem criptografia.</span><span class="sxs-lookup"><span data-stu-id="c84ac-181">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="c84ac-182">É perigoso exportar chaves privadas sem criptografia porque elas são então vulneráveis à interceptação e ao uso por entidades não autorizadas.</span><span class="sxs-lookup"><span data-stu-id="c84ac-182">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

 

 
