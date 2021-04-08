---
description: Os BLOBs são usados com o provedor RSA/Schannel para exportar chaves de e importar chaves para o CSP (provedor de serviços de criptografia).
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: BLOBs de chave RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea26a98e9c2925442166eb28245ebc471b1749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827245"
---
# <a name="rsaschannel-key-blobs"></a><span data-ttu-id="70ae3-103">BLOBs de chave RSA/Schannel</span><span class="sxs-lookup"><span data-stu-id="70ae3-103">RSA/Schannel Key BLOBs</span></span>

<span data-ttu-id="70ae3-104">Os [*BLOBs*](../secgloss/b-gly.md) são usados com [](../secgloss/r-gly.md)o provedor de / [*Schannel*](../secgloss/s-gly.md) RSA para exportar chaves de e importar chaves para o CSP (provedor de [*serviços de criptografia*](../secgloss/c-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="70ae3-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="70ae3-105">BLOBs de chave pública</span><span class="sxs-lookup"><span data-stu-id="70ae3-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="70ae3-106">BLOBs de chave privada</span><span class="sxs-lookup"><span data-stu-id="70ae3-106">Private Key BLOBs</span></span>](#private-key-blobs)
-   [<span data-ttu-id="70ae3-107">BLOBs de chave simples</span><span class="sxs-lookup"><span data-stu-id="70ae3-107">Simple Key BLOBs</span></span>](#simple-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="70ae3-108">BLOBs de chave pública</span><span class="sxs-lookup"><span data-stu-id="70ae3-108">Public Key BLOBs</span></span>

<span data-ttu-id="70ae3-109">Os [*blobs de chave pública*](../secgloss/p-gly.md), digite **PublicKeyBlob**, são usados para armazenar [*chaves públicas*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="70ae3-109">[*Public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to store [*public keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="70ae3-110">Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="70ae3-110">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

<span data-ttu-id="70ae3-111">A tabela a seguir descreve cada componente de chave pública.</span><span class="sxs-lookup"><span data-stu-id="70ae3-111">The following table describes each public key component.</span></span> <span data-ttu-id="70ae3-112">Todos os valores estão no formato [*little-endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="70ae3-112">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="70ae3-113">Campo</span><span class="sxs-lookup"><span data-stu-id="70ae3-113">Field</span></span>          | <span data-ttu-id="70ae3-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="70ae3-114">Description</span></span>                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70ae3-115">módulo</span><span class="sxs-lookup"><span data-stu-id="70ae3-115">modulus</span></span>        | <span data-ttu-id="70ae3-116">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="70ae3-116">A **BYTE** sequence.</span></span> <span data-ttu-id="70ae3-117">Os dados do módulo de chave pública estão localizados diretamente após a estrutura **RSAPUBKEY** .</span><span class="sxs-lookup"><span data-stu-id="70ae3-117">The public key modulus data is located directly after the **RSAPUBKEY** structure.</span></span> <span data-ttu-id="70ae3-118">O comprimento desses dados varia, dependendo do comprimento da chave pública.</span><span class="sxs-lookup"><span data-stu-id="70ae3-118">The length of this data varies, depending on the length of the public key.</span></span> <span data-ttu-id="70ae3-119">O número de bytes pode ser determinado pela divisão do valor do membro **bitlen** de **RSAPUBKEY** por oito.</span><span class="sxs-lookup"><span data-stu-id="70ae3-119">The number of bytes can be determined by dividing the value of the **bitlen** member of **RSAPUBKEY** by eight.</span></span> |
| <span data-ttu-id="70ae3-120">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="70ae3-120">publickeystruc</span></span> | <span data-ttu-id="70ae3-121">Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="70ae3-121">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="70ae3-122">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="70ae3-122">rsapubkey</span></span>      | <span data-ttu-id="70ae3-123">Uma estrutura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="70ae3-123">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="70ae3-124">O membro **mágico** deve ser definido como 0x31415352.</span><span class="sxs-lookup"><span data-stu-id="70ae3-124">The **magic** member must be set to 0x31415352.</span></span> <span data-ttu-id="70ae3-125">Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de RSA1.</span><span class="sxs-lookup"><span data-stu-id="70ae3-125">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA1.</span></span>                                                                                      |



 

> [!Note]  
> <span data-ttu-id="70ae3-126">Os BLOBs de chave pública não são criptografados.</span><span class="sxs-lookup"><span data-stu-id="70ae3-126">Public key BLOBs are not encrypted.</span></span> <span data-ttu-id="70ae3-127">Elas contêm chaves públicas em formato de [*texto sem formatação*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="70ae3-127">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="70ae3-128">BLOBs de chave privada</span><span class="sxs-lookup"><span data-stu-id="70ae3-128">Private Key BLOBs</span></span>

<span data-ttu-id="70ae3-129">Os [*blobs de chave privada*](../secgloss/p-gly.md), o tipo **PRIVATEKEYBLOB**, são usados para armazenar [*pares de chaves pública/privada*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="70ae3-129">[*Private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store [*public/private key pairs*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="70ae3-130">Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="70ae3-130">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
BYTE            prime1[rsapubkey.bitlen/16];
BYTE            prime2[rsapubkey.bitlen/16];
BYTE            exponent1[rsapubkey.bitlen/16];
BYTE            exponent2[rsapubkey.bitlen/16];
BYTE            coefficient[rsapubkey.bitlen/16];
BYTE            privateExponent[rsapubkey.bitlen/8];
```

<span data-ttu-id="70ae3-131">Se o [*blob de chave*](../secgloss/k-gly.md) for criptografado, tudo menos a parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) do blob será criptografada.</span><span class="sxs-lookup"><span data-stu-id="70ae3-131">If the [*key BLOB*](../secgloss/k-gly.md) is encrypted, then everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="70ae3-132">Os parâmetros de algoritmo de criptografia e chave de criptografia não são armazenados junto com o BLOB de chave privada.</span><span class="sxs-lookup"><span data-stu-id="70ae3-132">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="70ae3-133">É responsabilidade do aplicativo gerenciar essas informações.</span><span class="sxs-lookup"><span data-stu-id="70ae3-133">It is the responsibility of the application to manage this information.</span></span>

 

<span data-ttu-id="70ae3-134">A tabela a seguir descreve cada componente de BLOB de chave privada.</span><span class="sxs-lookup"><span data-stu-id="70ae3-134">The following table describes each private key BLOB component.</span></span>

> [!Note]  
> <span data-ttu-id="70ae3-135">Esses campos correspondem aos campos descritos na seção 7,2 de [*padrões de criptografia de chave pública*](../secgloss/p-gly.md) (PKCS) \# 1 com pequenas diferenças.</span><span class="sxs-lookup"><span data-stu-id="70ae3-135">These fields correspond to the fields described in section 7.2 of [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1 with minor differences.</span></span>

 



| <span data-ttu-id="70ae3-136">Campo</span><span class="sxs-lookup"><span data-stu-id="70ae3-136">Field</span></span>           | <span data-ttu-id="70ae3-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="70ae3-137">Description</span></span>                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70ae3-138">exponent1</span><span class="sxs-lookup"><span data-stu-id="70ae3-138">exponent1</span></span>       | <span data-ttu-id="70ae3-139">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="70ae3-139">A **BYTE** sequence.</span></span> <span data-ttu-id="70ae3-140">O primeiro expoente.</span><span class="sxs-lookup"><span data-stu-id="70ae3-140">The first exponent.</span></span> <span data-ttu-id="70ae3-141">Isso tem um valor numérico de d mod (p – 1).</span><span class="sxs-lookup"><span data-stu-id="70ae3-141">This has a numeric value of d mod (p – 1).</span></span>                                                                                                                           |
| <span data-ttu-id="70ae3-142">exponent2</span><span class="sxs-lookup"><span data-stu-id="70ae3-142">exponent2</span></span>       | <span data-ttu-id="70ae3-143">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="70ae3-143">A **BYTE** sequence.</span></span> <span data-ttu-id="70ae3-144">O segundo expoente.</span><span class="sxs-lookup"><span data-stu-id="70ae3-144">The second exponent.</span></span> <span data-ttu-id="70ae3-145">Isso tem um valor numérico de d mod (q – 1).</span><span class="sxs-lookup"><span data-stu-id="70ae3-145">This has a numeric value of d mod (q – 1).</span></span>                                                                                                                          |
| <span data-ttu-id="70ae3-146">cujo</span><span class="sxs-lookup"><span data-stu-id="70ae3-146">coefficient</span></span>     | <span data-ttu-id="70ae3-147">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="70ae3-147">A **BYTE** sequence.</span></span> <span data-ttu-id="70ae3-148">Cujo.</span><span class="sxs-lookup"><span data-stu-id="70ae3-148">Coefficient.</span></span> <span data-ttu-id="70ae3-149">Isso tem um valor numérico de (inverso de q) mod p.</span><span class="sxs-lookup"><span data-stu-id="70ae3-149">This has a numeric value of (inverse of q) mod p.</span></span>                                                                                                                           |
| <span data-ttu-id="70ae3-150">Modulus</span><span class="sxs-lookup"><span data-stu-id="70ae3-150">Modulus</span></span>         | <span data-ttu-id="70ae3-151">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="70ae3-151">A **BYTE** sequence.</span></span> <span data-ttu-id="70ae3-152">O módulo.</span><span class="sxs-lookup"><span data-stu-id="70ae3-152">The modulus.</span></span> <span data-ttu-id="70ae3-153">Isso tem uma cadeia de caracteres que contém *Prime1* \* *Prime2*.</span><span class="sxs-lookup"><span data-stu-id="70ae3-153">This has a string that contains *Prime1* \* *Prime2*.</span></span> <span data-ttu-id="70ae3-154">Geralmente é conhecido como n.</span><span class="sxs-lookup"><span data-stu-id="70ae3-154">It is often known as n.</span></span>                                                                                               |
| <span data-ttu-id="70ae3-155">prime1</span><span class="sxs-lookup"><span data-stu-id="70ae3-155">prime1</span></span>          | <span data-ttu-id="70ae3-156">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="70ae3-156">A **BYTE** sequence.</span></span> <span data-ttu-id="70ae3-157">Número principal 1, geralmente conhecido como p.</span><span class="sxs-lookup"><span data-stu-id="70ae3-157">Prime number 1, often known as p.</span></span>                                                                                                                                                        |
| <span data-ttu-id="70ae3-158">prime2</span><span class="sxs-lookup"><span data-stu-id="70ae3-158">prime2</span></span>          | <span data-ttu-id="70ae3-159">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="70ae3-159">A **BYTE** sequence.</span></span> <span data-ttu-id="70ae3-160">Número principal 2, geralmente conhecido como q.</span><span class="sxs-lookup"><span data-stu-id="70ae3-160">Prime number 2, often known as q.</span></span>                                                                                                                                                        |
| <span data-ttu-id="70ae3-161">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="70ae3-161">publickeystruc</span></span>  | <span data-ttu-id="70ae3-162">Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="70ae3-162">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                         |
| <span data-ttu-id="70ae3-163">privateExponent</span><span class="sxs-lookup"><span data-stu-id="70ae3-163">privateExponent</span></span> | <span data-ttu-id="70ae3-164">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="70ae3-164">A **BYTE** sequence.</span></span> <span data-ttu-id="70ae3-165">O expoente privado, geralmente conhecido como d.</span><span class="sxs-lookup"><span data-stu-id="70ae3-165">The private exponent, often known as d.</span></span>                                                                                                                                                  |
| <span data-ttu-id="70ae3-166">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="70ae3-166">rsapubkey</span></span>       | <span data-ttu-id="70ae3-167">Uma estrutura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="70ae3-167">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="70ae3-168">O membro **mágico** deve ser definido como 0x32415352.</span><span class="sxs-lookup"><span data-stu-id="70ae3-168">The **magic** member must be set to 0x32415352.</span></span> <span data-ttu-id="70ae3-169">Esse valor hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de RSA2.</span><span class="sxs-lookup"><span data-stu-id="70ae3-169">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA2.</span></span> |



 

> [!Note]  
> <span data-ttu-id="70ae3-170">Os BLOBs de chave privada não são criptografados.</span><span class="sxs-lookup"><span data-stu-id="70ae3-170">Private key BLOBs are not encrypted.</span></span> <span data-ttu-id="70ae3-171">Eles contêm chaves privadas em formato de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="70ae3-171">They contain private keys in plaintext form.</span></span>

 

<span data-ttu-id="70ae3-172">Ao chamar [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), o desenvolvedor pode escolher se deseja criptografar a chave.</span><span class="sxs-lookup"><span data-stu-id="70ae3-172">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="70ae3-173">O **PRIVATEKEYBLOB** será criptografado se o parâmetro *hExpKey* contiver um identificador válido para uma chave de sessão.</span><span class="sxs-lookup"><span data-stu-id="70ae3-173">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="70ae3-174">Tudo menos a parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) do blob é criptografada.</span><span class="sxs-lookup"><span data-stu-id="70ae3-174">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="70ae3-175">Os parâmetros de algoritmo de criptografia e chave de criptografia não são armazenados junto com o BLOB de chave privada.</span><span class="sxs-lookup"><span data-stu-id="70ae3-175">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="70ae3-176">O aplicativo deve gerenciar e armazenar essas informações.</span><span class="sxs-lookup"><span data-stu-id="70ae3-176">The application must manage and store this information.</span></span> <span data-ttu-id="70ae3-177">Se zero for passado para *hExpKey*, a chave privada será exportada sem criptografia.</span><span class="sxs-lookup"><span data-stu-id="70ae3-177">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="70ae3-178">É perigoso exportar chaves privadas sem criptografia porque elas são então vulneráveis à interceptação e ao uso por entidades não autorizadas.</span><span class="sxs-lookup"><span data-stu-id="70ae3-178">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

## <a name="simple-key-blobs"></a><span data-ttu-id="70ae3-179">BLOBs de chave simples</span><span class="sxs-lookup"><span data-stu-id="70ae3-179">Simple Key BLOBs</span></span>

<span data-ttu-id="70ae3-180">[*Blobs de chave simples*](../secgloss/s-gly.md), tipo **SIMPLEBLOB**, são usados para armazenar e transportar chaves de sessão.</span><span class="sxs-lookup"><span data-stu-id="70ae3-180">[*Simple key BLOBs*](../secgloss/s-gly.md), type **SIMPLEBLOB**, are used to store and transport session keys.</span></span> <span data-ttu-id="70ae3-181">Eles são sempre criptografados com uma [*chave pública de troca de chaves*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="70ae3-181">These are always encrypted with a [*key exchange public key*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="70ae3-182">Essas chaves são exportadas e importadas como uma sequência de bytes com o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="70ae3-182">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

<span data-ttu-id="70ae3-183">A tabela a seguir descreve cada componente de BLOB simples.</span><span class="sxs-lookup"><span data-stu-id="70ae3-183">The following table describes each simple BLOB component.</span></span>



| <span data-ttu-id="70ae3-184">Campo</span><span class="sxs-lookup"><span data-stu-id="70ae3-184">Field</span></span>          | <span data-ttu-id="70ae3-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="70ae3-185">Description</span></span>                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70ae3-186">algid</span><span class="sxs-lookup"><span data-stu-id="70ae3-186">algid</span></span>          | <span data-ttu-id="70ae3-187">Uma estrutura de [**\_ ID alg**](alg-id.md) .</span><span class="sxs-lookup"><span data-stu-id="70ae3-187">An [**ALG\_ID**](alg-id.md) structure.</span></span> <span data-ttu-id="70ae3-188">Isso normalmente especifica o \_ algoritmo CALG RSA \_ KEYX, que indica que os dados de chave de sessão foram criptografados com uma chave pública de troca de chaves, usando o [*algoritmo de chave pública RSA*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="70ae3-188">This typically specifies the CALG\_RSA\_KEYX algorithm, which indicates that the session key data was encrypted with a key exchange public key, using the [*RSA Public Key algorithm*](../secgloss/r-gly.md).</span></span> |
| <span data-ttu-id="70ae3-189">EncryptedKey</span><span class="sxs-lookup"><span data-stu-id="70ae3-189">encryptedkey</span></span>   | <span data-ttu-id="70ae3-190">Uma sequência de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="70ae3-190">A **BYTE** sequence.</span></span> <span data-ttu-id="70ae3-191">Os dados de chave de sessão criptografada estão na forma de um \# bloco de criptografia PKCS 1, tipo 2.</span><span class="sxs-lookup"><span data-stu-id="70ae3-191">The encrypted session key data is in the form of a PKCS \#1, type 2 encryption block.</span></span> <span data-ttu-id="70ae3-192">Para obter informações sobre esse formato de dados, consulte os padrões de criptografia de chave pública (PKCS), publicados pelo RSA Data Security, Inc.</span><span class="sxs-lookup"><span data-stu-id="70ae3-192">For information about this data format, see the Public Key Cryptography Standards (PKCS), published by RSA Data Security, Inc.</span></span>                                                                                     |
| <span data-ttu-id="70ae3-193">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="70ae3-193">publickeystruc</span></span> | <span data-ttu-id="70ae3-194">Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="70ae3-194">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="70ae3-195">Esses dados são sempre do mesmo tamanho que o módulo da chave pública.</span><span class="sxs-lookup"><span data-stu-id="70ae3-195">This data is always the same size as the modulus of the public key.</span></span> <span data-ttu-id="70ae3-196">Por exemplo, as chaves públicas geradas pelo provedor Microsoft Base Cryptographic são sempre 512 bits (64 bytes), portanto, os dados de chave de sessão criptografados também são sempre 64 bytes.</span><span class="sxs-lookup"><span data-stu-id="70ae3-196">For example, public keys generated by the Microsoft Base Cryptographic Provider are always 512 bits (64 bytes) in length, so the encrypted session key data is also always 64 bytes.</span></span>

 

 
