---
description: Contém definições de termos de segurança que começam com a letra B.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2e570727-7da0-4e17-bf5d-6fe0e6aef65b
title: B (Glossário de segurança)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40aedaebddb86ddf9f32a9a3d86cf4cf4a613642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796363"
---
# <a name="b-security-glossary"></a><span data-ttu-id="588f3-103">B (Glossário de segurança)</span><span class="sxs-lookup"><span data-stu-id="588f3-103">B (Security Glossary)</span></span>

<span data-ttu-id="588f3-104">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="588f3-104">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="588f3-105"><span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**autoridade de backup**</span><span class="sxs-lookup"><span data-stu-id="588f3-105"><span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**backup authority**</span></span>
</dt> <dd>

<span data-ttu-id="588f3-106">Um aplicativo confiável em execução em um computador seguro que fornece armazenamento secundário para as chaves de sessão de seus clientes.</span><span class="sxs-lookup"><span data-stu-id="588f3-106">A trusted application running on a secure computer that provides secondary storage for the session keys of its clients.</span></span> <span data-ttu-id="588f3-107">A autoridade de backup armazena chaves de sessão como BLOBs de chave que são criptografados com a chave pública da autoridade de backup.</span><span class="sxs-lookup"><span data-stu-id="588f3-107">The backup authority stores session keys as key BLOBs that are encrypted with the backup authority's public key.</span></span>

</dd> <dt>

<span data-ttu-id="588f3-108"><span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**tipo de conteúdo base**</span><span class="sxs-lookup"><span data-stu-id="588f3-108"><span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**base content type**</span></span>
</dt> <dd>

<span data-ttu-id="588f3-109">Um tipo de dados contidos em uma \# mensagem PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="588f3-109">A type of data contained in a PKCS \#7 message.</span></span> <span data-ttu-id="588f3-110">Os tipos de conteúdo base contêm apenas dados, sem aprimoramentos de criptografia, como hashes ou assinaturas.</span><span class="sxs-lookup"><span data-stu-id="588f3-110">Base content types only contain data, no cryptographic enhancements such as hashes or signatures.</span></span> <span data-ttu-id="588f3-111">Atualmente, o único tipo de conteúdo base é o tipo de conteúdo de dados.</span><span class="sxs-lookup"><span data-stu-id="588f3-111">Currently, the only base content type is the Data content type.</span></span>

</dd> <dt>

<span data-ttu-id="588f3-112"><span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**funções de criptografia base**</span><span class="sxs-lookup"><span data-stu-id="588f3-112"><span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**base cryptographic functions**</span></span>
</dt> <dd>

<span data-ttu-id="588f3-113">O menor nível de funções na arquitetura de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="588f3-113">The lowest level of functions in the CryptoAPI architecture.</span></span> <span data-ttu-id="588f3-114">Eles são usados por aplicativos e outras funções de CryptoAPI de alto nível para fornecer acesso aos algoritmos criptográficos fornecidos pelo CSP, à geração de chave segura e ao armazenamento seguro de segredos.</span><span class="sxs-lookup"><span data-stu-id="588f3-114">They are used by applications and other high-level CryptoAPI functions to provide access to CSP-provided cryptographic algorithms, secure key generation, and secure storage of secrets.</span></span>

