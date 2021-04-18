---
description: Contém definições de termos de segurança que começam com a letra C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: db46def4-bfdc-4801-a57d-d568e94a2dbb
title: C (Glossário de segurança)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 863422525326ec0a04a597d33a29553006bb014b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756671"
---
# <a name="c-security-glossary"></a><span data-ttu-id="5c881-103">C (Glossário de segurança)</span><span class="sxs-lookup"><span data-stu-id="5c881-103">C (Security Glossary)</span></span>

<span data-ttu-id="5c881-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="5c881-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="5c881-105"><span id="_security_ca_gly"></span><span id="_SECURITY_CA_GLY"></span>**AC**</span><span class="sxs-lookup"><span data-stu-id="5c881-105"><span id="_security_ca_gly"></span><span id="_SECURITY_CA_GLY"></span>**CA**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-106">Consulte *autoridade de certificação*.</span><span class="sxs-lookup"><span data-stu-id="5c881-106">See *certification authority*.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-107"><span id="_security_ca_certificate_gly"></span><span id="_SECURITY_CA_CERTIFICATE_GLY"></span>**Certificado de autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="5c881-107"><span id="_security_ca_certificate_gly"></span><span id="_SECURITY_CA_CERTIFICATE_GLY"></span>**CA certificate**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-108">Identifica a AC (autoridade de certificação) que emite certificados de autenticação de servidor e cliente para os servidores e clientes que solicitam esses certificados.</span><span class="sxs-lookup"><span data-stu-id="5c881-108">Identifies the certification authority (CA) that issues server and client authentication certificates to the servers and clients that request these certificates.</span></span> <span data-ttu-id="5c881-109">Como ele contém uma chave pública usada em assinaturas digitais, ele também é conhecido como um certificado de assinatura.</span><span class="sxs-lookup"><span data-stu-id="5c881-109">Because it contains a public key used in digital signatures, it is also referred to as a signature certificate.</span></span> <span data-ttu-id="5c881-110">Se a autoridade de certificação for uma autoridade raiz, o certificado de autoridade de certificação poderá ser chamado de certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="5c881-110">If the CA is a root authority, the CA certificate may be referred to as a root certificate.</span></span> <span data-ttu-id="5c881-111">Às vezes, também conhecido como um certificado de site.</span><span class="sxs-lookup"><span data-stu-id="5c881-111">Also sometimes known as a site certificate.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-112"><span id="_security_ca_hierarchy_gly"></span><span id="_SECURITY_CA_HIERARCHY_GLY"></span>**Hierarquia de CA**</span><span class="sxs-lookup"><span data-stu-id="5c881-112"><span id="_security_ca_hierarchy_gly"></span><span id="_SECURITY_CA_HIERARCHY_GLY"></span>**CA hierarchy**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-113">Uma hierarquia de autoridade de certificação (CA) contém várias CAs.</span><span class="sxs-lookup"><span data-stu-id="5c881-113">A certification authority (CA) hierarchy contains multiple CAs.</span></span> <span data-ttu-id="5c881-114">Ele é organizado de forma que cada CA seja certificada por outra CA em um nível mais alto da hierarquia até que a parte superior da hierarquia, também conhecida como a autoridade raiz, seja atingida.</span><span class="sxs-lookup"><span data-stu-id="5c881-114">It is organized such that each CA is certified by another CA in a higher level of the hierarchy until the top of the hierarchy, also known as the root authority, is reached.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-115"><span id="_security_calg_dh_ephem_gly"></span><span id="_SECURITY_CALG_DH_EPHEM_GLY"></span>**CALG \_ DH \_ EPHEM**</span><span class="sxs-lookup"><span data-stu-id="5c881-115"><span id="_security_calg_dh_ephem_gly"></span><span id="_SECURITY_CALG_DH_EPHEM_GLY"></span>**CALG\_DH\_EPHEM**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-116">O identificador do algoritmo CryptoAPI para o algoritmo de troca de chave Diffie-Hellman quando usado para a geração de chaves efêmeras.</span><span class="sxs-lookup"><span data-stu-id="5c881-116">The CryptoAPI algorithm identifier for the Diffie-Hellman key-exchange algorithm when used for the generation of ephemeral keys.</span></span>

