---
description: O provedor base e o provedor estendido usam os mesmos BLOBs de chave.
ms.assetid: b4592036-0fa3-4b7e-beed-78cf1d2f39a9
title: BLOBs de chave do provedor base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c763f97fe6e7868246e0bce30ee2a741e8bd212f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750439"
---
# <a name="base-provider-key-blobs"></a><span data-ttu-id="94dc2-103">BLOBs de chave do provedor base</span><span class="sxs-lookup"><span data-stu-id="94dc2-103">Base Provider Key BLOBs</span></span>

<span data-ttu-id="94dc2-104">O provedor base e o provedor estendido usam os mesmos [*blobs de chave*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="94dc2-104">The Base Provider and Extended Provider use the same [*key BLOBs*](../secgloss/k-gly.md).</span></span>

-   [<span data-ttu-id="94dc2-105">BLOBs de chave pública</span><span class="sxs-lookup"><span data-stu-id="94dc2-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="94dc2-106">BLOBs de chave privada</span><span class="sxs-lookup"><span data-stu-id="94dc2-106">Private Key BLOBs</span></span>](#private-key-blobs)
-   [<span data-ttu-id="94dc2-107">BLOBs de chave simples</span><span class="sxs-lookup"><span data-stu-id="94dc2-107">Simple Key BLOBs</span></span>](#simple-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="94dc2-108">BLOBs de chave pública</span><span class="sxs-lookup"><span data-stu-id="94dc2-108">Public Key BLOBs</span></span>

<span data-ttu-id="94dc2-109">Os [*blobs de chave pública*](../secgloss/p-gly.md), digite **PublicKeyBlob**, são usados para armazenar [*chaves públicas*](../secgloss/p-gly.md) fora de um [*provedor de serviços de criptografia*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="94dc2-109">[*Public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to store [*public keys*](../secgloss/p-gly.md) outside a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span> <span data-ttu-id="94dc2-110">Os BLOBs de chave pública do provedor base têm o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="94dc2-110">Base provider public key BLOBs have the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

<span data-ttu-id="94dc2-111">A tabela a seguir descreve cada componente de chave pública.</span><span class="sxs-lookup"><span data-stu-id="94dc2-111">The following table describes each public key component.</span></span> <span data-ttu-id="94dc2-112">Todos os valores estão no formato [*little-endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="94dc2-112">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="94dc2-113">Campo</span><span class="sxs-lookup"><span data-stu-id="94dc2-113">Field</span></span>          | <span data-ttu-id="94dc2-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="94dc2-114">Description</span></span>                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94dc2-115">módulo</span><span class="sxs-lookup"><span data-stu-id="94dc2-115">modulus</span></span>        | <span data-ttu-id="94dc2-116">Os dados do módulo de chave pública estão localizados diretamente após a estrutura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="94dc2-116">The public key modulus data is located directly after the [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="94dc2-117">O tamanho desses dados irá variar, dependendo do tamanho da chave pública.</span><span class="sxs-lookup"><span data-stu-id="94dc2-117">The size of this data will vary, depending on the size of the public key.</span></span> <span data-ttu-id="94dc2-118">O número de bytes pode ser determinado pela divisão do valor do campo **RSAPUBKEY bitlen** por oito.</span><span class="sxs-lookup"><span data-stu-id="94dc2-118">The number of bytes can be determined by dividing the value of the **RSAPUBKEY bitlen** field by eight.</span></span> |
| <span data-ttu-id="94dc2-119">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="94dc2-119">publickeystruc</span></span> | <span data-ttu-id="94dc2-120">Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="94dc2-120">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="94dc2-121">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="94dc2-121">rsapubkey</span></span>      | <span data-ttu-id="94dc2-122">Uma estrutura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="94dc2-122">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="94dc2-123">O membro **mágico** deve ser definido como 0x31415352.</span><span class="sxs-lookup"><span data-stu-id="94dc2-123">The **magic** member must be set to 0x31415352.</span></span> <span data-ttu-id="94dc2-124">Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de RSA1.</span><span class="sxs-lookup"><span data-stu-id="94dc2-124">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA1.</span></span>                                                                         |



 

> [!Note]  
> <span data-ttu-id="94dc2-125">Os BLOBs de chave pública não são criptografados.</span><span class="sxs-lookup"><span data-stu-id="94dc2-125">Public key BLOBs are not encrypted.</span></span> <span data-ttu-id="94dc2-126">Elas contêm chaves públicas em formato de [*texto sem formatação*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="94dc2-126">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="94dc2-127">BLOBs de chave privada</span><span class="sxs-lookup"><span data-stu-id="94dc2-127">Private Key BLOBs</span></span>

<span data-ttu-id="94dc2-128">Os [*blobs de chave privada*](../secgloss/p-gly.md), o tipo **PRIVATEKEYBLOB**, são usados para armazenar [*chaves privadas*](../secgloss/p-gly.md) fora de um CSP.</span><span class="sxs-lookup"><span data-stu-id="94dc2-128">[*Private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store [*private keys*](../secgloss/p-gly.md) outside a CSP.</span></span> <span data-ttu-id="94dc2-129">Os BLOBs de chave privada do provedor base têm o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="94dc2-129">Base provider private key BLOBs have the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
BYTE prime1[rsapubkey.bitlen/16];
BYTE prime2[rsapubkey.bitlen/16];
BYTE exponent1[rsapubkey.bitlen/16];
BYTE exponent2[rsapubkey.bitlen/16];
BYTE coefficient[rsapubkey.bitlen/16];
BYTE privateExponent[rsapubkey.bitlen/8];
```

<span data-ttu-id="94dc2-130">A tabela a seguir descreve o componente BLOB de chave privada.</span><span class="sxs-lookup"><span data-stu-id="94dc2-130">The following table describes the private key BLOB component.</span></span>

> [!Note]  
> <span data-ttu-id="94dc2-131">Esses campos correspondem aos campos descritos na seção 7,2 de [*padrões de criptografia de chave pública*](../secgloss/p-gly.md) (PKCS) \# 1 com pequenas diferenças.</span><span class="sxs-lookup"><span data-stu-id="94dc2-131">These fields correspond to the fields described in section 7.2 of [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1 with minor differences.</span></span>

 



| <span data-ttu-id="94dc2-132">Campo</span><span class="sxs-lookup"><span data-stu-id="94dc2-132">Field</span></span>           | <span data-ttu-id="94dc2-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="94dc2-133">Description</span></span>                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94dc2-134">cujo</span><span class="sxs-lookup"><span data-stu-id="94dc2-134">coefficient</span></span>     | <span data-ttu-id="94dc2-135">Cujo.</span><span class="sxs-lookup"><span data-stu-id="94dc2-135">Coefficient.</span></span> <span data-ttu-id="94dc2-136">Isso tem um valor numérico de (inverso de q) mod p.</span><span class="sxs-lookup"><span data-stu-id="94dc2-136">This has a numeric value of (inverse of q) mod p.</span></span>                                                                                                                                                |
| <span data-ttu-id="94dc2-137">exponent1</span><span class="sxs-lookup"><span data-stu-id="94dc2-137">exponent1</span></span>       | <span data-ttu-id="94dc2-138">Expoente 1.</span><span class="sxs-lookup"><span data-stu-id="94dc2-138">Exponent 1.</span></span> <span data-ttu-id="94dc2-139">Isso tem um valor numérico de d mod (p – 1).</span><span class="sxs-lookup"><span data-stu-id="94dc2-139">This has a numeric value of d mod (p – 1).</span></span>                                                                                                                                                        |
| <span data-ttu-id="94dc2-140">exponent2</span><span class="sxs-lookup"><span data-stu-id="94dc2-140">exponent2</span></span>       | <span data-ttu-id="94dc2-141">Expoente 2.</span><span class="sxs-lookup"><span data-stu-id="94dc2-141">Exponent 2.</span></span> <span data-ttu-id="94dc2-142">Isso tem um valor numérico de d mod (q – 1).</span><span class="sxs-lookup"><span data-stu-id="94dc2-142">This has a numeric value of d mod (q – 1).</span></span>                                                                                                                                                        |
| <span data-ttu-id="94dc2-143">Modulus</span><span class="sxs-lookup"><span data-stu-id="94dc2-143">Modulus</span></span>         | <span data-ttu-id="94dc2-144">O módulo.</span><span class="sxs-lookup"><span data-stu-id="94dc2-144">The modulus.</span></span> <span data-ttu-id="94dc2-145">Isso tem um valor de *Prime1*×*Prime2* e geralmente é conhecido como n.</span><span class="sxs-lookup"><span data-stu-id="94dc2-145">This has a value of *Prime1*×*Prime2* and is often known as n.</span></span>                                                                                                                                   |
| <span data-ttu-id="94dc2-146">prime1</span><span class="sxs-lookup"><span data-stu-id="94dc2-146">prime1</span></span>          | <span data-ttu-id="94dc2-147">Número principal 1, geralmente conhecido como p.</span><span class="sxs-lookup"><span data-stu-id="94dc2-147">Prime number 1, often known as p.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="94dc2-148">prime2</span><span class="sxs-lookup"><span data-stu-id="94dc2-148">prime2</span></span>          | <span data-ttu-id="94dc2-149">Número principal 2, geralmente conhecido como q.</span><span class="sxs-lookup"><span data-stu-id="94dc2-149">Prime number 2, often known as q.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="94dc2-150">privateExponent</span><span class="sxs-lookup"><span data-stu-id="94dc2-150">privateExponent</span></span> | <span data-ttu-id="94dc2-151">Expoente privado, geralmente conhecido como d.</span><span class="sxs-lookup"><span data-stu-id="94dc2-151">Private exponent, often known as d.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="94dc2-152">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="94dc2-152">publickeystruc</span></span>  | <span data-ttu-id="94dc2-153">Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="94dc2-153">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                         |
| <span data-ttu-id="94dc2-154">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="94dc2-154">rsapubkey</span></span>       | <span data-ttu-id="94dc2-155">Uma estrutura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="94dc2-155">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="94dc2-156">O membro **mágico** deve ser definido como 0x32415352.</span><span class="sxs-lookup"><span data-stu-id="94dc2-156">The **magic** member must be set to 0x32415352.</span></span> <span data-ttu-id="94dc2-157">Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de RSA2.</span><span class="sxs-lookup"><span data-stu-id="94dc2-157">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA2.</span></span> |



 

> [!Note]  
> <span data-ttu-id="94dc2-158">Os BLOBs de chave privada não são criptografados.</span><span class="sxs-lookup"><span data-stu-id="94dc2-158">Private key BLOBs are not encrypted.</span></span> <span data-ttu-id="94dc2-159">Eles contêm chaves privadas em formato de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="94dc2-159">They contain private keys in plaintext form.</span></span>

 

<span data-ttu-id="94dc2-160">Ao chamar [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), o desenvolvedor pode escolher se deseja criptografar a chave.</span><span class="sxs-lookup"><span data-stu-id="94dc2-160">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="94dc2-161">O **PRIVATEKEYBLOB** será criptografado se o parâmetro *hExpKey* contiver um identificador válido para uma chave de sessão.</span><span class="sxs-lookup"><span data-stu-id="94dc2-161">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="94dc2-162">Tudo menos a parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) do blob é criptografada.</span><span class="sxs-lookup"><span data-stu-id="94dc2-162">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="94dc2-163">Os parâmetros de algoritmo de criptografia e chave de criptografia não são armazenados junto com o BLOB de chave privada.</span><span class="sxs-lookup"><span data-stu-id="94dc2-163">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="94dc2-164">O aplicativo deve gerenciar e armazenar essas informações.</span><span class="sxs-lookup"><span data-stu-id="94dc2-164">The application must manage and store this information.</span></span> <span data-ttu-id="94dc2-165">Se zero for passado para *hExpKey*, a chave privada será exportada sem criptografia.</span><span class="sxs-lookup"><span data-stu-id="94dc2-165">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="94dc2-166">É perigoso exportar chaves privadas sem criptografia porque elas são então vulneráveis à interceptação e ao uso por entidades não autorizadas.</span><span class="sxs-lookup"><span data-stu-id="94dc2-166">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

## <a name="simple-key-blobs"></a><span data-ttu-id="94dc2-167">BLOBs de chave simples</span><span class="sxs-lookup"><span data-stu-id="94dc2-167">Simple Key BLOBs</span></span>

<span data-ttu-id="94dc2-168">[*Blobs de chave simples*](../secgloss/s-gly.md), tipo **SIMPLEBLOB**, são usados para armazenar e transportar chaves de sessão fora de um CSP.</span><span class="sxs-lookup"><span data-stu-id="94dc2-168">[*Simple key BLOBs*](../secgloss/s-gly.md), type **SIMPLEBLOB**, are used to store and transport session keys outside a CSP.</span></span> <span data-ttu-id="94dc2-169">Os BLOBs de chave simples do provedor base são sempre criptografados com uma [*chave pública de troca de chaves*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="94dc2-169">Base provider simple key BLOBs are always encrypted with a [*key exchange public key*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="94dc2-170">O membro **pbData** do **SIMPLEBLOB** é uma sequência de bytes no formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="94dc2-170">The **pbData** member of the **SIMPLEBLOB** is a sequence of bytes in the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

<span data-ttu-id="94dc2-171">A tabela a seguir descreve cada componente do membro **pbData** do **SIMPLEBLOB**.</span><span class="sxs-lookup"><span data-stu-id="94dc2-171">The following table describes each component of the **pbData** member of the **SIMPLEBLOB**.</span></span>



| <span data-ttu-id="94dc2-172">Campo</span><span class="sxs-lookup"><span data-stu-id="94dc2-172">Field</span></span>          | <span data-ttu-id="94dc2-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="94dc2-173">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94dc2-174">algid</span><span class="sxs-lookup"><span data-stu-id="94dc2-174">algid</span></span>          | <span data-ttu-id="94dc2-175">Uma estrutura de [**\_ ID alg**](alg-id.md) que especifica o algoritmo de criptografia usado para criptografar os dados de chave de sessão.</span><span class="sxs-lookup"><span data-stu-id="94dc2-175">An [**ALG\_ID**](alg-id.md) structure that specifies the encryption algorithm used to encrypt the session key data.</span></span> <span data-ttu-id="94dc2-176">Normalmente, isso tem um valor de CALG \_ RSA \_ KEYX, que indica que os dados de chave de sessão foram criptografados com uma chave pública de troca de chaves usando o [*algoritmo de chave pública RSA*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="94dc2-176">This typically has a value of CALG\_RSA\_KEYX, which indicates that the session key data was encrypted with a key exchange public key using the [*RSA Public Key algorithm*](../secgloss/r-gly.md).</span></span>                                                                                                                           |
| <span data-ttu-id="94dc2-177">EncryptedKey</span><span class="sxs-lookup"><span data-stu-id="94dc2-177">encryptedkey</span></span>   | <span data-ttu-id="94dc2-178">Uma sequência de **bytes** que representa os dados de chave de sessão criptografados na forma de um \# bloco de criptografia PKCS 1, tipo 2.</span><span class="sxs-lookup"><span data-stu-id="94dc2-178">A **BYTE** sequence that represents the encrypted session key data in the form of a PKCS \#1, type 2 encryption block.</span></span> <span data-ttu-id="94dc2-179">Para obter informações sobre esse formato de dados, consulte os padrões de criptografia de chave pública (PKCS) \# 1, publicados pelo RSA Data Security, Inc. Esses dados são sempre do mesmo tamanho que o módulo da chave pública.</span><span class="sxs-lookup"><span data-stu-id="94dc2-179">For information about this data format, see the Public Key Cryptography Standards (PKCS) \#1, published by RSA Data Security, Inc. This data is always the same size as the modulus of the public key.</span></span> <span data-ttu-id="94dc2-180">Por exemplo, as chaves públicas geradas pelo provedor de base RSA da Microsoft podem ter 512 bits (64 bytes) de comprimento, de modo que os dados de chave de sessão criptografados também são sempre 512 bits (64 bytes).</span><span class="sxs-lookup"><span data-stu-id="94dc2-180">For example, public keys generated by the Microsoft RSA Base Provider can be 512 bits (64 bytes) in length, so the encrypted session key data is also always 512 bits (64 bytes).</span></span><br/> |
| <span data-ttu-id="94dc2-181">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="94dc2-181">publickeystruc</span></span> | <span data-ttu-id="94dc2-182">Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="94dc2-182">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

 

 
