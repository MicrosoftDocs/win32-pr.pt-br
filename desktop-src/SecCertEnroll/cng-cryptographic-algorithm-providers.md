---
description: 'Ao contrário da CryptoAPI (API de criptografia), a CNG (API de criptografia: próxima geração) separa os provedores criptográficos dos principais provedores de armazenamento.'
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: Provedores de algoritmos criptográficos CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc64926236157e581ce6406d95681bd8d4add14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748661"
---
# <a name="cng-cryptographic-algorithm-providers"></a><span data-ttu-id="0a063-103">Provedores de algoritmos criptográficos CNG</span><span class="sxs-lookup"><span data-stu-id="0a063-103">CNG Cryptographic Algorithm Providers</span></span>

<span data-ttu-id="0a063-104">Ao contrário da CryptoAPI (API de criptografia), a CNG (API de criptografia: próxima geração) separa os provedores criptográficos dos principais provedores de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0a063-104">Unlike Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separates cryptographic providers from key storage providers.</span></span> <span data-ttu-id="0a063-105">As operações básicas do algoritmo de criptografia, como hash e assinatura, são chamadas de operações primitivas ou simplesmente primitivos.</span><span class="sxs-lookup"><span data-stu-id="0a063-105">Basic cryptographic algorithm operations such as hashing and signing are called primitive operations or simply primitives.</span></span> <span data-ttu-id="0a063-106">A CNG inclui um provedor que implementa os seguintes algoritmos.</span><span class="sxs-lookup"><span data-stu-id="0a063-106">CNG includes a provider that implements the following algorithms.</span></span>

