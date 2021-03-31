---
description: Contém definições de termos de segurança que começam com a letra P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a
title: P (Glossário de segurança)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd5b580295c35bc021ade53d3cb922ce8fe13d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829145"
---
# <a name="p-security-glossary"></a><span data-ttu-id="05e11-103">P (Glossário de segurança)</span><span class="sxs-lookup"><span data-stu-id="05e11-103">P (Security Glossary)</span></span>

<span data-ttu-id="05e11-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="05e11-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="05e11-105"><span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**margem**</span><span class="sxs-lookup"><span data-stu-id="05e11-105"><span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**padding**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-106">Uma cadeia de caracteres, normalmente adicionada quando o último bloco de texto não criptografado é curto.</span><span class="sxs-lookup"><span data-stu-id="05e11-106">A string, typically added when the last plaintext block is short.</span></span> <span data-ttu-id="05e11-107">Por exemplo, se o tamanho do bloco for 64 bits e o último bloco contiver apenas 40 bits, 24 bits de preenchimento deverão ser adicionados ao último bloco.</span><span class="sxs-lookup"><span data-stu-id="05e11-107">For example, if the block length is 64 bits and the last block contains only 40 bits, then 24 bits of padding must be added to the last block.</span></span> <span data-ttu-id="05e11-108">A cadeia de caracteres de preenchimento pode conter zeros, alternar entre zeros e uns ou algum outro padrão.</span><span class="sxs-lookup"><span data-stu-id="05e11-108">The padding string may contain zeros, alternating zeros and ones, or some other pattern.</span></span> <span data-ttu-id="05e11-109">Os aplicativos que usam o [*CryptoAPI*](c-gly.md) não precisam adicionar preenchimento ao seu texto sem formatação antes de serem criptografados, nem precisam removê-lo após a descriptografia.</span><span class="sxs-lookup"><span data-stu-id="05e11-109">Applications that use [*CryptoAPI*](c-gly.md) need not add padding to their plaintext before it is encrypted, nor do they have to remove it after decrypting.</span></span> <span data-ttu-id="05e11-110">Tudo isso é tratado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="05e11-110">This is all handled automatically.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-111"><span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**filtro de senha**</span><span class="sxs-lookup"><span data-stu-id="05e11-111"><span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**password filter**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-112">Uma DLL que fornece imposição de política de senha e notificação de alteração.</span><span class="sxs-lookup"><span data-stu-id="05e11-112">A DLL that provides password policy enforcement and change notification.</span></span> <span data-ttu-id="05e11-113">As funções implementadas por filtros de senha são chamadas pela [*autoridade de segurança local*](l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="05e11-113">The functions implemented by password filters are called by the [*Local Security Authority*](l-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="05e11-114"><span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**armazenamento persistente**</span><span class="sxs-lookup"><span data-stu-id="05e11-114"><span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**persistent storage**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-115">Qualquer mídia de armazenamento que permaneça intacta quando a energia para ela for desconectada.</span><span class="sxs-lookup"><span data-stu-id="05e11-115">Any storage medium that remains intact when the power to it is disconnected.</span></span> <span data-ttu-id="05e11-116">Muitos bancos de dados de [*repositório de certificados*](c-gly.md) são formas de armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="05e11-116">Many [*certificate store*](c-gly.md) databases are forms of persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-117"><span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS#7**</span><span class="sxs-lookup"><span data-stu-id="05e11-117"><span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-118">Consulte *padrões de criptografia de chave pública*.</span><span class="sxs-lookup"><span data-stu-id="05e11-118">See *Public Key Cryptography Standards*.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-119"><span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \# 1**</span><span class="sxs-lookup"><span data-stu-id="05e11-119"><span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \#1**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-120">Os padrões recomendados para a implementação da criptografia de chave pública com base no algoritmo RSA, conforme definido no [RFC 3447](https://tools.ietf.org/html/rfc3447).</span><span class="sxs-lookup"><span data-stu-id="05e11-120">The recommended standards for the implementation of public-key cryptography based on the RSA algorithm as defined in [RFC 3447](https://tools.ietf.org/html/rfc3447).</span></span>

</dd> <dt>

<span data-ttu-id="05e11-121"><span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \# 12**</span><span class="sxs-lookup"><span data-stu-id="05e11-121"><span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \#12**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-122">O padrão de sintaxe de troca de informações pessoais, desenvolvido e mantido pela RSA Data Security, Inc. Esse padrão de sintaxe especifica um formato portátil para armazenar ou transportar as chaves privadas de um usuário, os certificados e os segredos diversos.</span><span class="sxs-lookup"><span data-stu-id="05e11-122">The Personal Information Exchange Syntax Standard, developed and maintained by RSA Data Security, Inc. This syntax standard specifies a portable format for storing or transporting a user's private keys, certificates, and miscellaneous secrets.</span></span>

<span data-ttu-id="05e11-123">Consulte também padrões de [*certificado*](c-gly.md) e *criptografia de chave pública*.</span><span class="sxs-lookup"><span data-stu-id="05e11-123">See also [*certificate*](c-gly.md) and *Public Key Cryptography Standards*.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-124"><span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**\#Dados assinados PKCS 7**</span><span class="sxs-lookup"><span data-stu-id="05e11-124"><span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**PKCS \#7 Signed Data**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-125">Um objeto de dados que é assinado com o padrão de criptografia de chave pública \# 7 (PKCS \# 7) e que encapsula as informações usadas para assinar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="05e11-125">A data object that is signed with the Public Key Cryptography Standard \#7 (PKCS \#7) and that encapsulates the information used to sign a file.</span></span> <span data-ttu-id="05e11-126">Normalmente, inclui o certificado do assinante e o [*certificado raiz*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="05e11-126">Typically, it includes the signer's certificate and the [*root certificate*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="05e11-127"><span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \# 7**</span><span class="sxs-lookup"><span data-stu-id="05e11-127"><span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \#7**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-128">O padrão de sintaxe de mensagem criptográfica.</span><span class="sxs-lookup"><span data-stu-id="05e11-128">The Cryptographic Message Syntax Standard.</span></span> <span data-ttu-id="05e11-129">Uma sintaxe geral de dados para os quais a criptografia pode ser aplicada, como assinaturas digitais e criptografia.</span><span class="sxs-lookup"><span data-stu-id="05e11-129">A general syntax for data to which cryptography may be applied, such as digital signatures and encryption.</span></span> <span data-ttu-id="05e11-130">Ele também fornece uma sintaxe para disseminar certificados ou listas de certificados revogados e outros atributos de mensagem, como carimbos de data/hora, para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="05e11-130">It also provides a syntax for disseminating certificates or certificate revocation lists and other message attributes, such as time stamps, to the message.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-131"><span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**\_ \_ Codificação ASN do PKCS 7 \_**</span><span class="sxs-lookup"><span data-stu-id="05e11-131"><span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**PKCS\_7\_ASN\_ENCODING**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-132">Um [*tipo de codificação de mensagem*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="05e11-132">A [*message encoding type*](m-gly.md).</span></span> <span data-ttu-id="05e11-133">Os tipos de codificação de mensagens são armazenados na palavra de ordem superior de um **DWORD** (o valor é: 0x00010000).</span><span class="sxs-lookup"><span data-stu-id="05e11-133">Message encoding types are stored in the high-order word of a **DWORD** (value is: 0x00010000).</span></span>

</dd> <dt>

<span data-ttu-id="05e11-134"><span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**comum**</span><span class="sxs-lookup"><span data-stu-id="05e11-134"><span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**plaintext**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-135">Uma mensagem que não está criptografada.</span><span class="sxs-lookup"><span data-stu-id="05e11-135">A message that is not encrypted.</span></span> <span data-ttu-id="05e11-136">As mensagens em texto não criptografado são, às vezes, chamadas de mensagens não criptografadas</span><span class="sxs-lookup"><span data-stu-id="05e11-136">Plaintext messages are sometimes referred to as cleartext messages.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-137"><span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Imagem executável portátil (PE)**</span><span class="sxs-lookup"><span data-stu-id="05e11-137"><span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Portable Executable (PE) Image**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-138">O formato executável padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="05e11-138">The standard Windows executable format.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-139"><span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**</span><span class="sxs-lookup"><span data-stu-id="05e11-139"><span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-140">Consulte *função pseudo-aleatória*.</span><span class="sxs-lookup"><span data-stu-id="05e11-140">See *Pseudo-Random Function*.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-141"><span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**credenciais principais**</span><span class="sxs-lookup"><span data-stu-id="05e11-141"><span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**primary credentials**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-142">O \_ pacote de autenticação MsV1 0 define um valor de cadeia de caracteres de chave de credencial primária: a cadeia de credenciais primária contém as credenciais fornecidas na hora de logon inicial.</span><span class="sxs-lookup"><span data-stu-id="05e11-142">The MsV1\_0 authentication package defines a primary credential key string value: The primary credentials string holds the credentials provided at initial logon time.</span></span> <span data-ttu-id="05e11-143">Ele inclui o nome de usuário e as formas de diferenciação de maiúsculas e minúsculas da senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="05e11-143">It includes the user name and both case-sensitive and case-insensitive forms of the user's password.</span></span>

<span data-ttu-id="05e11-144">Consulte também [*credenciais complementares*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="05e11-144">See also [*supplemental credentials*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="05e11-145"><span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**provedor de serviços primário**</span><span class="sxs-lookup"><span data-stu-id="05e11-145"><span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**primary service provider**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-146">O provedor de serviços que fornece as interfaces de controle para o cartão.</span><span class="sxs-lookup"><span data-stu-id="05e11-146">The service provider that supplies the control interfaces to the card.</span></span> <span data-ttu-id="05e11-147">Cada cartão inteligente pode registrar seu provedor de serviços primário no banco de dados do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="05e11-147">Each smart card can register its primary service provider in the smart card database.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-148"><span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**token primário**</span><span class="sxs-lookup"><span data-stu-id="05e11-148"><span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**primary token**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-149">Um token de acesso que normalmente é criado somente pelo kernel do Windows.</span><span class="sxs-lookup"><span data-stu-id="05e11-149">An access token that is typically created only by the Windows kernel.</span></span> <span data-ttu-id="05e11-150">Ele pode ser atribuído a um processo para representar as informações de segurança padrão para esse processo.</span><span class="sxs-lookup"><span data-stu-id="05e11-150">It may be assigned to a process to represent the default security information for that process.</span></span>

<span data-ttu-id="05e11-151">Consulte também [*token de acesso*](a-gly.md) e [*token de representação*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="05e11-151">See also [*access token*](a-gly.md) and [*impersonation token*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="05e11-152"><span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**beneficiário**</span><span class="sxs-lookup"><span data-stu-id="05e11-152"><span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**principal**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-153">Consulte [*entidade de segurança*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="05e11-153">See [*security principal*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="05e11-154"><span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**privacidade**</span><span class="sxs-lookup"><span data-stu-id="05e11-154"><span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**privacy**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-155">A condição de ser isolada da exibição ou do segredo.</span><span class="sxs-lookup"><span data-stu-id="05e11-155">The condition of being isolated from view or secret.</span></span> <span data-ttu-id="05e11-156">Com relação às mensagens, as mensagens privadas são mensagens criptografadas cujo texto está oculto da exibição.</span><span class="sxs-lookup"><span data-stu-id="05e11-156">With respect to messages, private messages are encrypted messages whose text is hidden from view.</span></span> <span data-ttu-id="05e11-157">Em relação às chaves, uma chave privada é uma chave secreta ocultada de outras.</span><span class="sxs-lookup"><span data-stu-id="05e11-157">With respect to keys, a private key is a secret key concealed from others.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-158"><span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**chave privada**</span><span class="sxs-lookup"><span data-stu-id="05e11-158"><span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**private key**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-159">A metade secreta de um par de chaves usado em um algoritmo de chave pública.</span><span class="sxs-lookup"><span data-stu-id="05e11-159">The secret half of a key pair used in a public key algorithm.</span></span> <span data-ttu-id="05e11-160">As chaves privadas normalmente são usadas para criptografar uma chave de sessão simétrica, assinar digitalmente uma mensagem ou descriptografar uma mensagem que foi criptografada com a chave pública correspondente.</span><span class="sxs-lookup"><span data-stu-id="05e11-160">Private keys are typically used to encrypt a symmetric session key, digitally sign a message, or decrypt a message that has been encrypted with the corresponding public key.</span></span>

<span data-ttu-id="05e11-161">Consulte também *chave pública*.</span><span class="sxs-lookup"><span data-stu-id="05e11-161">See also *public key*.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-162"><span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**BLOB de chave privada**</span><span class="sxs-lookup"><span data-stu-id="05e11-162"><span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**private key BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-163">Um BLOB de chave que contém um par de chaves pública/privada completo.</span><span class="sxs-lookup"><span data-stu-id="05e11-163">A key BLOB that contains a complete public/private key pair.</span></span> <span data-ttu-id="05e11-164">Os BLOBs de chave privada são usados por programas administrativos para transportar pares de chaves.</span><span class="sxs-lookup"><span data-stu-id="05e11-164">Private key BLOBs are used by administrative programs to transport key pairs.</span></span> <span data-ttu-id="05e11-165">Como a parte da chave privada do par de chaves é extremamente confidencial, esses BLOBs normalmente são mantidos criptografados com uma codificação simétrica.</span><span class="sxs-lookup"><span data-stu-id="05e11-165">As the private key portion of the key pair is extremely confidential, these BLOBs are typically kept encrypted with a symmetric cipher.</span></span> <span data-ttu-id="05e11-166">Esses BLOBs de chave também podem ser usados por aplicativos avançados em que os pares de chaves são armazenados no aplicativo, em vez de depender do mecanismo de armazenamento do CSP.</span><span class="sxs-lookup"><span data-stu-id="05e11-166">These key BLOBs can also be used by advanced applications where the key pairs are stored within the application, rather than relying on the CSP's storage mechanism.</span></span> <span data-ttu-id="05e11-167">Um BLOB de chave é criado chamando a função **CryptExportKey** .</span><span class="sxs-lookup"><span data-stu-id="05e11-167">A key BLOB is created by calling the **CryptExportKey** function.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-168"><span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**privilégio**</span><span class="sxs-lookup"><span data-stu-id="05e11-168"><span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**privilege**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-169">O direito de um usuário executar várias operações relacionadas ao sistema, como desligar o sistema, carregar drivers de dispositivo ou alterar a hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="05e11-169">The right of a user to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span> <span data-ttu-id="05e11-170">O token de acesso de um usuário contém uma lista dos privilégios mantidos pelo usuário ou pelos grupos do usuário.</span><span class="sxs-lookup"><span data-stu-id="05e11-170">A user's access token contains a list of the privileges held by either the user or the user's groups.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-171"><span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**Process**</span><span class="sxs-lookup"><span data-stu-id="05e11-171"><span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**process**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-172">O contexto de segurança no qual um aplicativo é executado.</span><span class="sxs-lookup"><span data-stu-id="05e11-172">The security context under which an application runs.</span></span> <span data-ttu-id="05e11-173">Normalmente, o contexto de segurança é associado a um usuário, de modo que todos os aplicativos em execução em um determinado processo assumem as permissões e os privilégios do usuário proprietário.</span><span class="sxs-lookup"><span data-stu-id="05e11-173">Typically, the security context is associated with a user, so all applications running under a given process take on the permissions and privileges of the owning user.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-174"><span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**PROV \_ DSS**</span><span class="sxs-lookup"><span data-stu-id="05e11-174"><span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**PROV\_DSS**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-175">Consulte *\_ tipo de provedor do Prov DSS*.</span><span class="sxs-lookup"><span data-stu-id="05e11-175">See *PROV\_DSS provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-176"><span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**Tipo de provedor do PROV \_ DSS**</span><span class="sxs-lookup"><span data-stu-id="05e11-176"><span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**PROV\_DSS Provider Type**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-177">Tipo de provedor predefinido que dá suporte apenas a assinaturas digitais e hashes.</span><span class="sxs-lookup"><span data-stu-id="05e11-177">Predefined provider type that only supports digital signatures and hashes.</span></span> <span data-ttu-id="05e11-178">Ele especifica o algoritmo de assinatura DSA e os algoritmos de hash MD5 e SHA-1.</span><span class="sxs-lookup"><span data-stu-id="05e11-178">It specifies the DSA signature algorithm, and the MD5 and SHA-1 hashing algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-179"><span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**o PROV \_ DSS \_ DH**</span><span class="sxs-lookup"><span data-stu-id="05e11-179"><span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**PROV\_DSS\_DH**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-180">Consulte *\_ tipo de \_ provedor DH do Prov DSS*.</span><span class="sxs-lookup"><span data-stu-id="05e11-180">See *PROV\_DSS\_DH provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-181"><span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**\_Tipo de \_ provedor DH do Prov DSS**</span><span class="sxs-lookup"><span data-stu-id="05e11-181"><span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**PROV\_DSS\_DH provider type**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-182">Tipo de provedor predefinido que fornece a troca de chaves, assinatura digital e algoritmos de hash.</span><span class="sxs-lookup"><span data-stu-id="05e11-182">Predefined provider type that provides key exchange, digital signature, and hashing algorithms.</span></span> <span data-ttu-id="05e11-183">É semelhante ao tipo de provedor do PROV \_ DSS.</span><span class="sxs-lookup"><span data-stu-id="05e11-183">It is similar to the PROV\_DSS provider type.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-184"><span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**PROV \_ Fortezza**</span><span class="sxs-lookup"><span data-stu-id="05e11-184"><span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**PROV\_FORTEZZA**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-185">Consulte *\_ tipo de provedor do Prov Fortezza*.</span><span class="sxs-lookup"><span data-stu-id="05e11-185">See *PROV\_FORTEZZA provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-186"><span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**Tipo de provedor do PROV \_ Fortezza**</span><span class="sxs-lookup"><span data-stu-id="05e11-186"><span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**PROV\_FORTEZZA provider type**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-187">Tipo de provedor predefinido que fornece troca de chaves, assinatura digital, criptografia e algoritmos de hash.</span><span class="sxs-lookup"><span data-stu-id="05e11-187">Predefined provider type that provides key exchange, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="05e11-188">Os protocolos criptográficos e os algoritmos especificados por esse tipo de provedor pertencem ao National Institute of Standards and Technology (NIST).</span><span class="sxs-lookup"><span data-stu-id="05e11-188">The cryptographic protocols and algorithms specified by this provider type are owned by the National Institute of Standards and Technology (NIST).</span></span>

</dd> <dt>

<span data-ttu-id="05e11-189"><span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROV \_ MS \_ Exchange**</span><span class="sxs-lookup"><span data-stu-id="05e11-189"><span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROV\_MS\_EXCHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-190">Confira o *\_ tipo de provedor Prov MS \_ Exchange*.</span><span class="sxs-lookup"><span data-stu-id="05e11-190">See *PROV\_MS\_EXCHANGE provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-191"><span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**\_Tipo de \_ provedor Prov MS Exchange**</span><span class="sxs-lookup"><span data-stu-id="05e11-191"><span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**PROV\_MS\_EXCHANGE provider type**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-192">Tipo de provedor predefinido projetado para as necessidades do Microsoft Exchange, bem como outros aplicativos que são compatíveis com o Microsoft mail.</span><span class="sxs-lookup"><span data-stu-id="05e11-192">Predefined provider type designed for the needs of Microsoft Exchange, as well as other applications that are compatible with Microsoft Mail.</span></span> <span data-ttu-id="05e11-193">Ele fornece troca de chaves, assinatura digital, criptografia e algoritmos de hash.</span><span class="sxs-lookup"><span data-stu-id="05e11-193">It provides key exchange, digital signature, encryption, and hashing algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-194"><span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROV \_ RSA \_ completo**</span><span class="sxs-lookup"><span data-stu-id="05e11-194"><span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROV\_RSA\_FULL**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-195">Confira o *\_ tipo de \_ provedor completo RSA do Prov*.</span><span class="sxs-lookup"><span data-stu-id="05e11-195">See *PROV\_RSA\_FULL provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-196"><span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**\_Tipo de \_ provedor completo RSA Prov**</span><span class="sxs-lookup"><span data-stu-id="05e11-196"><span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**PROV\_RSA\_FULL provider type**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-197">Tipo de provedor predefinido definido pela Microsoft e RSA Data Security, Inc. Esse tipo de provedor de uso geral fornece troca de chaves, assinatura digital, criptografia e algoritmos de hash.</span><span class="sxs-lookup"><span data-stu-id="05e11-197">Predefined provider type defined by Microsoft and RSA Data Security, Inc. This general purpose provider type provides key exchange, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="05e11-198">A troca de chaves, a assinatura digital e os algoritmos de criptografia são baseados na criptografia de chave pública RSA.</span><span class="sxs-lookup"><span data-stu-id="05e11-198">The key exchange, digital signature, and encryption algorithms are based on RSA public key cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-199"><span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROV \_ RSA \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="05e11-199"><span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROV\_RSA\_SIG**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-200">Confira o *\_ tipo Prov RSA \_ SIG Provider*.</span><span class="sxs-lookup"><span data-stu-id="05e11-200">See *PROV\_RSA\_SIG provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-201"><span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**\_Tipo de provedor de SIG RSA do Prov \_**</span><span class="sxs-lookup"><span data-stu-id="05e11-201"><span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**PROV\_RSA\_SIG provider type**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-202">Tipo de provedor predefinido definido pela Microsoft e pela RSA Data Security.</span><span class="sxs-lookup"><span data-stu-id="05e11-202">Predefined provider type defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="05e11-203">Esse tipo de provedor é um subconjunto do PROV \_ RSA \_ Full que fornece apenas algoritmos de hash e assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="05e11-203">This provider type is a subset of PROV\_RSA\_FULL that provides only digital signature and hashing algorithms.</span></span> <span data-ttu-id="05e11-204">O algoritmo de assinatura digital é um algoritmo de chave pública RSA.</span><span class="sxs-lookup"><span data-stu-id="05e11-204">The digital signature algorithm is an RSA public key algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-205"><span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**PROV \_ SSL**</span><span class="sxs-lookup"><span data-stu-id="05e11-205"><span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**PROV\_SSL**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-206">Consulte *\_ tipo de provedor de SSL Prov*.</span><span class="sxs-lookup"><span data-stu-id="05e11-206">See *PROV\_SSL provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-207"><span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**\_Tipo de provedor de SSL Prov**</span><span class="sxs-lookup"><span data-stu-id="05e11-207"><span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**PROV\_SSL provider type**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-208">Tipo de provedor predefinido que dá suporte ao protocolo protocolo SSL (SSL).</span><span class="sxs-lookup"><span data-stu-id="05e11-208">Predefined provider type that supports the Secure Sockets Layer (SSL) protocol.</span></span> <span data-ttu-id="05e11-209">Esse tipo fornece criptografia de chave, assinatura digital, criptografia e algoritmos de hash.</span><span class="sxs-lookup"><span data-stu-id="05e11-209">This type provides key encryption, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="05e11-210">Uma especificação explicando o SSL está disponível no Netscape Communications Corp.</span><span class="sxs-lookup"><span data-stu-id="05e11-210">A specification explaining SSL is available from Netscape Communications Corp.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-211"><span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**operador**</span><span class="sxs-lookup"><span data-stu-id="05e11-211"><span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-212">Consulte [*provedor de serviços de criptografia*](c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="05e11-212">See [*Cryptographic Service Provider*](c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="05e11-213"><span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**nome do provedor**</span><span class="sxs-lookup"><span data-stu-id="05e11-213"><span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**provider name**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-214">Um nome usado para identificar um CSP.</span><span class="sxs-lookup"><span data-stu-id="05e11-214">A name used to identify a CSP.</span></span> <span data-ttu-id="05e11-215">Por exemplo, o Microsoft Base Cryptographic Provider versão 1,0.</span><span class="sxs-lookup"><span data-stu-id="05e11-215">For example, the Microsoft Base Cryptographic Provider version 1.0.</span></span> <span data-ttu-id="05e11-216">O nome do provedor normalmente é usado ao chamar a função **CryptAcquireContext** para se conectar a um CSP.</span><span class="sxs-lookup"><span data-stu-id="05e11-216">The provider name is typically used when calling the **CryptAcquireContext** function to connect to a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-217"><span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**tipo de provedor**</span><span class="sxs-lookup"><span data-stu-id="05e11-217"><span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**provider type**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-218">Um termo usado para identificar um tipo de CSP (provedor de serviços de criptografia).</span><span class="sxs-lookup"><span data-stu-id="05e11-218">A term used to identify a type of cryptographic service provider (CSP).</span></span> <span data-ttu-id="05e11-219">Os CSPs são agrupados em diferentes tipos de provedor que representam uma família específica de protocolos e formatos de dados padrão.</span><span class="sxs-lookup"><span data-stu-id="05e11-219">CSPs are grouped into different provider types that represent a specific families of standard data formats and protocols.</span></span> <span data-ttu-id="05e11-220">Ao contrário do nome do provedor exclusivo de um CSP, os tipos de provedor não são exclusivos para um determinado CSP.</span><span class="sxs-lookup"><span data-stu-id="05e11-220">In contrast to a CSP's unique provider name, provider types are not unique for a given CSP.</span></span> <span data-ttu-id="05e11-221">O tipo de provedor geralmente é usado ao chamar a função **CryptAcquireContext** para se conectar a um CSP.</span><span class="sxs-lookup"><span data-stu-id="05e11-221">The provider type is typically used when calling the **CryptAcquireContext** function to connect to a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-222"><span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**função pseudo aleatória**</span><span class="sxs-lookup"><span data-stu-id="05e11-222"><span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**pseudo-random function**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-223">PRF Uma função que usa uma chave, rótulo e semente como entrada e produz uma saída de comprimento arbitrário.</span><span class="sxs-lookup"><span data-stu-id="05e11-223">(PRF) A function that takes a key, label, and seed as input, then produces an output of arbitrary length.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-224"><span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**par de chaves pública/privada**</span><span class="sxs-lookup"><span data-stu-id="05e11-224"><span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**public/private key pair**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-225">Um conjunto de chaves de criptografia usadas para criptografia de chave pública.</span><span class="sxs-lookup"><span data-stu-id="05e11-225">A set of cryptographic keys used for public key cryptography.</span></span> <span data-ttu-id="05e11-226">Para cada usuário, um CSP geralmente mantém dois pares de chaves públicas/privadas: um par de chaves do Exchange e um par de chaves de assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="05e11-226">For each user, a CSP usually maintains two public/private key pairs: an exchange key pair and a digital signature key pair.</span></span> <span data-ttu-id="05e11-227">Os dois pares de chaves são mantidos da sessão para a sessão.</span><span class="sxs-lookup"><span data-stu-id="05e11-227">Both key pairs are maintained from session to session.</span></span>

<span data-ttu-id="05e11-228">Consulte par de chaves do [*Exchange*](e-gly.md) e [*pares de chaves de assinatura*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="05e11-228">See [*exchange key pair*](e-gly.md) and [*signature key pair*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="05e11-229"><span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**chave pública**</span><span class="sxs-lookup"><span data-stu-id="05e11-229"><span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**public key**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-230">Uma chave criptográfica normalmente usada ao descriptografar uma chave de sessão ou uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="05e11-230">A cryptographic key typically used when decrypting a session key or a digital signature.</span></span> <span data-ttu-id="05e11-231">A chave pública também pode ser usada para criptografar uma mensagem, garantindo que apenas a pessoa com a chave privada correspondente possa descriptografar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="05e11-231">The public key can also be used to encrypt a message, guaranteeing that only the person with the corresponding private key can decrypt the message.</span></span>

<span data-ttu-id="05e11-232">Consulte também *chave privada*.</span><span class="sxs-lookup"><span data-stu-id="05e11-232">See also *private key*.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-233"><span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**algoritmo de chave pública**</span><span class="sxs-lookup"><span data-stu-id="05e11-233"><span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**public key algorithm**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-234">Uma codificação assimétrica que usa duas chaves, uma para criptografia, a chave pública e a outra para descriptografia, a chave privada.</span><span class="sxs-lookup"><span data-stu-id="05e11-234">An asymmetric cipher that uses two keys, one for encryption, the public key, and the other for decryption, the private key.</span></span> <span data-ttu-id="05e11-235">Conforme implícito pelos nomes de chave, a chave pública usada para codificar texto não criptografado pode ser disponibilizada para qualquer pessoa.</span><span class="sxs-lookup"><span data-stu-id="05e11-235">As implied by the key names, the public key used to encode plaintext can be made available to anyone.</span></span> <span data-ttu-id="05e11-236">No entanto, a chave privada deve permanecer secreta.</span><span class="sxs-lookup"><span data-stu-id="05e11-236">However, the private key must remain secret.</span></span> <span data-ttu-id="05e11-237">Somente a chave privada pode descriptografar o texto cifrado.</span><span class="sxs-lookup"><span data-stu-id="05e11-237">Only the private key can decrypt the ciphertext.</span></span> <span data-ttu-id="05e11-238">O algoritmo de chave pública usado nesse processo é lento (na ordem de 1.000 vezes mais lenta que os algoritmos simétricos) e normalmente é usado para criptografar chaves de sessão ou assinar digitalmente uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="05e11-238">The public key algorithm used in this process is slow (on the order of 1,000 times slower than symmetric algorithms), and is typically used to encrypt session keys or digitally sign a message.</span></span>

<span data-ttu-id="05e11-239">Consulte também *chave pública* e *chave privada*.</span><span class="sxs-lookup"><span data-stu-id="05e11-239">See also *public key* and *private key*.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-240"><span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**BLOB de chave pública**</span><span class="sxs-lookup"><span data-stu-id="05e11-240"><span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**public key BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-241">Um BLOB usado para armazenar a parte da chave pública de um par de chaves pública/privada.</span><span class="sxs-lookup"><span data-stu-id="05e11-241">A BLOB used to store the public key portion of a public/private key pair.</span></span> <span data-ttu-id="05e11-242">Os BLOBs de chave pública não são criptografados, pois a chave pública contida em não é secreta.</span><span class="sxs-lookup"><span data-stu-id="05e11-242">Public key BLOBs are not encrypted as the public key contained within is not secret.</span></span> <span data-ttu-id="05e11-243">Um BLOB de chave pública é criado chamando a função **CryptExportKey** .</span><span class="sxs-lookup"><span data-stu-id="05e11-243">A public key BLOB is created by calling the **CryptExportKey** function.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-244"><span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Padrões de criptografia de chave pública**</span><span class="sxs-lookup"><span data-stu-id="05e11-244"><span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Public Key Cryptography Standards**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-245">PKCS#7 Um conjunto de padrões de sintaxe para criptografia de chave pública que abrange funções de segurança, incluindo métodos de assinatura de dados, troca de chaves, solicitação de certificados, criptografia de chave pública e descriptografia e outras funções de segurança.</span><span class="sxs-lookup"><span data-stu-id="05e11-245">(PKCS) A set of syntax standards for public key cryptography covering security functions, including methods for signing data, exchanging keys, requesting certificates, public key encryption and decryption, and other security functions.</span></span>

</dd> <dt>

<span data-ttu-id="05e11-246"><span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**criptografia de chave pública**</span><span class="sxs-lookup"><span data-stu-id="05e11-246"><span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**public key encryption**</span></span>
</dt> <dd>

<span data-ttu-id="05e11-247">Criptografia que usa um par de chaves, uma chave para criptografar dados e a outra chave para descriptografar dados.</span><span class="sxs-lookup"><span data-stu-id="05e11-247">Encryption that uses a pair of keys, one key to encrypt data and the other key to decrypt data.</span></span> <span data-ttu-id="05e11-248">Em contraste, os algoritmos de criptografia simétrica que usam a mesma chave para criptografia e descriptografia.</span><span class="sxs-lookup"><span data-stu-id="05e11-248">In contrast, symmetric encryption algorithms that use the same key for both encryption and decryption.</span></span> <span data-ttu-id="05e11-249">Na prática, a criptografia de chave pública normalmente é usada para proteger a chave de sessão usada por um algoritmo de criptografia simétrica.</span><span class="sxs-lookup"><span data-stu-id="05e11-249">In practice, public key cryptography is typically used to protect the session key used by a symmetric encryption algorithm.</span></span> <span data-ttu-id="05e11-250">Nesse caso, a chave pública é usada para criptografar a chave de sessão, que, por sua vez, foi usada para criptografar alguns dados, e a chave privada é usada para descriptografia.</span><span class="sxs-lookup"><span data-stu-id="05e11-250">In this case, the public key is used to encrypt the session key, which in turn was used to encrypt some data, and the private key is used for decryption.</span></span> <span data-ttu-id="05e11-251">Além de proteger as chaves de sessão, a criptografia de chave pública também pode ser usada para assinar digitalmente uma mensagem (usando a chave privada) e validar a assinatura (usando a chave pública).</span><span class="sxs-lookup"><span data-stu-id="05e11-251">In addition to protecting session keys, public key cryptography may also be used to digitally sign a message (using the private key) and validate the signature (using the public key).</span></span>

<span data-ttu-id="05e11-252">Consulte também *algoritmo de chave pública*.</span><span class="sxs-lookup"><span data-stu-id="05e11-252">See also *public key algorithm*.</span></span>

</dd> </dl>

 

 