<span data-ttu-id="588f3-115">Consulte também [*provedores de serviço de criptografia*](c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="588f3-115">See also [*cryptographic service providers*](c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="588f3-116"><span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**Regras básicas de codificação**</span><span class="sxs-lookup"><span data-stu-id="588f3-116"><span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**Basic Encoding Rules**</span></span>
</dt> <dd>

<span data-ttu-id="588f3-117">BRO O conjunto de regras usadas para codificar os dados definidos pelo ASN. 1 em um fluxo de bits (zeros ou uns) para armazenamento ou transmissão externa.</span><span class="sxs-lookup"><span data-stu-id="588f3-117">(BER) The set of rules used to encode ASN.1 defined data into a stream of bits (zeros or ones) for external storage or transmission.</span></span> <span data-ttu-id="588f3-118">Um único objeto ASN. 1 pode ter vários codificadores do BER equivalentes.</span><span class="sxs-lookup"><span data-stu-id="588f3-118">A single ASN.1 object may have several equivalent BER encodes.</span></span> <span data-ttu-id="588f3-119">O BER é definido na recomendação de CCITT X. 209.</span><span class="sxs-lookup"><span data-stu-id="588f3-119">BER is defined in CCITT Recommendation X.209.</span></span> <span data-ttu-id="588f3-120">Esse é um dos dois métodos de codificação usados atualmente pelo CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="588f3-120">This is one of the two encoding methods currently used by CryptoAPI.</span></span>

</dd> <dt>

<span data-ttu-id="588f3-121"><span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**BRO**</span><span class="sxs-lookup"><span data-stu-id="588f3-121"><span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**BER**</span></span>
</dt> <dd>

<span data-ttu-id="588f3-122">Consulte *regras básicas de codificação*.</span><span class="sxs-lookup"><span data-stu-id="588f3-122">See *Basic Encoding Rules*.</span></span>

</dd> <dt>

<span data-ttu-id="588f3-123"><span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**big endian**</span><span class="sxs-lookup"><span data-stu-id="588f3-123"><span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**big-endian**</span></span>
</dt> <dd>

<span data-ttu-id="588f3-124">Um formato de memória ou de dados no qual o byte mais significativo é armazenado no endereço inferior ou chega primeiro.</span><span class="sxs-lookup"><span data-stu-id="588f3-124">A memory or data format in which the most significant byte is stored at the lower address or arrives first.</span></span>

<span data-ttu-id="588f3-125">Veja também [*little-endian*](l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="588f3-125">See also [*little-endian*](l-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="588f3-126"><span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**BLOB**</span><span class="sxs-lookup"><span data-stu-id="588f3-126"><span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="588f3-127">Uma sequência genérica de bits que contém uma ou mais estruturas de cabeçalho de comprimento fixo, além de dados específicos de contexto.</span><span class="sxs-lookup"><span data-stu-id="588f3-127">A generic sequence of bits that contain one or more fixed-length header structures plus context specific data.</span></span>

<span data-ttu-id="588f3-128">Consulte também [*blobs de chave*](k-gly.md), [*blobs de certificado*](c-gly.md), [*blobs de nome de certificado*](c-gly.md)e [*blobs de atributo*](a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="588f3-128">See also [*key BLOBs*](k-gly.md), [*certificate BLOBs*](c-gly.md), [*certificate name BLOBs*](c-gly.md), and [*attribute BLOBs*](a-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="588f3-129"><span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**codificação de bloco**</span><span class="sxs-lookup"><span data-stu-id="588f3-129"><span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**block cipher**</span></span>
</dt> <dd>

<span data-ttu-id="588f3-130">Um algoritmo de codificação que criptografa dados em unidades discretas (chamadas de blocos), em vez de como um fluxo contínuo de bits.</span><span class="sxs-lookup"><span data-stu-id="588f3-130">A cipher algorithm that encrypts data in discrete units (called blocks), rather than as a continuous stream of bits.</span></span> <span data-ttu-id="588f3-131">O tamanho de bloco mais comum é de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="588f3-131">The most common block size is 64 bits.</span></span> <span data-ttu-id="588f3-132">Por exemplo, o DES é uma codificação de bloco.</span><span class="sxs-lookup"><span data-stu-id="588f3-132">For example, DES is a block cipher.</span></span>

<span data-ttu-id="588f3-133">Consulte também [*codificação de fluxo*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="588f3-133">See also [*stream cipher*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="588f3-134"><span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**chave de criptografia em massa**</span><span class="sxs-lookup"><span data-stu-id="588f3-134"><span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**bulk encryption key**</span></span>
</dt> <dd>

<span data-ttu-id="588f3-135">Uma chave de sessão derivada de uma chave mestra.</span><span class="sxs-lookup"><span data-stu-id="588f3-135">A session key derived from a master key.</span></span> <span data-ttu-id="588f3-136">As chaves de criptografia em massa são usadas na criptografia [*Schannel*](s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="588f3-136">Bulk encryption keys are used in [*Schannel*](s-gly.md) encryption.</span></span>

</dd> </dl>

 

 



