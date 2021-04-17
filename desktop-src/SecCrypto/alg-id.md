---
description: Especifica um identificador de algoritmo.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab1eb6dc262faae76d38f2b96c9e6191a313390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762909"
---
# <a name="alg_id"></a><span data-ttu-id="542ff-103">ALG_ID</span><span class="sxs-lookup"><span data-stu-id="542ff-103">ALG_ID</span></span>

<span data-ttu-id="542ff-104">O tipo de dados **ALG_ID** especifica um identificador de algoritmo.</span><span class="sxs-lookup"><span data-stu-id="542ff-104">The **ALG_ID** data type specifies an algorithm identifier.</span></span> <span data-ttu-id="542ff-105">Os parâmetros desse tipo de dados são passados para a maioria das funções no CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="542ff-105">Parameters of this data type are passed to most of the functions in CryptoAPI.</span></span>


```C++
typedef unsigned int ALG_ID;
```



<span data-ttu-id="542ff-106">A tabela a seguir lista os identificadores de algoritmo que estão definidos no momento.</span><span class="sxs-lookup"><span data-stu-id="542ff-106">The following table lists the algorithm identifiers that are currently defined.</span></span> <span data-ttu-id="542ff-107">Os autores de CSPs ( [*provedores de serviços de criptografia*](../secgloss/c-gly.md) ) personalizados podem definir novos valores.</span><span class="sxs-lookup"><span data-stu-id="542ff-107">Authors of custom [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs) can define new values.</span></span> <span data-ttu-id="542ff-108">Além disso, o **ALG_ID** usado por CSPs personalizados para as principais especificações **AT_KEYEXCHANGE** e **AT_SIGNATURE** são dependentes do provedor.</span><span class="sxs-lookup"><span data-stu-id="542ff-108">Also, the **ALG_ID** used by custom CSPs for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are provider dependent.</span></span> <span data-ttu-id="542ff-109">Os mapeamentos atuais seguem a tabela.</span><span class="sxs-lookup"><span data-stu-id="542ff-109">Current mappings follow the table.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="542ff-110">Identificador</span><span class="sxs-lookup"><span data-stu-id="542ff-110">Identifier</span></span></th>
<th><span data-ttu-id="542ff-111">Valor</span><span class="sxs-lookup"><span data-stu-id="542ff-111">Value</span></span></th>
<th><span data-ttu-id="542ff-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="542ff-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="542ff-113">CALG_3DES</span><span class="sxs-lookup"><span data-stu-id="542ff-113">CALG_3DES</span></span></td>
<td><span data-ttu-id="542ff-114">0x00006603</span><span class="sxs-lookup"><span data-stu-id="542ff-114">0x00006603</span></span></td>
<td><span data-ttu-id="542ff-115">Algoritmo de criptografia <a href="/windows/desktop/SecGloss/t-gly"><em>Triple DES</em></a> .</span><span class="sxs-lookup"><span data-stu-id="542ff-115"><a href="/windows/desktop/SecGloss/t-gly"><em>Triple DES</em></a> encryption algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-116">CALG_3DES_112</span><span class="sxs-lookup"><span data-stu-id="542ff-116">CALG_3DES_112</span></span></td>
<td><span data-ttu-id="542ff-117">0x00006609</span><span class="sxs-lookup"><span data-stu-id="542ff-117">0x00006609</span></span></td>
<td><span data-ttu-id="542ff-118">Criptografia <a href="/windows/desktop/SecGloss/t-gly"><em>Triple DES</em></a> de duas chaves com comprimento de chave efetivo igual a 112 bits.</span><span class="sxs-lookup"><span data-stu-id="542ff-118">Two-key <a href="/windows/desktop/SecGloss/t-gly"><em>triple DES</em></a> encryption with effective key length equal to 112 bits.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-119">CALG_AES</span><span class="sxs-lookup"><span data-stu-id="542ff-119">CALG_AES</span></span></td>
<td><span data-ttu-id="542ff-120">0x00006611</span><span class="sxs-lookup"><span data-stu-id="542ff-120">0x00006611</span></span></td>
<td><span data-ttu-id="542ff-121">Criptografia AES (AES).</span><span class="sxs-lookup"><span data-stu-id="542ff-121">Advanced Encryption Standard (AES).</span></span> <span data-ttu-id="542ff-122">Esse algoritmo é compatível com o <a href="microsoft-aes-cryptographic-provider.md">provedor criptográfico do Microsoft AES</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-122">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-123">CALG_AES_128</span><span class="sxs-lookup"><span data-stu-id="542ff-123">CALG_AES_128</span></span></td>
<td><span data-ttu-id="542ff-124">0x0000660e</span><span class="sxs-lookup"><span data-stu-id="542ff-124">0x0000660e</span></span></td>
<td><span data-ttu-id="542ff-125">AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="542ff-125">128 bit AES.</span></span> <span data-ttu-id="542ff-126">Esse algoritmo é compatível com o <a href="microsoft-aes-cryptographic-provider.md">provedor criptográfico do Microsoft AES</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-126">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-127">CALG_AES_192</span><span class="sxs-lookup"><span data-stu-id="542ff-127">CALG_AES_192</span></span></td>
<td><span data-ttu-id="542ff-128">0x0000660f</span><span class="sxs-lookup"><span data-stu-id="542ff-128">0x0000660f</span></span></td>
<td><span data-ttu-id="542ff-129">AES de 192 bits.</span><span class="sxs-lookup"><span data-stu-id="542ff-129">192 bit AES.</span></span> <span data-ttu-id="542ff-130">Esse algoritmo é compatível com o <a href="microsoft-aes-cryptographic-provider.md">provedor criptográfico do Microsoft AES</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-130">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-131">CALG_AES_256</span><span class="sxs-lookup"><span data-stu-id="542ff-131">CALG_AES_256</span></span></td>
<td><span data-ttu-id="542ff-132">0x00006610</span><span class="sxs-lookup"><span data-stu-id="542ff-132">0x00006610</span></span></td>
<td><span data-ttu-id="542ff-133">AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="542ff-133">256 bit AES.</span></span> <span data-ttu-id="542ff-134">Esse algoritmo é compatível com o <a href="microsoft-aes-cryptographic-provider.md">provedor criptográfico do Microsoft AES</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-134">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-135">CALG_AGREEDKEY_ANY</span><span class="sxs-lookup"><span data-stu-id="542ff-135">CALG_AGREEDKEY_ANY</span></span></td>
<td><span data-ttu-id="542ff-136">0x0000aa03</span><span class="sxs-lookup"><span data-stu-id="542ff-136">0x0000aa03</span></span></td>
<td><span data-ttu-id="542ff-137">Identificador de algoritmo temporário para identificadores do Diffie-Hellman – chaves acordadas.</span><span class="sxs-lookup"><span data-stu-id="542ff-137">Temporary algorithm identifier for handles of Diffie-Hellman–agreed keys.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-138">CALG_CYLINK_MEK</span><span class="sxs-lookup"><span data-stu-id="542ff-138">CALG_CYLINK_MEK</span></span></td>
<td><span data-ttu-id="542ff-139">0x0000660c</span><span class="sxs-lookup"><span data-stu-id="542ff-139">0x0000660c</span></span></td>
<td><span data-ttu-id="542ff-140">Um algoritmo para criar uma chave DES de 40 bits que tem bits de paridade e bits de chave zerados para tornar seu comprimento de chave 64 bits.</span><span class="sxs-lookup"><span data-stu-id="542ff-140">An algorithm to create a 40-bit DES key that has parity bits and zeroed key bits to make its key length 64 bits.</span></span> <span data-ttu-id="542ff-141">Esse algoritmo é compatível com o <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-141">This algorithm is supported by the <a href=""></a><a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-142">CALG_DES</span><span class="sxs-lookup"><span data-stu-id="542ff-142">CALG_DES</span></span></td>
<td><span data-ttu-id="542ff-143">0x00006601</span><span class="sxs-lookup"><span data-stu-id="542ff-143">0x00006601</span></span></td>
<td><span data-ttu-id="542ff-144">Algoritmo de criptografia DES.</span><span class="sxs-lookup"><span data-stu-id="542ff-144">DES encryption algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-145">CALG_DESX</span><span class="sxs-lookup"><span data-stu-id="542ff-145">CALG_DESX</span></span></td>
<td><span data-ttu-id="542ff-146">0x00006604</span><span class="sxs-lookup"><span data-stu-id="542ff-146">0x00006604</span></span></td>
<td><span data-ttu-id="542ff-147">Algoritmo de criptografia DESX.</span><span class="sxs-lookup"><span data-stu-id="542ff-147">DESX encryption algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-148">CALG_DH_EPHEM</span><span class="sxs-lookup"><span data-stu-id="542ff-148">CALG_DH_EPHEM</span></span></td>
<td><span data-ttu-id="542ff-149">0x0000aa02</span><span class="sxs-lookup"><span data-stu-id="542ff-149">0x0000aa02</span></span></td>
<td><span data-ttu-id="542ff-150">Diffie-Hellman algoritmo de troca de chave efêmera.</span><span class="sxs-lookup"><span data-stu-id="542ff-150">Diffie-Hellman ephemeral key exchange algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-151">CALG_DH_SF</span><span class="sxs-lookup"><span data-stu-id="542ff-151">CALG_DH_SF</span></span></td>
<td><span data-ttu-id="542ff-152">0x0000aa01</span><span class="sxs-lookup"><span data-stu-id="542ff-152">0x0000aa01</span></span></td>
<td><span data-ttu-id="542ff-153">Diffie-Hellman armazenar e encaminhar o algoritmo de troca de chaves.</span><span class="sxs-lookup"><span data-stu-id="542ff-153">Diffie-Hellman store and forward key exchange algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-154">CALG_DSS_SIGN</span><span class="sxs-lookup"><span data-stu-id="542ff-154">CALG_DSS_SIGN</span></span></td>
<td><span data-ttu-id="542ff-155">0x00002200</span><span class="sxs-lookup"><span data-stu-id="542ff-155">0x00002200</span></span></td>
<td><span data-ttu-id="542ff-156">Algoritmo de assinatura de <a href="/windows/desktop/SecGloss/p-gly"><em>chave pública</em></a> DSA.</span><span class="sxs-lookup"><span data-stu-id="542ff-156">DSA <a href="/windows/desktop/SecGloss/p-gly"><em>public key</em></a> signature algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-157">CALG_ECDH</span><span class="sxs-lookup"><span data-stu-id="542ff-157">CALG_ECDH</span></span></td>
<td><span data-ttu-id="542ff-158">0x0000aa05</span><span class="sxs-lookup"><span data-stu-id="542ff-158">0x0000aa05</span></span></td>
<td><span data-ttu-id="542ff-159">Curva elíptica Diffie-Hellman algoritmo de troca de chaves.</span><span class="sxs-lookup"><span data-stu-id="542ff-159">Elliptic curve Diffie-Hellman key exchange algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="542ff-160">Esse algoritmo tem suporte apenas por meio da <a href="/windows/desktop/SecCNG/cng-portal">API de criptografia: próxima geração</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-160">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="542ff-161"><strong>Windows Server 2003 e Windows XP:</strong> Não há suporte para esse algoritmo.</span><span class="sxs-lookup"><span data-stu-id="542ff-161"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-162">CALG_ECDH_EPHEM</span><span class="sxs-lookup"><span data-stu-id="542ff-162">CALG_ECDH_EPHEM</span></span></td>
<td><span data-ttu-id="542ff-163">0x0000ae06</span><span class="sxs-lookup"><span data-stu-id="542ff-163">0x0000ae06</span></span></td>
<td><span data-ttu-id="542ff-164">Curva elíptica efêmera Diffie-Hellman algoritmo de troca de chaves.</span><span class="sxs-lookup"><span data-stu-id="542ff-164">Ephemeral elliptic curve Diffie-Hellman key exchange algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="542ff-165">Esse algoritmo tem suporte apenas por meio da <a href="/windows/desktop/SecCNG/cng-portal">API de criptografia: próxima geração</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-165">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="542ff-166"><strong>Windows Server 2003 e Windows XP:</strong> Não há suporte para esse algoritmo.</span><span class="sxs-lookup"><span data-stu-id="542ff-166"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-167">CALG_ECDSA</span><span class="sxs-lookup"><span data-stu-id="542ff-167">CALG_ECDSA</span></span></td>
<td><span data-ttu-id="542ff-168">0x00002203</span><span class="sxs-lookup"><span data-stu-id="542ff-168">0x00002203</span></span></td>
<td><span data-ttu-id="542ff-169">Algoritmo de assinatura digital de curva elíptica.</span><span class="sxs-lookup"><span data-stu-id="542ff-169">Elliptic curve digital signature algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="542ff-170">Esse algoritmo tem suporte apenas por meio da <a href="/windows/desktop/SecCNG/cng-portal">API de criptografia: próxima geração</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-170">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="542ff-171"><strong>Windows Server 2003 e Windows XP:</strong> Não há suporte para esse algoritmo.</span><span class="sxs-lookup"><span data-stu-id="542ff-171"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-172">CALG_ECMQV</span><span class="sxs-lookup"><span data-stu-id="542ff-172">CALG_ECMQV</span></span></td>
<td><span data-ttu-id="542ff-173">0x0000a001</span><span class="sxs-lookup"><span data-stu-id="542ff-173">0x0000a001</span></span></td>
<td><span data-ttu-id="542ff-174">Algoritmo de troca de chave Menezes, t e Vanstone (MQV) de curva elíptica.</span><span class="sxs-lookup"><span data-stu-id="542ff-174">Elliptic curve Menezes, Qu, and Vanstone (MQV) key exchange algorithm.</span></span> <span data-ttu-id="542ff-175">Não há suporte para esse algoritmo.</span><span class="sxs-lookup"><span data-stu-id="542ff-175">This algorithm is not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-176">CALG_HASH_REPLACE_OWF</span><span class="sxs-lookup"><span data-stu-id="542ff-176">CALG_HASH_REPLACE_OWF</span></span></td>
<td><span data-ttu-id="542ff-177">0x0000800b</span><span class="sxs-lookup"><span data-stu-id="542ff-177">0x0000800b</span></span></td>
<td><span data-ttu-id="542ff-178">Algoritmo de hash de função unidirecional.</span><span class="sxs-lookup"><span data-stu-id="542ff-178">One way function hashing algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-179">CALG_HUGHES_MD5</span><span class="sxs-lookup"><span data-stu-id="542ff-179">CALG_HUGHES_MD5</span></span></td>
<td><span data-ttu-id="542ff-180">0x0000a003</span><span class="sxs-lookup"><span data-stu-id="542ff-180">0x0000a003</span></span></td>
<td><span data-ttu-id="542ff-181">Algoritmo de hash MD5 Hughes.</span><span class="sxs-lookup"><span data-stu-id="542ff-181">Hughes MD5 hashing algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-182">CALG_HMAC</span><span class="sxs-lookup"><span data-stu-id="542ff-182">CALG_HMAC</span></span></td>
<td><span data-ttu-id="542ff-183">0x00008009</span><span class="sxs-lookup"><span data-stu-id="542ff-183">0x00008009</span></span></td>
<td><span data-ttu-id="542ff-184">Algoritmo de hash com chave HMAC.</span><span class="sxs-lookup"><span data-stu-id="542ff-184">HMAC keyed hash algorithm.</span></span> <span data-ttu-id="542ff-185">Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-185">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-186">CALG_KEA_KEYX</span><span class="sxs-lookup"><span data-stu-id="542ff-186">CALG_KEA_KEYX</span></span></td>
<td><span data-ttu-id="542ff-187">0x0000aa04</span><span class="sxs-lookup"><span data-stu-id="542ff-187">0x0000aa04</span></span></td>
<td><span data-ttu-id="542ff-188">FORTEZZA (KEA Key Exchange Algorithm).</span><span class="sxs-lookup"><span data-stu-id="542ff-188">KEA key exchange algorithm (FORTEZZA).</span></span> <span data-ttu-id="542ff-189">Não há suporte para esse algoritmo.</span><span class="sxs-lookup"><span data-stu-id="542ff-189">This algorithm is not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-190">CALG_MAC</span><span class="sxs-lookup"><span data-stu-id="542ff-190">CALG_MAC</span></span></td>
<td><span data-ttu-id="542ff-191">0x00008005</span><span class="sxs-lookup"><span data-stu-id="542ff-191">0x00008005</span></span></td>
<td><span data-ttu-id="542ff-192">Algoritmo de hash com chave <a href="/windows/desktop/SecGloss/m-gly"><em>Mac</em></a> .</span><span class="sxs-lookup"><span data-stu-id="542ff-192"><a href="/windows/desktop/SecGloss/m-gly"><em>MAC</em></a> keyed hash algorithm.</span></span> <span data-ttu-id="542ff-193">Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-193">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-194">CALG_MD2</span><span class="sxs-lookup"><span data-stu-id="542ff-194">CALG_MD2</span></span></td>
<td><span data-ttu-id="542ff-195">0x00008001</span><span class="sxs-lookup"><span data-stu-id="542ff-195">0x00008001</span></span></td>
<td><span data-ttu-id="542ff-196">Algoritmo de hash MD2.</span><span class="sxs-lookup"><span data-stu-id="542ff-196">MD2 hashing algorithm.</span></span> <span data-ttu-id="542ff-197">Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-197">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-198">CALG_MD4</span><span class="sxs-lookup"><span data-stu-id="542ff-198">CALG_MD4</span></span></td>
<td><span data-ttu-id="542ff-199">0x00008002</span><span class="sxs-lookup"><span data-stu-id="542ff-199">0x00008002</span></span></td>
<td><span data-ttu-id="542ff-200">Algoritmo de hash MD4.</span><span class="sxs-lookup"><span data-stu-id="542ff-200">MD4 hashing algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-201">CALG_MD5</span><span class="sxs-lookup"><span data-stu-id="542ff-201">CALG_MD5</span></span></td>
<td><span data-ttu-id="542ff-202">0x00008003</span><span class="sxs-lookup"><span data-stu-id="542ff-202">0x00008003</span></span></td>
<td><span data-ttu-id="542ff-203">Algoritmo de hash MD5.</span><span class="sxs-lookup"><span data-stu-id="542ff-203">MD5 hashing algorithm.</span></span> <span data-ttu-id="542ff-204">Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-204">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-205">CALG_NO_SIGN</span><span class="sxs-lookup"><span data-stu-id="542ff-205">CALG_NO_SIGN</span></span></td>
<td><span data-ttu-id="542ff-206">0x00002000</span><span class="sxs-lookup"><span data-stu-id="542ff-206">0x00002000</span></span></td>
<td><span data-ttu-id="542ff-207">Nenhum algoritmo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="542ff-207">No signature algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-208">CALG_OID_INFO_CNG_ONLY</span><span class="sxs-lookup"><span data-stu-id="542ff-208">CALG_OID_INFO_CNG_ONLY</span></span></td>
<td><span data-ttu-id="542ff-209">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="542ff-209">0xffffffff</span></span></td>
<td><span data-ttu-id="542ff-210">O algoritmo é implementado apenas na CNG.</span><span class="sxs-lookup"><span data-stu-id="542ff-210">The algorithm is only implemented in CNG.</span></span> <span data-ttu-id="542ff-211">A macro, IS_SPECIAL_OID_INFO_ALGID, pode ser usada para determinar se um algoritmo de criptografia tem suporte apenas usando as funções CNG.</span><span class="sxs-lookup"><span data-stu-id="542ff-211">The macro, IS_SPECIAL_OID_INFO_ALGID, can be used to determine whether a cryptography algorithm is only supported by using the CNG functions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-212">CALG_OID_INFO_PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="542ff-212">CALG_OID_INFO_PARAMETERS</span></span></td>
<td><span data-ttu-id="542ff-213">0xfffffffe</span><span class="sxs-lookup"><span data-stu-id="542ff-213">0xfffffffe</span></span></td>
<td><span data-ttu-id="542ff-214">O algoritmo é definido nos parâmetros codificados.</span><span class="sxs-lookup"><span data-stu-id="542ff-214">The algorithm is defined in the encoded parameters.</span></span> <span data-ttu-id="542ff-215">O algoritmo só tem suporte usando o CNG.</span><span class="sxs-lookup"><span data-stu-id="542ff-215">The algorithm is only supported by using CNG.</span></span> <span data-ttu-id="542ff-216">A macro, IS_SPECIAL_OID_INFO_ALGID, pode ser usada para determinar se um algoritmo de criptografia tem suporte apenas usando as funções CNG.</span><span class="sxs-lookup"><span data-stu-id="542ff-216">The macro, IS_SPECIAL_OID_INFO_ALGID, can be used to determine whether a cryptography algorithm is only supported by using the CNG functions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-217">CALG_PCT1_MASTER</span><span class="sxs-lookup"><span data-stu-id="542ff-217">CALG_PCT1_MASTER</span></span></td>
<td><span data-ttu-id="542ff-218">0x00004c04</span><span class="sxs-lookup"><span data-stu-id="542ff-218">0x00004c04</span></span></td>
<td><span data-ttu-id="542ff-219">Usado pelo sistema de operações Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="542ff-219">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="542ff-220">Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="542ff-220">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-221">CALG_RC2</span><span class="sxs-lookup"><span data-stu-id="542ff-221">CALG_RC2</span></span></td>
<td><span data-ttu-id="542ff-222">0x00006602</span><span class="sxs-lookup"><span data-stu-id="542ff-222">0x00006602</span></span></td>
<td><span data-ttu-id="542ff-223">Algoritmo de criptografia de bloco RC2.</span><span class="sxs-lookup"><span data-stu-id="542ff-223">RC2 block encryption algorithm.</span></span> <span data-ttu-id="542ff-224">Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-224">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-225">CALG_RC4</span><span class="sxs-lookup"><span data-stu-id="542ff-225">CALG_RC4</span></span></td>
<td><span data-ttu-id="542ff-226">0x00006801</span><span class="sxs-lookup"><span data-stu-id="542ff-226">0x00006801</span></span></td>
<td><span data-ttu-id="542ff-227">Algoritmo de criptografia de fluxo RC4.</span><span class="sxs-lookup"><span data-stu-id="542ff-227">RC4 stream encryption algorithm.</span></span> <span data-ttu-id="542ff-228">Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-228">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-229">CALG_RC5</span><span class="sxs-lookup"><span data-stu-id="542ff-229">CALG_RC5</span></span></td>
<td><span data-ttu-id="542ff-230">0x0000660d</span><span class="sxs-lookup"><span data-stu-id="542ff-230">0x0000660d</span></span></td>
<td><span data-ttu-id="542ff-231">Algoritmo de criptografia de bloco RC5.</span><span class="sxs-lookup"><span data-stu-id="542ff-231">RC5 block encryption algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-232">CALG_RSA_KEYX</span><span class="sxs-lookup"><span data-stu-id="542ff-232">CALG_RSA_KEYX</span></span></td>
<td><span data-ttu-id="542ff-233">0x0000a400</span><span class="sxs-lookup"><span data-stu-id="542ff-233">0x0000a400</span></span></td>
<td><span data-ttu-id="542ff-234">Algoritmo de troca de chave pública RSA.</span><span class="sxs-lookup"><span data-stu-id="542ff-234">RSA public key exchange algorithm.</span></span> <span data-ttu-id="542ff-235">Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-235">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-236">CALG_RSA_SIGN</span><span class="sxs-lookup"><span data-stu-id="542ff-236">CALG_RSA_SIGN</span></span></td>
<td><span data-ttu-id="542ff-237">0x00002400</span><span class="sxs-lookup"><span data-stu-id="542ff-237">0x00002400</span></span></td>
<td><span data-ttu-id="542ff-238">Algoritmo de assinatura de chave pública RSA.</span><span class="sxs-lookup"><span data-stu-id="542ff-238">RSA public key signature algorithm.</span></span> <span data-ttu-id="542ff-239">Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-239">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-240">CALG_SCHANNEL_ENC_KEY</span><span class="sxs-lookup"><span data-stu-id="542ff-240">CALG_SCHANNEL_ENC_KEY</span></span></td>
<td><span data-ttu-id="542ff-241">0x00004c07</span><span class="sxs-lookup"><span data-stu-id="542ff-241">0x00004c07</span></span></td>
<td><span data-ttu-id="542ff-242">Usado pelo sistema de operações Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="542ff-242">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="542ff-243">Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="542ff-243">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-244">CALG_SCHANNEL_MAC_KEY</span><span class="sxs-lookup"><span data-stu-id="542ff-244">CALG_SCHANNEL_MAC_KEY</span></span></td>
<td><span data-ttu-id="542ff-245">0x00004c03</span><span class="sxs-lookup"><span data-stu-id="542ff-245">0x00004c03</span></span></td>
<td><span data-ttu-id="542ff-246">Usado pelo sistema de operações Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="542ff-246">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="542ff-247">Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="542ff-247">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-248">CALG_SCHANNEL_MASTER_HASH</span><span class="sxs-lookup"><span data-stu-id="542ff-248">CALG_SCHANNEL_MASTER_HASH</span></span></td>
<td><span data-ttu-id="542ff-249">0x00004c02</span><span class="sxs-lookup"><span data-stu-id="542ff-249">0x00004c02</span></span></td>
<td><span data-ttu-id="542ff-250">Usado pelo sistema de operações Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="542ff-250">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="542ff-251">Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="542ff-251">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-252">CALG_SEAL</span><span class="sxs-lookup"><span data-stu-id="542ff-252">CALG_SEAL</span></span></td>
<td><span data-ttu-id="542ff-253">0x00006802</span><span class="sxs-lookup"><span data-stu-id="542ff-253">0x00006802</span></span></td>
<td><span data-ttu-id="542ff-254">Algoritmo de criptografia do lacre.</span><span class="sxs-lookup"><span data-stu-id="542ff-254">SEAL encryption algorithm.</span></span> <span data-ttu-id="542ff-255">Não há suporte para esse algoritmo.</span><span class="sxs-lookup"><span data-stu-id="542ff-255">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-256">CALG_SHA</span><span class="sxs-lookup"><span data-stu-id="542ff-256">CALG_SHA</span></span></td>
<td><span data-ttu-id="542ff-257">0x00008004</span><span class="sxs-lookup"><span data-stu-id="542ff-257">0x00008004</span></span></td>
<td><span data-ttu-id="542ff-258">Algoritmo de hash SHA.</span><span class="sxs-lookup"><span data-stu-id="542ff-258">SHA hashing algorithm.</span></span> <span data-ttu-id="542ff-259">Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-259">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-260">CALG_SHA1</span><span class="sxs-lookup"><span data-stu-id="542ff-260">CALG_SHA1</span></span></td>
<td><span data-ttu-id="542ff-261">0x00008004</span><span class="sxs-lookup"><span data-stu-id="542ff-261">0x00008004</span></span></td>
<td><span data-ttu-id="542ff-262">O mesmo que <strong>CALG_SHA</strong>.</span><span class="sxs-lookup"><span data-stu-id="542ff-262">Same as <strong>CALG_SHA</strong>.</span></span> <span data-ttu-id="542ff-263">Esse algoritmo é compatível com o <a href="microsoft-base-cryptographic-provider.md">provedor Microsoft Base Cryptographic</a>.</span><span class="sxs-lookup"><span data-stu-id="542ff-263">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-264">CALG_SHA_256</span><span class="sxs-lookup"><span data-stu-id="542ff-264">CALG_SHA_256</span></span></td>
<td><span data-ttu-id="542ff-265">0x0000800c</span><span class="sxs-lookup"><span data-stu-id="542ff-265">0x0000800c</span></span></td>
<td><span data-ttu-id="542ff-266">algoritmo de hash SHA de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="542ff-266">256 bit SHA hashing algorithm.</span></span> <span data-ttu-id="542ff-267">Esse algoritmo tem suporte do provedor criptográfico RSA e AES aprimorado da Microsoft. <strong>Windows XP com SP3:</strong> Esse algoritmo tem suporte do Microsoft Enhanced RSA e do AES (provedor criptográfico).</span><span class="sxs-lookup"><span data-stu-id="542ff-267">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider..<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="542ff-268"><strong>Windows XP com SP2, Windows XP com SP1 e Windows XP:</strong> Não há suporte para esse algoritmo.</span><span class="sxs-lookup"><span data-stu-id="542ff-268"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-269">CALG_SHA_384</span><span class="sxs-lookup"><span data-stu-id="542ff-269">CALG_SHA_384</span></span></td>
<td><span data-ttu-id="542ff-270">0x0000800d</span><span class="sxs-lookup"><span data-stu-id="542ff-270">0x0000800d</span></span></td>
<td><span data-ttu-id="542ff-271">algoritmo de hash SHA de 384 bits.</span><span class="sxs-lookup"><span data-stu-id="542ff-271">384 bit SHA hashing algorithm.</span></span> <span data-ttu-id="542ff-272">Esse algoritmo tem suporte do provedor criptográfico RSA e AES aprimorado da Microsoft. <strong>Windows XP com SP3:</strong> Esse algoritmo tem suporte do Microsoft Enhanced RSA e do AES (provedor criptográfico).</span><span class="sxs-lookup"><span data-stu-id="542ff-272">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider.<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="542ff-273"><strong>Windows XP com SP2, Windows XP com SP1 e Windows XP:</strong> Não há suporte para esse algoritmo.</span><span class="sxs-lookup"><span data-stu-id="542ff-273"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-274">CALG_SHA_512</span><span class="sxs-lookup"><span data-stu-id="542ff-274">CALG_SHA_512</span></span></td>
<td><span data-ttu-id="542ff-275">0x0000800e</span><span class="sxs-lookup"><span data-stu-id="542ff-275">0x0000800e</span></span></td>
<td><span data-ttu-id="542ff-276">algoritmo de hash SHA de 512 bits.</span><span class="sxs-lookup"><span data-stu-id="542ff-276">512 bit SHA hashing algorithm.</span></span> <span data-ttu-id="542ff-277">Esse algoritmo tem suporte do provedor criptográfico RSA e AES aprimorado da Microsoft. <strong>Windows XP com SP3:</strong> Esse algoritmo tem suporte do Microsoft Enhanced RSA e do AES (provedor criptográfico).</span><span class="sxs-lookup"><span data-stu-id="542ff-277">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider.<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="542ff-278"><strong>Windows XP com SP2, Windows XP com SP1 e Windows XP:</strong> Não há suporte para esse algoritmo.</span><span class="sxs-lookup"><span data-stu-id="542ff-278"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-279">CALG_SKIPJACK</span><span class="sxs-lookup"><span data-stu-id="542ff-279">CALG_SKIPJACK</span></span></td>
<td><span data-ttu-id="542ff-280">0x0000660a</span><span class="sxs-lookup"><span data-stu-id="542ff-280">0x0000660a</span></span></td>
<td><span data-ttu-id="542ff-281">Skipjack o algoritmo de criptografia de bloco (FORTEZZA).</span><span class="sxs-lookup"><span data-stu-id="542ff-281">Skipjack block encryption algorithm (FORTEZZA).</span></span> <span data-ttu-id="542ff-282">Não há suporte para esse algoritmo.</span><span class="sxs-lookup"><span data-stu-id="542ff-282">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-283">CALG_SSL2_MASTER</span><span class="sxs-lookup"><span data-stu-id="542ff-283">CALG_SSL2_MASTER</span></span></td>
<td><span data-ttu-id="542ff-284">0x00004c05</span><span class="sxs-lookup"><span data-stu-id="542ff-284">0x00004c05</span></span></td>
<td><span data-ttu-id="542ff-285">Usado pelo sistema de operações Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="542ff-285">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="542ff-286">Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="542ff-286">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-287">CALG_SSL3_MASTER</span><span class="sxs-lookup"><span data-stu-id="542ff-287">CALG_SSL3_MASTER</span></span></td>
<td><span data-ttu-id="542ff-288">0x00004c01</span><span class="sxs-lookup"><span data-stu-id="542ff-288">0x00004c01</span></span></td>
<td><span data-ttu-id="542ff-289">Usado pelo sistema de operações Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="542ff-289">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="542ff-290">Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="542ff-290">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-291">CALG_SSL3_SHAMD5</span><span class="sxs-lookup"><span data-stu-id="542ff-291">CALG_SSL3_SHAMD5</span></span></td>
<td><span data-ttu-id="542ff-292">0x00008008</span><span class="sxs-lookup"><span data-stu-id="542ff-292">0x00008008</span></span></td>
<td><span data-ttu-id="542ff-293">Usado pelo sistema de operações Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="542ff-293">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="542ff-294">Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="542ff-294">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-295">CALG_TEK</span><span class="sxs-lookup"><span data-stu-id="542ff-295">CALG_TEK</span></span></td>
<td><span data-ttu-id="542ff-296">0x0000660b</span><span class="sxs-lookup"><span data-stu-id="542ff-296">0x0000660b</span></span></td>
<td><span data-ttu-id="542ff-297">TEK (FORTEZZA).</span><span class="sxs-lookup"><span data-stu-id="542ff-297">TEK (FORTEZZA).</span></span> <span data-ttu-id="542ff-298">Não há suporte para esse algoritmo.</span><span class="sxs-lookup"><span data-stu-id="542ff-298">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="542ff-299">CALG_TLS1_MASTER</span><span class="sxs-lookup"><span data-stu-id="542ff-299">CALG_TLS1_MASTER</span></span></td>
<td><span data-ttu-id="542ff-300">0x00004c06</span><span class="sxs-lookup"><span data-stu-id="542ff-300">0x00004c06</span></span></td>
<td><span data-ttu-id="542ff-301">Usado pelo sistema de operações Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="542ff-301">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="542ff-302">Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="542ff-302">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="542ff-303">CALG_TLS1PRF</span><span class="sxs-lookup"><span data-stu-id="542ff-303">CALG_TLS1PRF</span></span></td>
<td><span data-ttu-id="542ff-304">0x0000800a</span><span class="sxs-lookup"><span data-stu-id="542ff-304">0x0000800a</span></span></td>
<td><span data-ttu-id="542ff-305">Usado pelo sistema de operações Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="542ff-305">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="542ff-306">Esse <strong>ALG_ID</strong> não deve ser usado por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="542ff-306">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="542ff-307">Para o [provedor criptográfico base da Microsoft](microsoft-base-cryptographic-provider.md), o [provedor de criptografia forte da Microsoft](microsoft-strong-cryptographic-provider.md)e o [provedor criptográfico aprimorado](microsoft-enhanced-cryptographic-provider.md)da Microsoft, os **ALG_IDs** usados para as principais especificações **AT_KEYEXCHANGE** e **AT_SIGNATURE** são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="542ff-307">For the [Microsoft Base Cryptographic Provider](microsoft-base-cryptographic-provider.md), the [Microsoft Strong Cryptographic Provider](microsoft-strong-cryptographic-provider.md), and the [Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md), the **ALG_IDs** used for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are as follows:</span></span>