<span data-ttu-id="5c881-117">Consulte também [*algoritmo de troca de chave Diffie-Hellman (efêmero)*](d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5c881-117">See also [*Diffie-Hellman (ephemeral) key-exchange algorithm*](d-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-118"><span id="_security_calg_dh_sf_gly"></span><span id="_SECURITY_CALG_DH_SF_GLY"></span>**CALG \_ DH \_ it**</span><span class="sxs-lookup"><span data-stu-id="5c881-118"><span id="_security_calg_dh_sf_gly"></span><span id="_SECURITY_CALG_DH_SF_GLY"></span>**CALG\_DH\_SF**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-119">O identificador do algoritmo CryptoAPI para o algoritmo de troca de chave Diffie-Hellman quando usado para a geração de chaves de armazenamento e encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="5c881-119">The CryptoAPI algorithm identifier for the Diffie-Hellman key-exchange algorithm when used for the generation of store-and-forward keys.</span></span>

<span data-ttu-id="5c881-120">Consulte também [*algoritmo de troca de chaves Diffie-Hellman (armazenamento e encaminhamento)*](d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5c881-120">See also [*Diffie-Hellman (store and forward) key-exchange algorithm*](d-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-121"><span id="_security_calg_hmac_gly"></span><span id="_SECURITY_CALG_HMAC_GLY"></span>**\_HMAC CALG**</span><span class="sxs-lookup"><span data-stu-id="5c881-121"><span id="_security_calg_hmac_gly"></span><span id="_SECURITY_CALG_HMAC_GLY"></span>**CALG\_HMAC**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-122">O identificador do algoritmo CryptoAPI para o algoritmo de Message Authentication Code baseado em hash.</span><span class="sxs-lookup"><span data-stu-id="5c881-122">The CryptoAPI algorithm identifier for the hash-based Message Authentication Code algorithm.</span></span>

<span data-ttu-id="5c881-123">Consulte também [*Message Authentication Code com base em hash*](h-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5c881-123">See also [*Hash-Based Message Authentication Code*](h-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-124"><span id="_security_calg_mac_gly"></span><span id="_SECURITY_CALG_MAC_GLY"></span>**CALG \_ Mac**</span><span class="sxs-lookup"><span data-stu-id="5c881-124"><span id="_security_calg_mac_gly"></span><span id="_SECURITY_CALG_MAC_GLY"></span>**CALG\_MAC**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-125">O identificador do algoritmo CryptoAPI para o algoritmo de Message Authentication Code.</span><span class="sxs-lookup"><span data-stu-id="5c881-125">The CryptoAPI algorithm identifier for the Message Authentication Code algorithm.</span></span>

<span data-ttu-id="5c881-126">Consulte também [*Message Authentication Code*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5c881-126">See also [*Message Authentication Code*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-127"><span id="_security_calg_md2_gly"></span><span id="_SECURITY_CALG_MD2_GLY"></span>**CALG \_ MD2**</span><span class="sxs-lookup"><span data-stu-id="5c881-127"><span id="_security_calg_md2_gly"></span><span id="_SECURITY_CALG_MD2_GLY"></span>**CALG\_MD2**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-128">O identificador do algoritmo CryptoAPI para o algoritmo de hash MD2.</span><span class="sxs-lookup"><span data-stu-id="5c881-128">The CryptoAPI algorithm identifier for the MD2 hash algorithm.</span></span>

<span data-ttu-id="5c881-129">Consulte também [*algoritmo MD2*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5c881-129">See also [*MD2 algorithm*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-130"><span id="_security_calg_md5_gly"></span><span id="_SECURITY_CALG_MD5_GLY"></span>**CALG \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="5c881-130"><span id="_security_calg_md5_gly"></span><span id="_SECURITY_CALG_MD5_GLY"></span>**CALG\_MD5**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-131">O identificador do algoritmo CryptoAPI para o algoritmo de hash MD5.</span><span class="sxs-lookup"><span data-stu-id="5c881-131">The CryptoAPI algorithm identifier for the MD5 hash algorithm.</span></span>

<span data-ttu-id="5c881-132">Consulte também [*algoritmo MD5*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5c881-132">See also [*MD5 algorithm*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-133"><span id="_security_calg_rc2_gly"></span><span id="_SECURITY_CALG_RC2_GLY"></span>**CALG \_ RC2**</span><span class="sxs-lookup"><span data-stu-id="5c881-133"><span id="_security_calg_rc2_gly"></span><span id="_SECURITY_CALG_RC2_GLY"></span>**CALG\_RC2**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-134">O identificador do algoritmo CryptoAPI para o algoritmo de codificação de bloco RC2.</span><span class="sxs-lookup"><span data-stu-id="5c881-134">The CryptoAPI algorithm identifier for the RC2 block cipher algorithm.</span></span>

<span data-ttu-id="5c881-135">Consulte também [*algoritmo de bloqueio RC2*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5c881-135">See also [*RC2 block algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-136"><span id="_security_calg_rc4_gly"></span><span id="_SECURITY_CALG_RC4_GLY"></span>**CALG \_ RC4**</span><span class="sxs-lookup"><span data-stu-id="5c881-136"><span id="_security_calg_rc4_gly"></span><span id="_SECURITY_CALG_RC4_GLY"></span>**CALG\_RC4**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-137">O identificador do algoritmo CryptoAPI para o algoritmo de codificação de fluxo RC4.</span><span class="sxs-lookup"><span data-stu-id="5c881-137">The CryptoAPI algorithm identifier for the RC4 stream cipher algorithm.</span></span>

<span data-ttu-id="5c881-138">Consulte também [*algoritmo de fluxo RC4*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5c881-138">See also [*RC4 stream algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-139"><span id="_security_calg_rsa_keyx_gly"></span><span id="_SECURITY_CALG_RSA_KEYX_GLY"></span>**CALG \_ RSA \_ KEYX**</span><span class="sxs-lookup"><span data-stu-id="5c881-139"><span id="_security_calg_rsa_keyx_gly"></span><span id="_SECURITY_CALG_RSA_KEYX_GLY"></span>**CALG\_RSA\_KEYX**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-140">O identificador do algoritmo CryptoAPI para o algoritmo de chave pública RSA quando usado para troca de chaves.</span><span class="sxs-lookup"><span data-stu-id="5c881-140">The CryptoAPI algorithm identifier for the RSA public key algorithm when used for key exchange.</span></span>

<span data-ttu-id="5c881-141">Consulte também [*algoritmo de chave pública RSA*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5c881-141">See also [*RSA public key algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-142"><span id="_security_calg_rsa_sign_gly"></span><span id="_SECURITY_CALG_RSA_SIGN_GLY"></span>**CALG \_ \_ assinatura RSA**</span><span class="sxs-lookup"><span data-stu-id="5c881-142"><span id="_security_calg_rsa_sign_gly"></span><span id="_SECURITY_CALG_RSA_SIGN_GLY"></span>**CALG\_RSA\_SIGN**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-143">O identificador do algoritmo CryptoAPI para o algoritmo de chave pública RSA quando usado para gerar assinaturas digitais.</span><span class="sxs-lookup"><span data-stu-id="5c881-143">The CryptoAPI algorithm identifier for the RSA public key algorithm when used to generate digital signatures.</span></span>

<span data-ttu-id="5c881-144">Consulte também [*algoritmo de chave pública RSA*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5c881-144">See also [*RSA public key algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-145"><span id="_security_calg_sha_gly"></span><span id="_SECURITY_CALG_SHA_GLY"></span>**CALG \_ Sha**</span><span class="sxs-lookup"><span data-stu-id="5c881-145"><span id="_security_calg_sha_gly"></span><span id="_SECURITY_CALG_SHA_GLY"></span>**CALG\_SHA**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-146">O identificador do algoritmo CryptoAPI para o algoritmo de hash seguro (SHA-1).</span><span class="sxs-lookup"><span data-stu-id="5c881-146">The CryptoAPI algorithm identifier for the Secure Hash Algorithm (SHA-1).</span></span>

<span data-ttu-id="5c881-147">Consulte também [*algoritmo de hash seguro*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5c881-147">See also [*Secure Hash Algorithm*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-148"><span id="_security_cast_gly"></span><span id="_SECURITY_CAST_GLY"></span>**VERTIDA**</span><span class="sxs-lookup"><span data-stu-id="5c881-148"><span id="_security_cast_gly"></span><span id="_SECURITY_CAST_GLY"></span>**CAST**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-149">Um grupo de codificações de bloco simétricos do tipo DES desenvolvido pela C. M.</span><span class="sxs-lookup"><span data-stu-id="5c881-149">A group of DES-like symmetric block ciphers developed by C. M.</span></span> <span data-ttu-id="5c881-150">Adams e S. E.</span><span class="sxs-lookup"><span data-stu-id="5c881-150">Adams and S. E.</span></span> <span data-ttu-id="5c881-151">Tavares.</span><span class="sxs-lookup"><span data-stu-id="5c881-151">Tavares.</span></span> <span data-ttu-id="5c881-152">Os \_ \_ tipos de provedor Prov MS Exchange especificam um algoritmo de conversão específico que usa um tamanho de bloco de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5c881-152">PROV\_MS\_EXCHANGE provider types specify a particular CAST algorithm that uses a 64-bit block size.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-153"><span id="_security_cbc_gly"></span><span id="_SECURITY_CBC_GLY"></span>**CBC**</span><span class="sxs-lookup"><span data-stu-id="5c881-153"><span id="_security_cbc_gly"></span><span id="_SECURITY_CBC_GLY"></span>**CBC**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-154">Consulte *encadeamento de blocos de codificação*.</span><span class="sxs-lookup"><span data-stu-id="5c881-154">See *Cipher Block Chaining*.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-155"><span id="_security_certificate_gly"></span><span id="_SECURITY_CERTIFICATE_GLY"></span>**Certificate**</span><span class="sxs-lookup"><span data-stu-id="5c881-155"><span id="_security_certificate_gly"></span><span id="_SECURITY_CERTIFICATE_GLY"></span>**certificate**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-156">Uma instrução assinada digitalmente que contém informações sobre uma entidade e a chave pública da entidade, associando essas duas informações juntas.</span><span class="sxs-lookup"><span data-stu-id="5c881-156">A digitally signed statement that contains information about an entity and the entity's public key, thus binding these two pieces of information together.</span></span> <span data-ttu-id="5c881-157">Um certificado é emitido por uma organização (ou entidade) confiável chamada de autoridade de *certificação* (CA) depois que a AC verificou que a entidade é quem diz ser.</span><span class="sxs-lookup"><span data-stu-id="5c881-157">A certificate is issued by a trusted organization (or entity) called a *certification authority* (CA) after the CA has verified that the entity is who it says it is.</span></span>

<span data-ttu-id="5c881-158">Os certificados podem conter tipos diferentes de dados.</span><span class="sxs-lookup"><span data-stu-id="5c881-158">Certificates can contain different types of data.</span></span> <span data-ttu-id="5c881-159">Por exemplo, um certificado X. 509 inclui o formato do certificado, o número de série do certificado, o algoritmo usado para assinar o certificado, o nome da autoridade de certificação que emitiu o certificado, o nome e a chave pública da entidade que solicita o certificado e a assinatura da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="5c881-159">For example, an X.509 certificate includes the format of the certificate, the serial number of the certificate, the algorithm used to sign the certificate, the name of the CA that issued the certificate, the name and public key of the entity requesting the certificate, and the CA's signature.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-160"><span id="_security_certificate_blob_gly"></span><span id="_SECURITY_CERTIFICATE_BLOB_GLY"></span>**BLOB de certificado**</span><span class="sxs-lookup"><span data-stu-id="5c881-160"><span id="_security_certificate_blob_gly"></span><span id="_SECURITY_CERTIFICATE_BLOB_GLY"></span>**certificate BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-161">Um BLOB que contém os dados do certificado.</span><span class="sxs-lookup"><span data-stu-id="5c881-161">A BLOB that contains the certificate data.</span></span>

<span data-ttu-id="5c881-162">Um BLOB de certificado é criado por chamadas para **CryptEncodeObject**.</span><span class="sxs-lookup"><span data-stu-id="5c881-162">A certificate BLOB is created by calls to **CryptEncodeObject**.</span></span> <span data-ttu-id="5c881-163">O processo é concluído quando a saída da chamada contém todos os dados do certificado.</span><span class="sxs-lookup"><span data-stu-id="5c881-163">The process is complete when the output of the call contains all the certificate data.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-164"><span id="_security_certificate_context_gly"></span><span id="_SECURITY_CERTIFICATE_CONTEXT_GLY"></span>**contexto do certificado**</span><span class="sxs-lookup"><span data-stu-id="5c881-164"><span id="_security_certificate_context_gly"></span><span id="_SECURITY_CERTIFICATE_CONTEXT_GLY"></span>**certificate context**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-165">Uma estrutura de contexto de certificado \_ que contém um identificador para um repositório de certificados, um ponteiro para o blob de certificado codificado original, um ponteiro para uma estrutura de informações de certificado \_ e um membro de tipo de codificação.</span><span class="sxs-lookup"><span data-stu-id="5c881-165">A CERT\_CONTEXT structure that contains a handle to a certificate store, a pointer to the original encoded certificate BLOB, a pointer to a CERT\_INFO structure, and an encoding type member.</span></span> <span data-ttu-id="5c881-166">É a estrutura **de \_ informações** de certificado que contém a maioria das informações de certificado.</span><span class="sxs-lookup"><span data-stu-id="5c881-166">It is the **CERT\_INFO** structure that contains most of the certificate information.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-167"><span id="_security_certificate_encode_decode_functions_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODE_DECODE_FUNCTIONS_GLY"></span>**funções de codificação/decodificação de certificado**</span><span class="sxs-lookup"><span data-stu-id="5c881-167"><span id="_security_certificate_encode_decode_functions_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODE_DECODE_FUNCTIONS_GLY"></span>**certificate encode/decode functions**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-168">Funções que gerenciam a tradução de certificados e material relacionado em formatos binários padrão que podem ser usados em ambientes diferentes.</span><span class="sxs-lookup"><span data-stu-id="5c881-168">Functions that manage the translation of certificates and related material into standard, binary formats that can be used in different environments.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-169"><span id="_security_certificate_encoding_type_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODING_TYPE_GLY"></span>**tipo de codificação de certificado**</span><span class="sxs-lookup"><span data-stu-id="5c881-169"><span id="_security_certificate_encoding_type_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODING_TYPE_GLY"></span>**certificate encoding type**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-170">Define como o certificado é codificado.</span><span class="sxs-lookup"><span data-stu-id="5c881-170">Defines how the certificate is encoded.</span></span> <span data-ttu-id="5c881-171">O tipo de codificação de certificado é armazenado na palavra de ordem inferior da estrutura de tipo de codificação (**DWORD**).</span><span class="sxs-lookup"><span data-stu-id="5c881-171">The certificate encoding type is stored in the low-order word of the encoding type (**DWORD**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-172"><span id="_security_certificate_management_over_cms_gly"></span><span id="_SECURITY_CERTIFICATE_MANAGEMENT_OVER_CMS_GLY"></span>**Gerenciamento de certificados sobre o CMS**</span><span class="sxs-lookup"><span data-stu-id="5c881-172"><span id="_security_certificate_management_over_cms_gly"></span><span id="_SECURITY_CERTIFICATE_MANAGEMENT_OVER_CMS_GLY"></span>**Certificate Management over CMS**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-173">CMC.</span><span class="sxs-lookup"><span data-stu-id="5c881-173">CMC.</span></span> <span data-ttu-id="5c881-174">Gerenciamento de certificados sobre o CMS.</span><span class="sxs-lookup"><span data-stu-id="5c881-174">Certificate Management over CMS.</span></span> <span data-ttu-id="5c881-175">O CMC é um protocolo de gerenciamento de certificados que usa a sintaxe de mensagem criptográfica (CMS).</span><span class="sxs-lookup"><span data-stu-id="5c881-175">CMC is a certificate management protocol that uses Cryptographic Message Syntax (CMS).</span></span> <span data-ttu-id="5c881-176">A Microsoft encapsula solicitações de certificado CMC em um objeto de solicitação [*PKCS \# 7*](p-gly.md) (CMS) antes de enviar a solicitação para um servidor de registro.</span><span class="sxs-lookup"><span data-stu-id="5c881-176">Microsoft wraps CMC certificate requests in a [*PKCS \#7*](p-gly.md) (CMS) request object before sending the request to an enrollment server.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-177"><span id="_security_certificate_name_blob_gly"></span><span id="_SECURITY_CERTIFICATE_NAME_BLOB_GLY"></span>**BLOB do nome do certificado**</span><span class="sxs-lookup"><span data-stu-id="5c881-177"><span id="_security_certificate_name_blob_gly"></span><span id="_SECURITY_CERTIFICATE_NAME_BLOB_GLY"></span>**certificate name BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-178">Uma representação codificada das informações de nome incluídas em certificados.</span><span class="sxs-lookup"><span data-stu-id="5c881-178">An encoded representation of the name information that is included in certificates.</span></span> <span data-ttu-id="5c881-179">Cada BLOB de nome é mapeado para uma estrutura de **\_ \_ blob de nome de certificado** .</span><span class="sxs-lookup"><span data-stu-id="5c881-179">Each name BLOB is mapped to a **CERT\_NAME\_BLOB** structure.</span></span>

<span data-ttu-id="5c881-180">Por exemplo, as informações de emissor e assunto referenciadas por uma estrutura de **\_ informações de certificado** são armazenadas em duas estruturas de **blob de \_ nome \_ de certificado** .</span><span class="sxs-lookup"><span data-stu-id="5c881-180">For example, the issuer and subject information referenced by a **CERT\_INFO** structure is stored in two **CERT\_NAME\_BLOB** structures.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-181"><span id="_security_certificate_policy_gly"></span><span id="_SECURITY_CERTIFICATE_POLICY_GLY"></span>**política de certificado**</span><span class="sxs-lookup"><span data-stu-id="5c881-181"><span id="_security_certificate_policy_gly"></span><span id="_SECURITY_CERTIFICATE_POLICY_GLY"></span>**certificate policy**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-182">Um conjunto nomeado de regras que indicam a aplicabilidade de certificados para uma classe específica de aplicativos com requisitos de segurança comuns.</span><span class="sxs-lookup"><span data-stu-id="5c881-182">A named set of rules that indicate the applicability of certificates for a specific class of applications with common security requirements.</span></span> <span data-ttu-id="5c881-183">Essa política pode, por exemplo, limitar determinados certificados a transações de intercâmbio de dados eletrônicos dentro de determinados limites de preço.</span><span class="sxs-lookup"><span data-stu-id="5c881-183">Such a policy might, for example, limit certain certificates to electronic data interchange transactions within given price limits.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-184"><span id="_security_certificate_request_gly"></span><span id="_SECURITY_CERTIFICATE_REQUEST_GLY"></span>**solicitação de certificado**</span><span class="sxs-lookup"><span data-stu-id="5c881-184"><span id="_security_certificate_request_gly"></span><span id="_SECURITY_CERTIFICATE_REQUEST_GLY"></span>**certificate request**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-185">Uma mensagem eletrônica especialmente formatada (enviada para uma AC) usada para solicitar um certificado.</span><span class="sxs-lookup"><span data-stu-id="5c881-185">A specially formatted electronic message (sent to a CA) used to request a certificate.</span></span> <span data-ttu-id="5c881-186">A solicitação deve conter as informações exigidas pela autoridade de certificação para autenticar a solicitação, além da chave pública da entidade que solicita o certificado.</span><span class="sxs-lookup"><span data-stu-id="5c881-186">The request must contain the information required by the CA to authenticate the request, plus the public key of the entity requesting the certificate.</span></span>

<span data-ttu-id="5c881-187">Todas as informações necessárias para criar a solicitação são mapeadas para uma estrutura de **\_ \_ informações de solicitação de certificado** .</span><span class="sxs-lookup"><span data-stu-id="5c881-187">All the information necessary to create the request is mapped to a **CERT\_REQUEST\_INFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-188"><span id="_security_certificate_revocation_list_gly"></span><span id="_SECURITY_CERTIFICATE_REVOCATION_LIST_GLY"></span>**lista de certificados revogados**</span><span class="sxs-lookup"><span data-stu-id="5c881-188"><span id="_security_certificate_revocation_list_gly"></span><span id="_SECURITY_CERTIFICATE_REVOCATION_LIST_GLY"></span>**certificate revocation list**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-189">REVOGA Um documento mantido e publicado por uma autoridade de certificação (CA) que lista os certificados emitidos pela AC que não são mais válidos.</span><span class="sxs-lookup"><span data-stu-id="5c881-189">(CRL) A document maintained and published by a certification authority (CA) that lists certificates issued by the CA that are no longer valid.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-190"><span id="_security_certificate_server_gly"></span><span id="_SECURITY_CERTIFICATE_SERVER_GLY"></span>**servidor de certificado**</span><span class="sxs-lookup"><span data-stu-id="5c881-190"><span id="_security_certificate_server_gly"></span><span id="_SECURITY_CERTIFICATE_SERVER_GLY"></span>**certificate server**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-191">Um servidor que emite certificados para uma determinada autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="5c881-191">A server that issues certificates for a particular CA.</span></span> <span data-ttu-id="5c881-192">O software do servidor de certificado fornece serviços personalizáveis para emissão e gerenciamento de certificados usados em sistemas de segurança que empregam criptografia de chave pública.</span><span class="sxs-lookup"><span data-stu-id="5c881-192">The certificate server software provides customizable services for issuing and managing certificates used in security systems that employ public key cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-193"><span id="_security_certificate_services_gly"></span><span id="_SECURITY_CERTIFICATE_SERVICES_GLY"></span>**Serviços de certificados**</span><span class="sxs-lookup"><span data-stu-id="5c881-193"><span id="_security_certificate_services_gly"></span><span id="_SECURITY_CERTIFICATE_SERVICES_GLY"></span>**Certificate Services**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-194">Um serviço de software que emite certificados para uma *autoridade de certificação* (CA) específica.</span><span class="sxs-lookup"><span data-stu-id="5c881-194">A software service that issues certificates for a particular *certification authority* (CA).</span></span> <span data-ttu-id="5c881-195">Ele fornece serviços personalizáveis para emitir e gerenciar certificados para a empresa.</span><span class="sxs-lookup"><span data-stu-id="5c881-195">It provides customizable services for issuing and managing certificates for the enterprise.</span></span> <span data-ttu-id="5c881-196">Os certificados podem ser usados para fornecer suporte de autenticação, incluindo email seguro, autenticação baseada na Web e autenticação de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="5c881-196">Certificates can be used to provide authentication support, including secure email, web-based authentication, and smart card authentication.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-197"><span id="_security_certificate_store_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_GLY"></span>**repositório de certificados**</span><span class="sxs-lookup"><span data-stu-id="5c881-197"><span id="_security_certificate_store_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_GLY"></span>**certificate store**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-198">Normalmente, um armazenamento permanente em que certificados, CRLs (listas de certificados revogados) e listas de certificados confiáveis (CTLs) são armazenados.</span><span class="sxs-lookup"><span data-stu-id="5c881-198">Typically, a permanent storage where certificates, certificate revocation lists (CRLs), and certificate trust lists (CTLs) are stored.</span></span> <span data-ttu-id="5c881-199">No entanto, é possível criar e abrir um repositório de certificados somente na memória ao trabalhar com certificados que não precisam ser colocados no armazenamento permanente.</span><span class="sxs-lookup"><span data-stu-id="5c881-199">It is possible, however, to create and open a certificate store solely in memory when working with certificates that do not need to be put in permanent storage.</span></span>

<span data-ttu-id="5c881-200">O repositório de certificados é fundamental para grande parte da funcionalidade de certificado no CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="5c881-200">The certificate store is central to much of the certificate functionality in CryptoAPI.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-201"><span id="_security_certificate_store_functions_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_FUNCTIONS_GLY"></span>**funções de repositório de certificados**</span><span class="sxs-lookup"><span data-stu-id="5c881-201"><span id="_security_certificate_store_functions_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_FUNCTIONS_GLY"></span>**certificate store functions**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-202">Funções que gerenciam os dados de armazenamento e recuperação, como certificados, listas de certificados revogados (CRLs) e listas de certificados confiáveis (CTLs).</span><span class="sxs-lookup"><span data-stu-id="5c881-202">Functions that manage the storage and retrieval data such as certificates, certificate revocation lists (CRLs), and certificate trust lists (CTLs).</span></span> <span data-ttu-id="5c881-203">Essas funções podem ser separadas em funções de certificado comuns, funções de lista de certificados revogados e funções de lista de certificados confiáveis.</span><span class="sxs-lookup"><span data-stu-id="5c881-203">These functions can be separated into common certificate functions, certificate revocation list functions, and certificate trust list functions.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-204"><span id="_security_certificate_template_gly"></span><span id="_SECURITY_CERTIFICATE_TEMPLATE_GLY"></span>**modelo de certificado**</span><span class="sxs-lookup"><span data-stu-id="5c881-204"><span id="_security_certificate_template_gly"></span><span id="_SECURITY_CERTIFICATE_TEMPLATE_GLY"></span>**certificate template**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-205">Uma construção do Windows que faz o perfil de certificados (ou seja, ele Predefine o formato e o conteúdo) com base no uso pretendido.</span><span class="sxs-lookup"><span data-stu-id="5c881-205">A Windows construct that profiles certificates (that is, it prespecifies the format and content) based on their intended usage.</span></span> <span data-ttu-id="5c881-206">Ao solicitar um [*certificado*](/windows) de uma autoridade de *certificação* (CA) corporativa do Windows, os solicitantes de certificado são, dependendo de seus direitos de acesso, capazes de selecionar entre uma variedade de tipos de certificado baseados em modelos de certificado, como usuário e assinatura de código.</span><span class="sxs-lookup"><span data-stu-id="5c881-206">When requesting a [*certificate*](/windows) from a Windows enterprise *certification authority* (CA), certificate requesters are, depending on their access rights, able to select from a variety of certificate types that are based on certificate templates, such as User and Code Signing.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-207"><span id="_security_certificate_trust_list_gly"></span><span id="_SECURITY_CERTIFICATE_TRUST_LIST_GLY"></span>**lista de certificados confiáveis**</span><span class="sxs-lookup"><span data-stu-id="5c881-207"><span id="_security_certificate_trust_list_gly"></span><span id="_SECURITY_CERTIFICATE_TRUST_LIST_GLY"></span>**certificate trust list**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-208">CERTIFICADOS Uma lista predefinida de itens que foram assinados por uma entidade confiável.</span><span class="sxs-lookup"><span data-stu-id="5c881-208">(CTL) A predefined list of items that have been signed by a trusted entity.</span></span> <span data-ttu-id="5c881-209">Uma CTL pode ser qualquer coisa, como uma lista de hashes de certificados ou uma lista de nomes de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5c881-209">A CTL can be anything, such as a list of hashes of certificates, or a list of file names.</span></span> <span data-ttu-id="5c881-210">Todos os itens da lista são autenticados (aprovados) pela entidade de assinatura.</span><span class="sxs-lookup"><span data-stu-id="5c881-210">All the items in the list are authenticated (approved) by the signing entity.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-211"><span id="_security_certification_authority_gly"></span><span id="_SECURITY_CERTIFICATION_AUTHORITY_GLY"></span>**autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="5c881-211"><span id="_security_certification_authority_gly"></span><span id="_SECURITY_CERTIFICATION_AUTHORITY_GLY"></span>**certification authority**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-212">AC Uma entidade confiável para emitir certificados que afirmam que o indivíduo, o computador ou a organização do destinatário solicitando o certificado atende às condições de uma política estabelecida.</span><span class="sxs-lookup"><span data-stu-id="5c881-212">(CA) An entity entrusted to issue certificates that assert that the recipient individual, computer, or organization requesting the certificate fulfills the conditions of an established policy.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-213"><span id="_security_cfb_gly"></span><span id="_SECURITY_CFB_GLY"></span>**CFB**</span><span class="sxs-lookup"><span data-stu-id="5c881-213"><span id="_security_cfb_gly"></span><span id="_SECURITY_CFB_GLY"></span>**CFB**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-214">Consulte *comentários de codificação*.</span><span class="sxs-lookup"><span data-stu-id="5c881-214">See *Cipher Feedback*.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-215"><span id="_security_chaining_mode_gly"></span><span id="_SECURITY_CHAINING_MODE_GLY"></span>**modo de encadeamento**</span><span class="sxs-lookup"><span data-stu-id="5c881-215"><span id="_security_chaining_mode_gly"></span><span id="_SECURITY_CHAINING_MODE_GLY"></span>**chaining mode**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-216">Um modo de codificação de bloco que apresenta comentários combinando texto cifrado e texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="5c881-216">A block cipher mode that introduces feedback by combining ciphertext and plaintext.</span></span>

<span data-ttu-id="5c881-217">Consulte também *encadeamento de blocos de codificação*.</span><span class="sxs-lookup"><span data-stu-id="5c881-217">See also *Cipher Block Chaining*.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-218"><span id="_security_cipher_gly"></span><span id="_SECURITY_CIPHER_GLY"></span>**codificação**</span><span class="sxs-lookup"><span data-stu-id="5c881-218"><span id="_security_cipher_gly"></span><span id="_SECURITY_CIPHER_GLY"></span>**cipher**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-219">Um algoritmo criptográfico usado para criptografar dados; ou seja, para transformar o texto não criptografado em texto cifrado usando uma chave predefinida.</span><span class="sxs-lookup"><span data-stu-id="5c881-219">A cryptographic algorithm used to encrypt data; that is, to transform plaintext into ciphertext using a predefined key.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-220"><span id="_security_cipher_block_chaining_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_GLY"></span>**Encadeamento de blocos de codificação**</span><span class="sxs-lookup"><span data-stu-id="5c881-220"><span id="_security_cipher_block_chaining_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_GLY"></span>**Cipher Block Chaining**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-221">CBC Um método de operar uma codificação de bloco simétrico que usa comentários para combinar texto cifrado gerado anteriormente com novo texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="5c881-221">(CBC) A method of operating a symmetric block cipher that uses feedback to combine previously generated ciphertext with new plaintext.</span></span>

<span data-ttu-id="5c881-222">Cada bloco de texto não criptografado é combinado com o texto cifrado do bloco anterior por uma operação de **XOR** de bit-a-passo antes de ser criptografado.</span><span class="sxs-lookup"><span data-stu-id="5c881-222">Each plaintext block is combined with the ciphertext of the previous block by a bitwise-**XOR** operation before it is encrypted.</span></span> <span data-ttu-id="5c881-223">Combinar texto cifrado e texto não criptografado garante que, mesmo que o texto não contenha muitos blocos idênticos, eles serão criptografados para um bloco de texto cifrado diferente.</span><span class="sxs-lookup"><span data-stu-id="5c881-223">Combining ciphertext and plaintext ensures that even if the plaintext contains many identical blocks, they will each encrypt to a different ciphertext block.</span></span>

<span data-ttu-id="5c881-224">Quando o provedor Microsoft Base Cryptographic é usado, o CBC é o modo de codificação padrão.</span><span class="sxs-lookup"><span data-stu-id="5c881-224">When the Microsoft Base Cryptographic Provider is used, CBC is the default cipher mode.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-225"><span id="_security_cipher_block_chaining_mac_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_MAC_GLY"></span>**Cadeia de encadeamento de bloco de codificação MAC**</span><span class="sxs-lookup"><span data-stu-id="5c881-225"><span id="_security_cipher_block_chaining_mac_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_MAC_GLY"></span>**Cipher Block Chaining MAC**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-226">Um método de codificação de bloco que criptografa os dados base com uma codificação de bloco e, em seguida, usa o último bloco criptografado como o valor de hash.</span><span class="sxs-lookup"><span data-stu-id="5c881-226">A block cipher method that encrypts the base data with a block cipher and then uses the last encrypted block as the hash value.</span></span> <span data-ttu-id="5c881-227">O algoritmo de criptografia usado para criar o [*Message Authentication Code*](m-gly.md) (Mac) é aquele que foi especificado quando a chave de sessão foi criada.</span><span class="sxs-lookup"><span data-stu-id="5c881-227">The encryption algorithm used to build the [*Message Authentication Code*](m-gly.md) (MAC) is the one that was specified when the session key was created.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-228"><span id="_security_cipher_feedback_gly"></span><span id="_SECURITY_CIPHER_FEEDBACK_GLY"></span>**Comentários de codificação**</span><span class="sxs-lookup"><span data-stu-id="5c881-228"><span id="_security_cipher_feedback_gly"></span><span id="_SECURITY_CIPHER_FEEDBACK_GLY"></span>**Cipher Feedback**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-229">CFB Um modo de codificação de bloco que processa pequenos incrementos de texto não criptografado em texto cifrado, em vez de processar um bloco inteiro por vez.</span><span class="sxs-lookup"><span data-stu-id="5c881-229">(CFB) A block cipher mode that processes small increments of plaintext into ciphertext, instead of processing an entire block at a time.</span></span>

<span data-ttu-id="5c881-230">Esse modo usa um registro de mudança que tem um tamanho de bloco em comprimento e dividido em seções.</span><span class="sxs-lookup"><span data-stu-id="5c881-230">This mode uses a shift register that is one block size in length and divided into sections.</span></span> <span data-ttu-id="5c881-231">Por exemplo, se o tamanho do bloco for de 64 bits com oito bits processados por vez, o registro de turnos será dividido em oito seções.</span><span class="sxs-lookup"><span data-stu-id="5c881-231">For example, if the block size is 64 bits with eight bits processed at a time, then the shift register would be divided into eight sections.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-232"><span id="_security_cipher_mode_gly"></span><span id="_SECURITY_CIPHER_MODE_GLY"></span>**modo de codificação**</span><span class="sxs-lookup"><span data-stu-id="5c881-232"><span id="_security_cipher_mode_gly"></span><span id="_SECURITY_CIPHER_MODE_GLY"></span>**cipher mode**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-233">Um modo de codificação de bloco (cada bloco é criptografado individualmente) que pode ser especificado usando a função **CryptSetKeyParam** .</span><span class="sxs-lookup"><span data-stu-id="5c881-233">A block cipher mode (each block is encrypted individually) that can be specified by using the **CryptSetKeyParam** function.</span></span> <span data-ttu-id="5c881-234">Se o aplicativo não especificar explicitamente um desses modos, o modo de codificação CBC (encadeamento de blocos de codificação) será usado.</span><span class="sxs-lookup"><span data-stu-id="5c881-234">If the application does not explicitly specify one of these modes, then the cipher block chaining (CBC) cipher mode is used.</span></span>

<span data-ttu-id="5c881-235">ECB: um modo de codificação de bloco que não usa nenhum comentário.</span><span class="sxs-lookup"><span data-stu-id="5c881-235">ECB: A block cipher mode that uses no feedback.</span></span>

<span data-ttu-id="5c881-236">CBC: um modo de codificação de bloco que apresenta comentários combinando texto cifrado e texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="5c881-236">CBC: A block cipher mode that introduces feedback by combining ciphertext and plaintext.</span></span>

<span data-ttu-id="5c881-237">CFB: um modo de codificação de bloco que processa pequenos incrementos de texto não criptografado em texto cifrado, em vez de processar um bloco inteiro por vez.</span><span class="sxs-lookup"><span data-stu-id="5c881-237">CFB: A block cipher mode that processes small increments of plaintext into ciphertext, instead of processing an entire block at a time.</span></span>

<span data-ttu-id="5c881-238">OFB: um modo de codificação de bloco que usa comentários semelhantes a CFB.</span><span class="sxs-lookup"><span data-stu-id="5c881-238">OFB: A block cipher mode that uses feedback similar to CFB.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-239"><span id="_security_ciphertext_gly"></span><span id="_SECURITY_CIPHERTEXT_GLY"></span>**cifra**</span><span class="sxs-lookup"><span data-stu-id="5c881-239"><span id="_security_ciphertext_gly"></span><span id="_SECURITY_CIPHERTEXT_GLY"></span>**ciphertext**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-240">Uma mensagem que foi criptografada.</span><span class="sxs-lookup"><span data-stu-id="5c881-240">A message that has been encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-241"><span id="_security_cleartext_gly"></span><span id="_SECURITY_CLEARTEXT_GLY"></span>**criptografa**</span><span class="sxs-lookup"><span data-stu-id="5c881-241"><span id="_security_cleartext_gly"></span><span id="_SECURITY_CLEARTEXT_GLY"></span>**cleartext**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-242">Consulte [*texto não criptografado*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5c881-242">See [*plaintext*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-243"><span id="_security_client_gly"></span><span id="_SECURITY_CLIENT_GLY"></span>**cliente**</span><span class="sxs-lookup"><span data-stu-id="5c881-243"><span id="_security_client_gly"></span><span id="_SECURITY_CLIENT_GLY"></span>**client**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-244">O aplicativo, em vez do aplicativo de servidor, que inicia uma conexão com um servidor.</span><span class="sxs-lookup"><span data-stu-id="5c881-244">The application, rather than the server application, that initiates a connection to a server.</span></span>

<span data-ttu-id="5c881-245">Comparar com [*servidor*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5c881-245">Compare with [*server*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-246"><span id="_security_client_certificate_gly"></span><span id="_SECURITY_CLIENT_CERTIFICATE_GLY"></span>**certificado do cliente**</span><span class="sxs-lookup"><span data-stu-id="5c881-246"><span id="_security_client_certificate_gly"></span><span id="_SECURITY_CLIENT_CERTIFICATE_GLY"></span>**client certificate**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-247">Refere-se a um certificado usado para autenticação de cliente, como autenticar um navegador da Web em um servidor Web.</span><span class="sxs-lookup"><span data-stu-id="5c881-247">Refers to a certificate used for client authentication, such as authenticating a web browser on a web server.</span></span> <span data-ttu-id="5c881-248">Quando um cliente de navegador da Web tenta acessar um servidor Web seguro, o cliente envia seu certificado ao servidor para permitir que ele verifique a identidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="5c881-248">When a web browser client attempts to access a secured web server, the client sends its certificate to the server to allow it to verify the client's identity.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-249"><span id="_security_cmc_gly"></span><span id="_SECURITY_CMC_GLY"></span>**CMC**</span><span class="sxs-lookup"><span data-stu-id="5c881-249"><span id="_security_cmc_gly"></span><span id="_SECURITY_CMC_GLY"></span>**CMC**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-250">Consulte *Gerenciamento de certificados sobre o CMS*.</span><span class="sxs-lookup"><span data-stu-id="5c881-250">See *Certificate Management over CMS*.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-251"><span id="_security_cng_gly"></span><span id="_SECURITY_CNG_GLY"></span>**CNG**</span><span class="sxs-lookup"><span data-stu-id="5c881-251"><span id="_security_cng_gly"></span><span id="_SECURITY_CNG_GLY"></span>**CNG**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-252">Consulte *API de criptografia: próxima geração*.</span><span class="sxs-lookup"><span data-stu-id="5c881-252">See *Cryptography API: Next Generation*.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-253"><span id="_security_communication_protocol_gly"></span><span id="_SECURITY_COMMUNICATION_PROTOCOL_GLY"></span>**Protocolo de comunicação**</span><span class="sxs-lookup"><span data-stu-id="5c881-253"><span id="_security_communication_protocol_gly"></span><span id="_SECURITY_COMMUNICATION_PROTOCOL_GLY"></span>**communication protocol**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-254">O método no qual os dados são serializados (convertidos em uma cadeia de caracteres e zeros) e desserializados.</span><span class="sxs-lookup"><span data-stu-id="5c881-254">The method in which data is serialized (converted to a string of ones and zeros) and deserialized.</span></span> <span data-ttu-id="5c881-255">O protocolo é controlado pelo hardware de transmissão de dados e software.</span><span class="sxs-lookup"><span data-stu-id="5c881-255">The protocol is controlled by both software and data-transmission hardware.</span></span>

<span data-ttu-id="5c881-256">Normalmente discutido em termos de camadas, um protocolo de comunicação simplificado pode consistir em uma camada de aplicativo, uma camada de codificação/decodificação e uma camada de hardware.</span><span class="sxs-lookup"><span data-stu-id="5c881-256">Typically discussed in terms of layers, a simplified communication protocol might consist of an application layer, encode/decode layer, and hardware layer.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-257"><span id="_security_constrained_delegation_gly"></span><span id="_SECURITY_CONSTRAINED_DELEGATION_GLY"></span>**delegação restrita**</span><span class="sxs-lookup"><span data-stu-id="5c881-257"><span id="_security_constrained_delegation_gly"></span><span id="_SECURITY_CONSTRAINED_DELEGATION_GLY"></span>**constrained delegation**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-258">Comportamento que permite que o servidor encaminhe solicitações em nome do cliente somente para uma lista especificada de serviços.</span><span class="sxs-lookup"><span data-stu-id="5c881-258">Behavior that allows the server to forward requests on behalf of the client only to a specified list of services.</span></span>

<span data-ttu-id="5c881-259">**Windows XP:** Não há suporte para a delegação restrita.</span><span class="sxs-lookup"><span data-stu-id="5c881-259">**Windows XP:** Constrained delegation is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-260"><span id="_security_context_gly"></span><span id="_SECURITY_CONTEXT_GLY"></span>**noticioso**</span><span class="sxs-lookup"><span data-stu-id="5c881-260"><span id="_security_context_gly"></span><span id="_SECURITY_CONTEXT_GLY"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-261">Os dados de segurança relevantes para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="5c881-261">The security data relevant to a connection.</span></span> <span data-ttu-id="5c881-262">Um contexto contém informações como uma chave de sessão e a duração da sessão.</span><span class="sxs-lookup"><span data-stu-id="5c881-262">A context contains information such as a session key and duration of the session.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-263"><span id="_security_context_function_gly"></span><span id="_SECURITY_CONTEXT_FUNCTION_GLY"></span>**função de contexto**</span><span class="sxs-lookup"><span data-stu-id="5c881-263"><span id="_security_context_function_gly"></span><span id="_SECURITY_CONTEXT_FUNCTION_GLY"></span>**context function**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-264">Funções usadas para se conectar a um CSP (provedor de serviços de criptografia).</span><span class="sxs-lookup"><span data-stu-id="5c881-264">Functions used to connect to a cryptographic service provider (CSP).</span></span> <span data-ttu-id="5c881-265">Essas funções permitem que os aplicativos escolham um CSP específico por nome ou obtenham um com uma classe necessária de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="5c881-265">These functions enable applications to choose a specific CSP by name or get one with a needed class of functionality.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-266"><span id="_security_countersignature_gly"></span><span id="_SECURITY_COUNTERSIGNATURE_GLY"></span>**referenda**</span><span class="sxs-lookup"><span data-stu-id="5c881-266"><span id="_security_countersignature_gly"></span><span id="_SECURITY_COUNTERSIGNATURE_GLY"></span>**countersignature**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-267">Uma assinatura de uma assinatura e mensagem existente ou uma assinatura de uma assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="5c881-267">A signature of an existing signature and message or a signature of an existing signature.</span></span> <span data-ttu-id="5c881-268">Uma referenda é usada para assinar o hash criptografado de uma assinatura existente ou para o carimbo de data/hora de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="5c881-268">A countersignature is used to sign the encrypted hash of an existing signature or to time stamp a message.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-269"><span id="_security_credentials_gly"></span><span id="_SECURITY_CREDENTIALS_GLY"></span>**fornecidas**</span><span class="sxs-lookup"><span data-stu-id="5c881-269"><span id="_security_credentials_gly"></span><span id="_SECURITY_CREDENTIALS_GLY"></span>**credentials**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-270">Dados de logon autenticados anteriormente usados por uma [*entidade de segurança*](s-gly.md) para estabelecer sua própria identidade, como uma senha ou um tíquete de protocolo Kerberos.</span><span class="sxs-lookup"><span data-stu-id="5c881-270">Previously authenticated logon data used by a [*security principal*](s-gly.md) to establish its own identity, such as a password, or a Kerberos protocol ticket.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-271"><span id="_security_crl_gly"></span><span id="_SECURITY_CRL_GLY"></span>**REVOGA**</span><span class="sxs-lookup"><span data-stu-id="5c881-271"><span id="_security_crl_gly"></span><span id="_SECURITY_CRL_GLY"></span>**CRL**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-272">Consulte *lista de certificados revogados*.</span><span class="sxs-lookup"><span data-stu-id="5c881-272">See *certificate revocation list*.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-273"><span id="_security_crypt_asn_encoding_gly"></span><span id="_SECURITY_CRYPT_ASN_ENCODING_GLY"></span>**\_codificação ASN \_ cript**</span><span class="sxs-lookup"><span data-stu-id="5c881-273"><span id="_security_crypt_asn_encoding_gly"></span><span id="_SECURITY_CRYPT_ASN_ENCODING_GLY"></span>**CRYPT\_ASN\_ENCODING**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-274">Tipo de codificação que especifica a codificação de certificado.</span><span class="sxs-lookup"><span data-stu-id="5c881-274">Encoding type that specifies certificate encoding.</span></span> <span data-ttu-id="5c881-275">Os tipos de codificação de certificado são armazenados na palavra de ordem inferior de um **DWORD** (o valor é: 0x00000001).</span><span class="sxs-lookup"><span data-stu-id="5c881-275">Certificate encoding types are stored in the low-order word of a **DWORD** (value is: 0x00000001).</span></span> <span data-ttu-id="5c881-276">Esse tipo de codificação é funcionalmente o mesmo que o \_ tipo de codificação de codificação ASN X509 \_ .</span><span class="sxs-lookup"><span data-stu-id="5c881-276">This encoding type is functionally the same as the X509\_ASN\_ENCODING encoding type.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-277"><span id="_security_cryptoanalysis_gly"></span><span id="_SECURITY_CRYPTOANALYSIS_GLY"></span>**cryptanalysis**</span><span class="sxs-lookup"><span data-stu-id="5c881-277"><span id="_security_cryptoanalysis_gly"></span><span id="_SECURITY_CRYPTOANALYSIS_GLY"></span>**cryptanalysis**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-278">Cryptanalysis é a arte e a ciência do texto cifrado de quebra.</span><span class="sxs-lookup"><span data-stu-id="5c881-278">Cryptanalysis is the art and science of breaking ciphertext.</span></span> <span data-ttu-id="5c881-279">Por outro lado, a arte e a ciência de manter as mensagens seguras é a criptografia.</span><span class="sxs-lookup"><span data-stu-id="5c881-279">In contrast, the art and science of keeping messages secure is cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-280"><span id="_security_cryptoapi_gly"></span><span id="_SECURITY_CRYPTOAPI_GLY"></span>**CryptoAPI**</span><span class="sxs-lookup"><span data-stu-id="5c881-280"><span id="_security_cryptoapi_gly"></span><span id="_SECURITY_CRYPTOAPI_GLY"></span>**CryptoAPI**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-281">Interface de programação de aplicativo que permite aos desenvolvedores de aplicativos adicionar autenticação, codificação e criptografia a aplicativos baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="5c881-281">Application programming interface that enables application developers to add authentication, encoding, and encryption to Windows-based applications.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-282"><span id="_security_cryptographic_algorithm_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_ALGORITHM_GLY"></span>**algoritmo criptográfico**</span><span class="sxs-lookup"><span data-stu-id="5c881-282"><span id="_security_cryptographic_algorithm_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_ALGORITHM_GLY"></span>**cryptographic algorithm**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-283">Uma função matemática usada para criptografia e descriptografia.</span><span class="sxs-lookup"><span data-stu-id="5c881-283">A mathematical function used for encryption and decryption.</span></span> <span data-ttu-id="5c881-284">A maioria dos algoritmos criptográficos baseia-se em uma codificação de substituição, em uma codificação transposição ou em uma combinação de ambos.</span><span class="sxs-lookup"><span data-stu-id="5c881-284">Most cryptographic algorithms are based on a substitution cipher, a transposition cipher, or a combination of both.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-285"><span id="_security_cryptographic_digest_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_DIGEST_GLY"></span>**Resumo criptográfico**</span><span class="sxs-lookup"><span data-stu-id="5c881-285"><span id="_security_cryptographic_digest_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_DIGEST_GLY"></span>**Cryptographic Digest**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-286">Uma função de hash unidirecional que usa uma cadeia de caracteres de entrada de comprimento variável e a converte em uma cadeia de caracteres de saída de comprimento fixo (chamada de síntese de criptografia). Essa cadeia de caracteres de saída de comprimento fixo é Probabilistic exclusiva para cada cadeia de caracteres de entrada diferente e, portanto, pode atuar como uma impressão digital de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c881-286">A one-way hash function that takes a variable-length input string and converts it to a fixed-length output string (called a cryptographic digest.) This fixed-length output string is probabilistically unique for every different input string and thus can act as a fingerprint of a file.</span></span> <span data-ttu-id="5c881-287">Quando um arquivo com um resumo criptográfico é baixado, o destinatário Recomputa o resumo.</span><span class="sxs-lookup"><span data-stu-id="5c881-287">When a file with a cryptographic digest is downloaded, the receiver recomputes the digest.</span></span> <span data-ttu-id="5c881-288">Se a cadeia de caracteres de saída corresponder ao resumo contido no arquivo, o receptor terá provado de que o arquivo recebido não foi violado e é idêntico ao arquivo originalmente enviado.</span><span class="sxs-lookup"><span data-stu-id="5c881-288">If the output string matches the digest contained in the file, the receiver has proof that the received file was not tampered with and is identical to the file originally sent.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-289"><span id="_security_cryptographic_key_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_KEY_GLY"></span>**chave de criptografia**</span><span class="sxs-lookup"><span data-stu-id="5c881-289"><span id="_security_cryptographic_key_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_KEY_GLY"></span>**cryptographic key**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-290">Uma chave criptográfica é um dado que é necessário para inicializar um algoritmo criptográfico.</span><span class="sxs-lookup"><span data-stu-id="5c881-290">A cryptographic key is a piece of data that is required to initialize a cryptographic algorithm.</span></span> <span data-ttu-id="5c881-291">Os sistemas criptográficos são geralmente projetados de forma que sua segurança dependa apenas da segurança de suas chaves criptográficas e não, por exemplo, para manter seus algoritmos secretos.</span><span class="sxs-lookup"><span data-stu-id="5c881-291">Cryptographic systems are generally designed so that their security depends only on the security of their cryptographic keys and not, for example, on keeping their algorithms secret.</span></span>

<span data-ttu-id="5c881-292">Há muitos tipos diferentes de chaves de criptografia, correspondentes à ampla variedade de algoritmos criptográficos.</span><span class="sxs-lookup"><span data-stu-id="5c881-292">There are many different types of cryptographic keys, corresponding to the wide variety of cryptographic algorithms.</span></span> <span data-ttu-id="5c881-293">As chaves podem ser classificadas de acordo com o tipo de algoritmo com o qual são usadas (por exemplo, como chaves simétricas ou assimétricas).</span><span class="sxs-lookup"><span data-stu-id="5c881-293">Keys can be classified according to the type of algorithm they are used with (for example, as symmetric or asymmetric keys).</span></span> <span data-ttu-id="5c881-294">Eles também podem ser classificados com base em seu tempo de vida em um sistema (por exemplo, como longa duração ou chaves de sessão).</span><span class="sxs-lookup"><span data-stu-id="5c881-294">They can also be classified based on their lifetime within a system (for example, as long-lived or session keys).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-295"><span id="_security_cryptographic_service_provider_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_SERVICE_PROVIDER_GLY"></span>**provedor de serviços de criptografia**</span><span class="sxs-lookup"><span data-stu-id="5c881-295"><span id="_security_cryptographic_service_provider_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_SERVICE_PROVIDER_GLY"></span>**cryptographic service provider**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-296">CSP Um módulo de software independente que realmente executa algoritmos de criptografia para autenticação, codificação e criptografia.</span><span class="sxs-lookup"><span data-stu-id="5c881-296">(CSP) An independent software module that actually performs cryptography algorithms for authentication, encoding, and encryption.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-297"><span id="_security_cryptography_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_GLY"></span>**criptografia**</span><span class="sxs-lookup"><span data-stu-id="5c881-297"><span id="_security_cryptography_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_GLY"></span>**cryptography**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-298">A arte e a ciência da segurança das informações.</span><span class="sxs-lookup"><span data-stu-id="5c881-298">The art and science of information security.</span></span> <span data-ttu-id="5c881-299">Ele inclui confidencialidade de informações, integridade de dados, autenticação de entidade e autenticação de origem de dados.</span><span class="sxs-lookup"><span data-stu-id="5c881-299">It includes information confidentiality, data integrity, entity authentication, and data origin authentication.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-300"><span id="_security_cryptography_api_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API_GLY"></span>**API de criptografia**</span><span class="sxs-lookup"><span data-stu-id="5c881-300"><span id="_security_cryptography_api_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API_GLY"></span>**Cryptography API**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-301">Consulte *CryptoAPI*.</span><span class="sxs-lookup"><span data-stu-id="5c881-301">See *CryptoAPI*.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-302"><span id="_security_cryptography_api__next_generation_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API__NEXT_GENERATION_GLY"></span>**API de criptografia: próxima geração**</span><span class="sxs-lookup"><span data-stu-id="5c881-302"><span id="_security_cryptography_api__next_generation_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API__NEXT_GENERATION_GLY"></span>**Cryptography API: Next Generation**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-303">CNG A segunda geração do *CryptoAPI*.</span><span class="sxs-lookup"><span data-stu-id="5c881-303">(CNG) The second generation of the *CryptoAPI*.</span></span> <span data-ttu-id="5c881-304">A CNG permite que você substitua provedores de algoritmos existentes por seus próprios provedores e adicione novos algoritmos à medida que eles se tornarem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5c881-304">CNG allows you to replace existing algorithm providers with your own providers and add new algorithms as they become available.</span></span> <span data-ttu-id="5c881-305">A CNG também permite que as mesmas APIs sejam usadas em aplicativos de modo kernel e de usuário.</span><span class="sxs-lookup"><span data-stu-id="5c881-305">CNG also allows the same APIs to be used from user and kernel mode applications.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-306"><span id="_security_cryptology_gly"></span><span id="_SECURITY_CRYPTOLOGY_GLY"></span>**cryptology**</span><span class="sxs-lookup"><span data-stu-id="5c881-306"><span id="_security_cryptology_gly"></span><span id="_SECURITY_CRYPTOLOGY_GLY"></span>**cryptology**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-307">A ramificação da matemática que abrange tanto a criptografia quanto a cryptanalysis.</span><span class="sxs-lookup"><span data-stu-id="5c881-307">The branch of mathematics that encompasses both cryptography and cryptanalysis.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-308"><span id="_security_cryptospi_gly"></span><span id="_SECURITY_CRYPTOSPI_GLY"></span>**CryptoSPI**</span><span class="sxs-lookup"><span data-stu-id="5c881-308"><span id="_security_cryptospi_gly"></span><span id="_SECURITY_CRYPTOSPI_GLY"></span>**CryptoSPI**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-309">A interface de programa do sistema usada com um CSP ( *provedor de serviços de criptografia* ).</span><span class="sxs-lookup"><span data-stu-id="5c881-309">The system program interface used with a *cryptographic service provider* (CSP).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-310"><span id="_security_csp_gly"></span><span id="_SECURITY_CSP_GLY"></span>**CSP**</span><span class="sxs-lookup"><span data-stu-id="5c881-310"><span id="_security_csp_gly"></span><span id="_SECURITY_CSP_GLY"></span>**CSP**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-311">Consulte *provedor de serviços de criptografia*.</span><span class="sxs-lookup"><span data-stu-id="5c881-311">See *cryptographic service provider*.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-312"><span id="_security_csp_family_gly"></span><span id="_SECURITY_CSP_FAMILY_GLY"></span>**Família CSP**</span><span class="sxs-lookup"><span data-stu-id="5c881-312"><span id="_security_csp_family_gly"></span><span id="_SECURITY_CSP_FAMILY_GLY"></span>**CSP family**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-313">Um grupo exclusivo de CSPs que usam o mesmo conjunto de formatos de dados e executam sua função da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="5c881-313">A unique group of CSPs that use the same set of data formats and perform their function in the same way.</span></span> <span data-ttu-id="5c881-314">Mesmo quando duas famílias de CSP usam o mesmo algoritmo (por exemplo, a codificação de bloco RC2), seus esquemas de preenchimento diferentes, comprimentos de chaves ou modos padrão tornam cada grupo distinto.</span><span class="sxs-lookup"><span data-stu-id="5c881-314">Even when two CSP families use the same algorithm (for example, the RC2 block cipher), their different padding schemes, keys lengths, or default modes make each group distinct.</span></span> <span data-ttu-id="5c881-315">O CryptoAPI foi projetado para que cada tipo de CSP represente uma família específica.</span><span class="sxs-lookup"><span data-stu-id="5c881-315">CryptoAPI has been designed so that each CSP type represents a particular family.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-316"><span id="_security_csp_name_gly"></span><span id="_SECURITY_CSP_NAME_GLY"></span>**Nome do CSP**</span><span class="sxs-lookup"><span data-stu-id="5c881-316"><span id="_security_csp_name_gly"></span><span id="_SECURITY_CSP_NAME_GLY"></span>**CSP name**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-317">O nome textual do CSP.</span><span class="sxs-lookup"><span data-stu-id="5c881-317">The textual name of the CSP.</span></span> <span data-ttu-id="5c881-318">Se o CSP tiver sido assinado pela Microsoft, esse nome deverá corresponder exatamente ao nome do CSP que foi especificado no certificado de conformidade de exportação (ECC).</span><span class="sxs-lookup"><span data-stu-id="5c881-318">If the CSP has been signed by Microsoft, this name must exactly match the CSP name that was specified in the Export Compliance Certificate (ECC).</span></span>

</dd> <dt>

<span data-ttu-id="5c881-319"><span id="_security_csp_type_gly"></span><span id="_SECURITY_CSP_TYPE_GLY"></span>**Tipo de CSP**</span><span class="sxs-lookup"><span data-stu-id="5c881-319"><span id="_security_csp_type_gly"></span><span id="_SECURITY_CSP_TYPE_GLY"></span>**CSP type**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-320">Indica a família CSP associada a um provedor.</span><span class="sxs-lookup"><span data-stu-id="5c881-320">Indicates the CSP family associated with a provider.</span></span> <span data-ttu-id="5c881-321">Quando um aplicativo se conecta a um CSP de um tipo específico, cada uma das funções de CryptoAPI, por padrão, funciona de uma maneira prescrita pela família que corresponde a esse tipo de CSP.</span><span class="sxs-lookup"><span data-stu-id="5c881-321">When an application connects to a CSP of a particular type, each of the CryptoAPI functions will, by default, operate in a way prescribed by the family that corresponds to that CSP type.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-322"><span id="_security_ctl_gly"></span><span id="_SECURITY_CTL_GLY"></span>**CERTIFICADOS**</span><span class="sxs-lookup"><span data-stu-id="5c881-322"><span id="_security_ctl_gly"></span><span id="_SECURITY_CTL_GLY"></span>**CTL**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-323">Consulte *lista de certificados confiáveis*.</span><span class="sxs-lookup"><span data-stu-id="5c881-323">See *certificate trust list*.</span></span>

</dd> <dt>

<span data-ttu-id="5c881-324"><span id="_security_cylink_mek_gly"></span><span id="_SECURITY_CYLINK_MEK_GLY"></span>**CYLINK \_ MEK**</span><span class="sxs-lookup"><span data-stu-id="5c881-324"><span id="_security_cylink_mek_gly"></span><span id="_SECURITY_CYLINK_MEK_GLY"></span>**CYLINK\_MEK**</span></span>
</dt> <dd>

<span data-ttu-id="5c881-325">Um algoritmo de criptografia que usa uma variante de 40 bits de uma chave DES em que 16 bits da chave DES de 56 bits são definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="5c881-325">An encryption algorithm that uses a 40-bit variant of a DES key where 16 bits of the 56-bit DES key are set to zero.</span></span> <span data-ttu-id="5c881-326">Esse algoritmo é implementado conforme especificado na especificação de rascunho de IETF para DES de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="5c881-326">This algorithm is implemented as specified in the IETF Draft specification for 40-bit DES.</span></span> <span data-ttu-id="5c881-327">A especificação de rascunho, no momento da redação deste artigo, pode ser encontrada em ftp://ftp.ietf.org/internet-drafts/draft-hoffman-des40-02.txt.</span><span class="sxs-lookup"><span data-stu-id="5c881-327">The draft specification, at the time of this writing can be found at ftp://ftp.ietf.org/internet-drafts/draft-hoffman-des40-02.txt.</span></span> <span data-ttu-id="5c881-328">Esse algoritmo é usado com o valor de **\_ ID alg** CALG \_ CYLINK \_ Mek.</span><span class="sxs-lookup"><span data-stu-id="5c881-328">This algorithm is used with the **ALG\_ID** value CALG\_CYLINK\_MEK.</span></span>

</dd> </dl>

 

 