-   [<span data-ttu-id="0a063-107">Algoritmos simétricos</span><span class="sxs-lookup"><span data-stu-id="0a063-107">Symmetric Algorithms</span></span>](#symmetric-algorithms)
-   [<span data-ttu-id="0a063-108">Algoritmos assimétricos</span><span class="sxs-lookup"><span data-stu-id="0a063-108">Asymmetric Algorithms</span></span>](#asymmetric-algorithms)
-   [<span data-ttu-id="0a063-109">Algoritmos de hash</span><span class="sxs-lookup"><span data-stu-id="0a063-109">Hashing Algorithms</span></span>](#hashing-algorithms)
-   [<span data-ttu-id="0a063-110">Algoritmos de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="0a063-110">Key Exchange Algorithms</span></span>](#key-exchange-algorithms)
-   [<span data-ttu-id="0a063-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a063-111">Related topics</span></span>](#related-topics)

## <a name="symmetric-algorithms"></a><span data-ttu-id="0a063-112">Algoritmos simétricos</span><span class="sxs-lookup"><span data-stu-id="0a063-112">Symmetric Algorithms</span></span>



| <span data-ttu-id="0a063-113">Nome</span><span class="sxs-lookup"><span data-stu-id="0a063-113">Name</span></span>                                   | <span data-ttu-id="0a063-114">Modos com suporte</span><span class="sxs-lookup"><span data-stu-id="0a063-114">Supported modes</span></span>                                                                                                                                                                                                 | <span data-ttu-id="0a063-115">Tamanho da chave em bits (padrão/mín/máx.)</span><span class="sxs-lookup"><span data-stu-id="0a063-115">Key size in bits (Default/Min/Max)</span></span> |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="0a063-116">AES (criptografia AES)</span><span class="sxs-lookup"><span data-stu-id="0a063-116">Advanced Encryption Standard (AES)</span></span>     | <span data-ttu-id="0a063-117">ECB, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, encapsulamento de chave AES, XTS</span><span class="sxs-lookup"><span data-stu-id="0a063-117">ECB, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, AES Key Wrap, XTS</span></span><br/> <span data-ttu-id="0a063-118">**Windows 8:** O suporte para os modos CFB128 e CMAC começa.</span><span class="sxs-lookup"><span data-stu-id="0a063-118">**Windows 8:** Support for the CFB128 and CMAC modes begins.</span></span><br/> <span data-ttu-id="0a063-119">**Windows 10:** O suporte para o modo XTS-AES é iniciado.</span><span class="sxs-lookup"><span data-stu-id="0a063-119">**Windows 10:** Support for XTS-AES mode begins.</span></span><br/> | <span data-ttu-id="0a063-120">128/192/256</span><span class="sxs-lookup"><span data-stu-id="0a063-120">128/192/256</span></span>                        |
| <span data-ttu-id="0a063-121">DES (padrão de criptografia de dados)</span><span class="sxs-lookup"><span data-stu-id="0a063-121">Data Encryption Standard (DES)</span></span>         | <span data-ttu-id="0a063-122">ECB, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="0a063-122">ECB, CBC, CFB8, CFB64</span></span><br/> <span data-ttu-id="0a063-123">**Windows 8:** O suporte para o modo CFB64 começa.</span><span class="sxs-lookup"><span data-stu-id="0a063-123">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                   | <span data-ttu-id="0a063-124">56/56/56</span><span class="sxs-lookup"><span data-stu-id="0a063-124">56/56/56</span></span>                           |
| <span data-ttu-id="0a063-125">XORed padrão de criptografia de dados (DESX)</span><span class="sxs-lookup"><span data-stu-id="0a063-125">Data Encryption Standard XORed(DESX)</span></span>   | <span data-ttu-id="0a063-126">ECB, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="0a063-126">ECB, CBC, CFB8, CFB64</span></span> <br/> <span data-ttu-id="0a063-127">**Windows 8:** O suporte para o modo CFB64 começa.</span><span class="sxs-lookup"><span data-stu-id="0a063-127">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                  | <span data-ttu-id="0a063-128">192/192/192</span><span class="sxs-lookup"><span data-stu-id="0a063-128">192/192/192</span></span>                        |
| <span data-ttu-id="0a063-129">3DES (padrão de criptografia de dados triplo)</span><span class="sxs-lookup"><span data-stu-id="0a063-129">Triple Data Encryption Standard (3DES)</span></span> | <span data-ttu-id="0a063-130">ECB, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="0a063-130">ECB, CBC, CFB8, CFB64</span></span> <br/> <span data-ttu-id="0a063-131">**Windows 8:** O suporte para o modo CFB64 começa.</span><span class="sxs-lookup"><span data-stu-id="0a063-131">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                  | <span data-ttu-id="0a063-132">112/168</span><span class="sxs-lookup"><span data-stu-id="0a063-132">112/168</span></span>                            |
| <span data-ttu-id="0a063-133">RSA Data Security 2 (RC2)</span><span class="sxs-lookup"><span data-stu-id="0a063-133">RSA Data Security 2 (RC2)</span></span>              | <span data-ttu-id="0a063-134">Há suporte para os modos ECB, CBC, CFB8, CFB64.</span><span class="sxs-lookup"><span data-stu-id="0a063-134">ECB, CBC, CFB8, CFB64 modes are supported.</span></span><br/> <span data-ttu-id="0a063-135">**Windows 8:** O suporte para o modo CFB64 começa.</span><span class="sxs-lookup"><span data-stu-id="0a063-135">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                              | <span data-ttu-id="0a063-136">16 a 128 em incrementos de 8 bits</span><span class="sxs-lookup"><span data-stu-id="0a063-136">16 to 128 in 8 bit increments</span></span>      |
| <span data-ttu-id="0a063-137">RC4 (RSA Data Security 4)</span><span class="sxs-lookup"><span data-stu-id="0a063-137">RSA Data Security 4 (RC4)</span></span>              |                                                                                                                                                                                                                 | <span data-ttu-id="0a063-138">8 a 512, em incrementos de 8 bits</span><span class="sxs-lookup"><span data-stu-id="0a063-138">8 to 512, in 8-bit increments</span></span>      |



 

## <a name="asymmetric-algorithms"></a><span data-ttu-id="0a063-139">Algoritmos assimétricos</span><span class="sxs-lookup"><span data-stu-id="0a063-139">Asymmetric Algorithms</span></span>



| <span data-ttu-id="0a063-140">Nome</span><span class="sxs-lookup"><span data-stu-id="0a063-140">Name</span></span>                              | <span data-ttu-id="0a063-141">Observações</span><span class="sxs-lookup"><span data-stu-id="0a063-141">Notes</span></span>                                                                                                                                                                             | <span data-ttu-id="0a063-142">Tamanho da chave em bits (padrão/mín/máx.)</span><span class="sxs-lookup"><span data-stu-id="0a063-142">Key size in bits (Default/Min/Max)</span></span>                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a063-143">Algoritmo de assinatura digital (DSA)</span><span class="sxs-lookup"><span data-stu-id="0a063-143">Digital Signature Algorithm (DSA)</span></span> | <span data-ttu-id="0a063-144">A implementação está de acordo com o FIPS 186-3 para os tamanhos de chave entre 1024 e 3072 bits.</span><span class="sxs-lookup"><span data-stu-id="0a063-144">Implementation conforms to FIPS 186-3 for key sizes between 1024 and 3072 bits.</span></span> <br/> <span data-ttu-id="0a063-145">A implementação está de acordo com o FIPS 186-2 para os tamanhos de chave de 512 a 1024 bits.</span><span class="sxs-lookup"><span data-stu-id="0a063-145">Implementation conforms to FIPS 186-2 for key sizes from 512 to 1024 bits.</span></span><br/> | <span data-ttu-id="0a063-146">512 a 3072, em incrementos de bits 64</span><span class="sxs-lookup"><span data-stu-id="0a063-146">512 to 3072, in 64-bit increments</span></span><br/> <span data-ttu-id="0a063-147">**Windows 8:** O suporte para a chave de 3072 bits começa.</span><span class="sxs-lookup"><span data-stu-id="0a063-147">**Windows 8:** Support for the a 3072 bit key begins.</span></span><br/> |
| <span data-ttu-id="0a063-148">RSA</span><span class="sxs-lookup"><span data-stu-id="0a063-148">RSA</span></span>                               | <span data-ttu-id="0a063-149">Inclui algoritmos RSA que usam PKCS1, codificação ou preenchimento da OAEP (preenchimento de criptografia assimétrica) ideal ou preenchimento de texto não criptografado do PSS (esquema de assinatura probabilística)</span><span class="sxs-lookup"><span data-stu-id="0a063-149">Includes RSA algorithms that use PKCS1, Optimal Asymmetric Encryption Padding (OAEP) encoding or padding, or Probabilistic Signature Scheme (PSS) plaintext padding</span></span>               | <span data-ttu-id="0a063-150">512 a 16384, em incrementos de bits 64</span><span class="sxs-lookup"><span data-stu-id="0a063-150">512 to 16384, in 64-bit increments</span></span>                                                                            |



 

## <a name="hashing-algorithms"></a><span data-ttu-id="0a063-151">Algoritmos de hash</span><span class="sxs-lookup"><span data-stu-id="0a063-151">Hashing Algorithms</span></span>



| <span data-ttu-id="0a063-152">Nome</span><span class="sxs-lookup"><span data-stu-id="0a063-152">Name</span></span>                               | <span data-ttu-id="0a063-153">Observações</span><span class="sxs-lookup"><span data-stu-id="0a063-153">Notes</span></span>               | <span data-ttu-id="0a063-154">Tamanho da chave em bits (padrão/mín/máx.)</span><span class="sxs-lookup"><span data-stu-id="0a063-154">Key size in bits (Default/Min/Max)</span></span> |
|------------------------------------|---------------------|------------------------------------|
| <span data-ttu-id="0a063-155">Secure Hash Algorithm 1 (SHA1)</span><span class="sxs-lookup"><span data-stu-id="0a063-155">Secure Hash Algorithm 1 (SHA1)</span></span>     | <span data-ttu-id="0a063-156">Inclui HmacSha1</span><span class="sxs-lookup"><span data-stu-id="0a063-156">Includes HmacSha1</span></span>   | <span data-ttu-id="0a063-157">160/160/160</span><span class="sxs-lookup"><span data-stu-id="0a063-157">160/160/160</span></span>                        |
| <span data-ttu-id="0a063-158">Algoritmo de hash seguro 256 (SHA256)</span><span class="sxs-lookup"><span data-stu-id="0a063-158">Secure Hash Algorithm 256 (SHA256)</span></span> | <span data-ttu-id="0a063-159">Inclui HmacSha256</span><span class="sxs-lookup"><span data-stu-id="0a063-159">Includes HmacSha256</span></span> | <span data-ttu-id="0a063-160">256/256/256</span><span class="sxs-lookup"><span data-stu-id="0a063-160">256/256/256</span></span>                        |
| <span data-ttu-id="0a063-161">Algoritmo de hash seguro 384 (SHA384)</span><span class="sxs-lookup"><span data-stu-id="0a063-161">Secure Hash Algorithm 384 (SHA384)</span></span> | <span data-ttu-id="0a063-162">Inclui HmacSha384</span><span class="sxs-lookup"><span data-stu-id="0a063-162">Includes HmacSha384</span></span> | <span data-ttu-id="0a063-163">384/384/384</span><span class="sxs-lookup"><span data-stu-id="0a063-163">384/384/384</span></span>                        |
| <span data-ttu-id="0a063-164">Algoritmo de hash seguro 512 (SHA512)</span><span class="sxs-lookup"><span data-stu-id="0a063-164">Secure Hash Algorithm 512 (SHA512)</span></span> | <span data-ttu-id="0a063-165">Inclui HmacSha512</span><span class="sxs-lookup"><span data-stu-id="0a063-165">Includes HmacSha512</span></span> | <span data-ttu-id="0a063-166">512/512/512</span><span class="sxs-lookup"><span data-stu-id="0a063-166">512/512/512</span></span>                        |
| <span data-ttu-id="0a063-167">Mensagem Digest 2 (MD2)</span><span class="sxs-lookup"><span data-stu-id="0a063-167">Message Digest 2 (MD2)</span></span>             | <span data-ttu-id="0a063-168">Inclui HmacMd2</span><span class="sxs-lookup"><span data-stu-id="0a063-168">Includes HmacMd2</span></span>    | <span data-ttu-id="0a063-169">128/128/128</span><span class="sxs-lookup"><span data-stu-id="0a063-169">128/128/128</span></span>                        |
| <span data-ttu-id="0a063-170">Mensagem Digest 4 (MD4)</span><span class="sxs-lookup"><span data-stu-id="0a063-170">Message Digest 4 (MD4)</span></span>             | <span data-ttu-id="0a063-171">Inclui HmacMd4</span><span class="sxs-lookup"><span data-stu-id="0a063-171">Includes HmacMd4</span></span>    | <span data-ttu-id="0a063-172">128/128/128</span><span class="sxs-lookup"><span data-stu-id="0a063-172">128/128/128</span></span>                        |
| <span data-ttu-id="0a063-173">Message Digest 5 (MD5)</span><span class="sxs-lookup"><span data-stu-id="0a063-173">Message Digest 5 (MD5)</span></span>             | <span data-ttu-id="0a063-174">Inclui HmacMd5</span><span class="sxs-lookup"><span data-stu-id="0a063-174">Includes HmacMd5</span></span>    | <span data-ttu-id="0a063-175">128/128/128</span><span class="sxs-lookup"><span data-stu-id="0a063-175">128/128/128</span></span>                        |



 

## <a name="key-exchange-algorithms"></a><span data-ttu-id="0a063-176">Algoritmos de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="0a063-176">Key Exchange Algorithms</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a063-177">Nome do algoritmo</span><span class="sxs-lookup"><span data-stu-id="0a063-177">Algorithm name</span></span></th>
<th><span data-ttu-id="0a063-178">Observações</span><span class="sxs-lookup"><span data-stu-id="0a063-178">Notes</span></span></th>
<th><span data-ttu-id="0a063-179">Tamanho da chave em bits (padrão/mín/máx.)</span><span class="sxs-lookup"><span data-stu-id="0a063-179">Key size in bits (Default/Min/Max)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a063-180">Algoritmo de troca de chave Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="0a063-180">Diffie-Hellman Key Exchange Algorithm</span></span></td>

<td><span data-ttu-id="0a063-181">512 a 4096, em incrementos de bits 64</span><span class="sxs-lookup"><span data-stu-id="0a063-181">512 to 4096, in 64-bit increments</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a063-182">Diffie-Hellman de curva elíptica (ECDH)</span><span class="sxs-lookup"><span data-stu-id="0a063-182">Elliptic Curve Diffie-Hellman (ECDH)</span></span></td>
<td><span data-ttu-id="0a063-183">Inclui curvas que usam chaves públicas 256, 384 e 521 bits, conforme especificado em SP800-56A.</span><span class="sxs-lookup"><span data-stu-id="0a063-183">Includes curves that use 256, 384 and 521 bit public keys as specified in SP800-56A.</span></span></td>
<td><span data-ttu-id="0a063-184">256/384/521</span><span class="sxs-lookup"><span data-stu-id="0a063-184">256/384/521</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a063-185">ECDSA (algoritmo de assinatura digital de curva elíptica)</span><span class="sxs-lookup"><span data-stu-id="0a063-185">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span></td>
<td><span data-ttu-id="0a063-186">Inclui curvas que usam chaves públicas 256, 384 e 521 bits, conforme especificado no FIPS 186-3.</span><span class="sxs-lookup"><span data-stu-id="0a063-186">Includes curves that use 256, 384 and 521 bit public keys as specified in FIPS 186-3.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="0a063-187">Para exibir todas as curvas elípticas nomeadas, use <strong>certutil displayEccCurve</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a063-187">To display all named elliptic curves, use <strong>certutil  displayEccCurve</strong>.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="0a063-188">256/384/521</span><span class="sxs-lookup"><span data-stu-id="0a063-188">256/384/521</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="0a063-189">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a063-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a063-190">**Identificadores de algoritmo CNG**</span><span class="sxs-lookup"><span data-stu-id="0a063-190">**CNG Algorithm Identifiers**</span></span>](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[<span data-ttu-id="0a063-191">Funções primitivas de criptografia CNG</span><span class="sxs-lookup"><span data-stu-id="0a063-191">CNG Cryptographic Primitive Functions</span></span>](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[<span data-ttu-id="0a063-192">Noções básicas sobre provedores criptográficos</span><span class="sxs-lookup"><span data-stu-id="0a063-192">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 