-   <span data-ttu-id="542ff-308">**CALG_RSA_KEYX** é usado para **AT_KEYEXCHANGE**.</span><span class="sxs-lookup"><span data-stu-id="542ff-308">**CALG_RSA_KEYX** is used for **AT_KEYEXCHANGE**.</span></span>
-   <span data-ttu-id="542ff-309">**CALG_RSA_SIGN** é usado para **AT_SIGNATURE**.</span><span class="sxs-lookup"><span data-stu-id="542ff-309">**CALG_RSA_SIGN** is used for **AT_SIGNATURE**.</span></span>

<span data-ttu-id="542ff-310">Para o [Microsoft Base DSS e o provedor de criptografia Diffie-Hellman](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), os **ALG_IDs** usados para as principais especificações **AT_KEYEXCHANGE** e **AT_SIGNATURE** são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="542ff-310">For the [Microsoft Base DSS and Diffie-Hellman Cryptographic Provider](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), the **ALG_IDs** used for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are as follows:</span></span>

-   <span data-ttu-id="542ff-311">**CALG_DH_SF** é usado para **AT_KEYEXCHANGE**.</span><span class="sxs-lookup"><span data-stu-id="542ff-311">**CALG_DH_SF** is used for **AT_KEYEXCHANGE**.</span></span>
-   <span data-ttu-id="542ff-312">**CALG_DSS_SIGN** é usado para **AT_SIGNATURE**.</span><span class="sxs-lookup"><span data-stu-id="542ff-312">**CALG_DSS_SIGN** is used for **AT_SIGNATURE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="542ff-313">Requisitos</span><span class="sxs-lookup"><span data-stu-id="542ff-313">Requirements</span></span>



