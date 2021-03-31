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
# <a name="p-security-glossary"></a>P (Glossário de segurança)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**margem**
</dt> <dd>

Uma cadeia de caracteres, normalmente adicionada quando o último bloco de texto não criptografado é curto. Por exemplo, se o tamanho do bloco for 64 bits e o último bloco contiver apenas 40 bits, 24 bits de preenchimento deverão ser adicionados ao último bloco. A cadeia de caracteres de preenchimento pode conter zeros, alternar entre zeros e uns ou algum outro padrão. Os aplicativos que usam o [*CryptoAPI*](c-gly.md) não precisam adicionar preenchimento ao seu texto sem formatação antes de serem criptografados, nem precisam removê-lo após a descriptografia. Tudo isso é tratado automaticamente.

</dd> <dt>

<span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**filtro de senha**
</dt> <dd>

Uma DLL que fornece imposição de política de senha e notificação de alteração. As funções implementadas por filtros de senha são chamadas pela [*autoridade de segurança local*](l-gly.md).

</dd> <dt>

<span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**armazenamento persistente**
</dt> <dd>

Qualquer mídia de armazenamento que permaneça intacta quando a energia para ela for desconectada. Muitos bancos de dados de [*repositório de certificados*](c-gly.md) são formas de armazenamento persistente.

</dd> <dt>

<span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS#7**
</dt> <dd>

Consulte *padrões de criptografia de chave pública*.

</dd> <dt>

<span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \# 1**
</dt> <dd>