| <span data-ttu-id="542ff-314">Requisito</span><span class="sxs-lookup"><span data-stu-id="542ff-314">Requirement</span></span> | <span data-ttu-id="542ff-315">Valor</span><span class="sxs-lookup"><span data-stu-id="542ff-315">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="542ff-316">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="542ff-316">Minimum supported client</span></span><br/> | <span data-ttu-id="542ff-317">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="542ff-317">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="542ff-318">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="542ff-318">Minimum supported server</span></span><br/> | <span data-ttu-id="542ff-319">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="542ff-319">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="542ff-320">parâmetro</span><span class="sxs-lookup"><span data-stu-id="542ff-320">Header</span></span><br/>                   | <dl> <span data-ttu-id="542ff-321"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="542ff-321"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="542ff-322">Confira também</span><span class="sxs-lookup"><span data-stu-id="542ff-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="542ff-323">Funções de criptografia</span><span class="sxs-lookup"><span data-stu-id="542ff-323">Cryptography Functions</span></span>](cryptography-functions.md)
</dt> <dt>

[<span data-ttu-id="542ff-324">**CRYPT_ALGORITHM_IDENTIFIER**</span><span class="sxs-lookup"><span data-stu-id="542ff-324">**CRYPT_ALGORITHM_IDENTIFIER**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[<span data-ttu-id="542ff-325">**CryptFindOIDInfo**</span><span class="sxs-lookup"><span data-stu-id="542ff-325">**CryptFindOIDInfo**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