Os padrões recomendados para a implementação da criptografia de chave pública com base no algoritmo RSA, conforme definido no [RFC 3447](https://tools.ietf.org/html/rfc3447).

</dd> <dt>

<span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \# 12**
</dt> <dd>

O padrão de sintaxe de troca de informações pessoais, desenvolvido e mantido pela RSA Data Security, Inc. Esse padrão de sintaxe especifica um formato portátil para armazenar ou transportar as chaves privadas de um usuário, os certificados e os segredos diversos.

Consulte também padrões de [*certificado*](c-gly.md) e *criptografia de chave pública*.

</dd> <dt>

<span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**\#Dados assinados PKCS 7**
</dt> <dd>

Um objeto de dados que é assinado com o padrão de criptografia de chave pública \# 7 (PKCS \# 7) e que encapsula as informações usadas para assinar um arquivo. Normalmente, inclui o certificado do assinante e o [*certificado raiz*](r-gly.md).

</dd> <dt>

<span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \# 7**
</dt> <dd>

O padrão de sintaxe de mensagem criptográfica. Uma sintaxe geral de dados para os quais a criptografia pode ser aplicada, como assinaturas digitais e criptografia. Ele também fornece uma sintaxe para disseminar certificados ou listas de certificados revogados e outros atributos de mensagem, como carimbos de data/hora, para a mensagem.

</dd> <dt>

<span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**\_ \_ Codificação ASN do PKCS 7 \_**
</dt> <dd>

Um [*tipo de codificação de mensagem*](m-gly.md). Os tipos de codificação de mensagens são armazenados na palavra de ordem superior de um **DWORD** (o valor é: 0x00010000).

</dd> <dt>

<span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**comum**
</dt> <dd>

Uma mensagem que não está criptografada. As mensagens em texto não criptografado são, às vezes, chamadas de mensagens não criptografadas

</dd> <dt>

<span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Imagem executável portátil (PE)**
</dt> <dd>

O formato executável padrão do Windows.

</dd> <dt>

<span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**
</dt> <dd>

Consulte *função pseudo-aleatória*.

</dd> <dt>

<span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**credenciais principais**
</dt> <dd>

O \_ pacote de autenticação MsV1 0 define um valor de cadeia de caracteres de chave de credencial primária: a cadeia de credenciais primária contém as credenciais fornecidas na hora de logon inicial. Ele inclui o nome de usuário e as formas de diferenciação de maiúsculas e minúsculas da senha do usuário.

Consulte também [*credenciais complementares*](s-gly.md).

</dd> <dt>

<span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**provedor de serviços primário**
</dt> <dd>

O provedor de serviços que fornece as interfaces de controle para o cartão. Cada cartão inteligente pode registrar seu provedor de serviços primário no banco de dados do cartão inteligente.

</dd> <dt>

<span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**token primário**
</dt> <dd>

Um token de acesso que normalmente é criado somente pelo kernel do Windows. Ele pode ser atribuído a um processo para representar as informações de segurança padrão para esse processo.

Consulte também [*token de acesso*](a-gly.md) e [*token de representação*](i-gly.md).

</dd> <dt>

<span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**beneficiário**
</dt> <dd>

Consulte [*entidade de segurança*](s-gly.md).

</dd> <dt>

<span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**privacidade**
</dt> <dd>

A condição de ser isolada da exibição ou do segredo. Com relação às mensagens, as mensagens privadas são mensagens criptografadas cujo texto está oculto da exibição. Em relação às chaves, uma chave privada é uma chave secreta ocultada de outras.

</dd> <dt>

<span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**chave privada**
</dt> <dd>

A metade secreta de um par de chaves usado em um algoritmo de chave pública. As chaves privadas normalmente são usadas para criptografar uma chave de sessão simétrica, assinar digitalmente uma mensagem ou descriptografar uma mensagem que foi criptografada com a chave pública correspondente.

Consulte também *chave pública*.

</dd> <dt>

<span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**BLOB de chave privada**
</dt> <dd>

Um BLOB de chave que contém um par de chaves pública/privada completo. Os BLOBs de chave privada são usados por programas administrativos para transportar pares de chaves. Como a parte da chave privada do par de chaves é extremamente confidencial, esses BLOBs normalmente são mantidos criptografados com uma codificação simétrica. Esses BLOBs de chave também podem ser usados por aplicativos avançados em que os pares de chaves são armazenados no aplicativo, em vez de depender do mecanismo de armazenamento do CSP. Um BLOB de chave é criado chamando a função **CryptExportKey** .

</dd> <dt>

<span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**privilégio**
</dt> <dd>

O direito de um usuário executar várias operações relacionadas ao sistema, como desligar o sistema, carregar drivers de dispositivo ou alterar a hora do sistema. O token de acesso de um usuário contém uma lista dos privilégios mantidos pelo usuário ou pelos grupos do usuário.

</dd> <dt>

<span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**Process**
</dt> <dd>

O contexto de segurança no qual um aplicativo é executado. Normalmente, o contexto de segurança é associado a um usuário, de modo que todos os aplicativos em execução em um determinado processo assumem as permissões e os privilégios do usuário proprietário.

</dd> <dt>

<span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**PROV \_ DSS**
</dt> <dd>

Consulte *\_ tipo de provedor do Prov DSS*.

</dd> <dt>

<span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**Tipo de provedor do PROV \_ DSS**
</dt> <dd>

Tipo de provedor predefinido que dá suporte apenas a assinaturas digitais e hashes. Ele especifica o algoritmo de assinatura DSA e os algoritmos de hash MD5 e SHA-1.

</dd> <dt>

<span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**o PROV \_ DSS \_ DH**
</dt> <dd>

Consulte *\_ tipo de \_ provedor DH do Prov DSS*.

</dd> <dt>

<span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**\_Tipo de \_ provedor DH do Prov DSS**
</dt> <dd>

Tipo de provedor predefinido que fornece a troca de chaves, assinatura digital e algoritmos de hash. É semelhante ao tipo de provedor do PROV \_ DSS.

</dd> <dt>

<span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**PROV \_ Fortezza**
</dt> <dd>

Consulte *\_ tipo de provedor do Prov Fortezza*.

</dd> <dt>

<span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**Tipo de provedor do PROV \_ Fortezza**
</dt> <dd>

Tipo de provedor predefinido que fornece troca de chaves, assinatura digital, criptografia e algoritmos de hash. Os protocolos criptográficos e os algoritmos especificados por esse tipo de provedor pertencem ao National Institute of Standards and Technology (NIST).

</dd> <dt>

<span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROV \_ MS \_ Exchange**
</dt> <dd>

Confira o *\_ tipo de provedor Prov MS \_ Exchange*.

</dd> <dt>

<span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**\_Tipo de \_ provedor Prov MS Exchange**
</dt> <dd>

Tipo de provedor predefinido projetado para as necessidades do Microsoft Exchange, bem como outros aplicativos que são compatíveis com o Microsoft mail. Ele fornece troca de chaves, assinatura digital, criptografia e algoritmos de hash.

</dd> <dt>

<span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROV \_ RSA \_ completo**
</dt> <dd>

Confira o *\_ tipo de \_ provedor completo RSA do Prov*.

</dd> <dt>

<span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**\_Tipo de \_ provedor completo RSA Prov**
</dt> <dd>

Tipo de provedor predefinido definido pela Microsoft e RSA Data Security, Inc. Esse tipo de provedor de uso geral fornece troca de chaves, assinatura digital, criptografia e algoritmos de hash. A troca de chaves, a assinatura digital e os algoritmos de criptografia são baseados na criptografia de chave pública RSA.

</dd> <dt>

<span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROV \_ RSA \_ SIG**
</dt> <dd>

Confira o *\_ tipo Prov RSA \_ SIG Provider*.

</dd> <dt>

<span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**\_Tipo de provedor de SIG RSA do Prov \_**
</dt> <dd>

Tipo de provedor predefinido definido pela Microsoft e pela RSA Data Security. Esse tipo de provedor é um subconjunto do PROV \_ RSA \_ Full que fornece apenas algoritmos de hash e assinatura digital. O algoritmo de assinatura digital é um algoritmo de chave pública RSA.

</dd> <dt>

<span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**PROV \_ SSL**
</dt> <dd>

Consulte *\_ tipo de provedor de SSL Prov*.

</dd> <dt>

<span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**\_Tipo de provedor de SSL Prov**
</dt> <dd>

Tipo de provedor predefinido que dá suporte ao protocolo protocolo SSL (SSL). Esse tipo fornece criptografia de chave, assinatura digital, criptografia e algoritmos de hash. Uma especificação explicando o SSL está disponível no Netscape Communications Corp.

</dd> <dt>

<span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**operador**
</dt> <dd>

Consulte [*provedor de serviços de criptografia*](c-gly.md).

</dd> <dt>

<span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**nome do provedor**
</dt> <dd>

Um nome usado para identificar um CSP. Por exemplo, o Microsoft Base Cryptographic Provider versão 1,0. O nome do provedor normalmente é usado ao chamar a função **CryptAcquireContext** para se conectar a um CSP.

</dd> <dt>

<span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**tipo de provedor**
</dt> <dd>

Um termo usado para identificar um tipo de CSP (provedor de serviços de criptografia). Os CSPs são agrupados em diferentes tipos de provedor que representam uma família específica de protocolos e formatos de dados padrão. Ao contrário do nome do provedor exclusivo de um CSP, os tipos de provedor não são exclusivos para um determinado CSP. O tipo de provedor geralmente é usado ao chamar a função **CryptAcquireContext** para se conectar a um CSP.

</dd> <dt>

<span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**função pseudo aleatória**
</dt> <dd>

PRF Uma função que usa uma chave, rótulo e semente como entrada e produz uma saída de comprimento arbitrário.

</dd> <dt>

<span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**par de chaves pública/privada**
</dt> <dd>

Um conjunto de chaves de criptografia usadas para criptografia de chave pública. Para cada usuário, um CSP geralmente mantém dois pares de chaves públicas/privadas: um par de chaves do Exchange e um par de chaves de assinatura digital. Os dois pares de chaves são mantidos da sessão para a sessão.

Consulte par de chaves do [*Exchange*](e-gly.md) e [*pares de chaves de assinatura*](s-gly.md).

</dd> <dt>

<span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**chave pública**
</dt> <dd>

Uma chave criptográfica normalmente usada ao descriptografar uma chave de sessão ou uma assinatura digital. A chave pública também pode ser usada para criptografar uma mensagem, garantindo que apenas a pessoa com a chave privada correspondente possa descriptografar a mensagem.

Consulte também *chave privada*.

</dd> <dt>

<span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**algoritmo de chave pública**
</dt> <dd>

Uma codificação assimétrica que usa duas chaves, uma para criptografia, a chave pública e a outra para descriptografia, a chave privada. Conforme implícito pelos nomes de chave, a chave pública usada para codificar texto não criptografado pode ser disponibilizada para qualquer pessoa. No entanto, a chave privada deve permanecer secreta. Somente a chave privada pode descriptografar o texto cifrado. O algoritmo de chave pública usado nesse processo é lento (na ordem de 1.000 vezes mais lenta que os algoritmos simétricos) e normalmente é usado para criptografar chaves de sessão ou assinar digitalmente uma mensagem.

Consulte também *chave pública* e *chave privada*.

</dd> <dt>

<span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**BLOB de chave pública**
</dt> <dd>

Um BLOB usado para armazenar a parte da chave pública de um par de chaves pública/privada. Os BLOBs de chave pública não são criptografados, pois a chave pública contida em não é secreta. Um BLOB de chave pública é criado chamando a função **CryptExportKey** .

</dd> <dt>

<span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Padrões de criptografia de chave pública**
</dt> <dd>

PKCS#7 Um conjunto de padrões de sintaxe para criptografia de chave pública que abrange funções de segurança, incluindo métodos de assinatura de dados, troca de chaves, solicitação de certificados, criptografia de chave pública e descriptografia e outras funções de segurança.

</dd> <dt>

<span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**criptografia de chave pública**
</dt> <dd>

Criptografia que usa um par de chaves, uma chave para criptografar dados e a outra chave para descriptografar dados. Em contraste, os algoritmos de criptografia simétrica que usam a mesma chave para criptografia e descriptografia. Na prática, a criptografia de chave pública normalmente é usada para proteger a chave de sessão usada por um algoritmo de criptografia simétrica. Nesse caso, a chave pública é usada para criptografar a chave de sessão, que, por sua vez, foi usada para criptografar alguns dados, e a chave privada é usada para descriptografia. Além de proteger as chaves de sessão, a criptografia de chave pública também pode ser usada para assinar digitalmente uma mensagem (usando a chave privada) e validar a assinatura (usando a chave pública).

Consulte também *algoritmo de chave pública*.

</dd> </dl>

 

 



