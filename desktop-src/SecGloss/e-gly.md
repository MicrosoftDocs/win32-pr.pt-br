---
description: Contém definições de termos de segurança que começam com a letra E.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f1caccd2-3453-448e-b194-bf899eff8091
title: E (Glossário de segurança)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed30465ef5764d4553ceb03e1094b73d940f85f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506032"
---
# <a name="e-security-glossary"></a>E (Glossário de segurança)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_ecb_gly"></span><span id="_SECURITY_ECB_GLY"></span>**ECB**
</dt> <dd>

Consulte *Codebook eletrônico*.

</dd> <dt>

<span id="_security_ecc_gly"></span><span id="_SECURITY_ECC_GLY"></span>**ControlCenter**
</dt> <dd>

Consulte *criptografia de curva elíptica*.

</dd> <dt>

<span id="_security_efs_gly"></span><span id="_SECURITY_EFS_GLY"></span>**EFS**
</dt> <dd>

Consulte *sistema de arquivos com criptografia*.

</dd> <dt>

<span id="_security_eku_gly"></span><span id="_SECURITY_EKU_GLY"></span>**EKU**
</dt> <dd>

Consulte *uso avançado de chave*.

</dd> <dt>

<span id="_security_electronic_codebook_gly"></span><span id="_SECURITY_ELECTRONIC_CODEBOOK_GLY"></span>**Codebook eletrônico**
</dt> <dd>

ECB Um modo de codificação de bloco (cada bloco é criptografado individualmente) que não usa nenhum comentário. Isso significa que todos os blocos de texto sem formatação que são idênticos (na mesma mensagem ou em uma mensagem diferente criptografada com a mesma chave) são transformados em blocos cifrados idênticos. Os vetores de inicialização não podem ser usados com este modo de codificação. Se um único bit do bloco de texto cifrado for distorcido, todo o bloco de texto não criptografado correspondente também será distorcido.

</dd> <dt>

<span id="_security_elliptic_curve_cryptography_gly"></span><span id="_SECURITY_ELLIPTIC_CURVE_CRYPTOGRAPHY_GLY"></span>**criptografia de curva elíptica**
</dt> <dd>

ControlCenter Uma abordagem à criptografia de chave pública com base nas propriedades de curvas elípticas. A principal vantagem do ECC é a eficiência, que se torna importante, pois os dispositivos têm requisitos menores e de segurança mais exigentes. Por exemplo, chaves ECC entre 163 bits e 512 bits são um-sexto para um-thirtieth o tamanho de chaves RSA de nível de segurança equivalentes. À medida que o tamanho da chave aumenta a eficiência relativa dos aumentos de ECC.

</dd> <dt>

<span id="_security_encoding_gly"></span><span id="_SECURITY_ENCODING_GLY"></span>**mecanismo**
</dt> <dd>

O processo de transformar dados em um fluxo de bits. A codificação faz parte do processo de serialização que converte dados em um fluxo de uns e zeros.

</dd> <dt>

<span id="_security_encoding_type_gly"></span><span id="_SECURITY_ENCODING_TYPE_GLY"></span>**tipo de codificação**
</dt> <dd>

Refere-se a qual tipo de codificação é usado para codificação de certificado e mensagem. Os tipos de codificação são especificados como um **DWORD**, com o tipo de codificação de certificado armazenado na palavra de ordem inferior e o tipo de codificação de mensagem armazenado na palavra de ordem superior. Embora alguns campos de funções ou de estrutura exijam apenas um dos tipos de codificação, é sempre aceitável especificar ambos.

</dd> <dt>

<span id="_security_encryption_gly"></span><span id="_SECURITY_ENCRYPTION_GLY"></span>**encripta**
</dt> <dd>

O processo de converter o texto não criptografado em texto cifrado para ajudar a impedir que ele seja lido e compreendido por uma parte não autorizada. A criptografia é o oposto da descriptografia.

</dd> <dt>

<span id="_security_encrypted_data_gly"></span><span id="_SECURITY_ENCRYPTED_DATA_GLY"></span>**dados criptografados**
</dt> <dd>

Dados que foram convertidos de texto não criptografado em texto cifrado. Mensagens criptografadas são usadas para disfarçar o conteúdo de uma mensagem quando ela é enviada ou armazenada.

</dd> <dt>

<span id="_security_encrypting_file_system_gly"></span><span id="_SECURITY_ENCRYPTING_FILE_SYSTEM_GLY"></span>**sistema de arquivos com criptografia**
</dt> <dd>

EFS Um recurso no sistema operacional Windows que permite aos usuários criptografar arquivos e pastas em um disco de volume NTFS para mantê-los protegidos contra o acesso de intrusos.

</dd> <dt>

<span id="_security_encryption_and_decryption_functions_gly"></span><span id="_SECURITY_ENCRYPTION_AND_DECRYPTION_FUNCTIONS_GLY"></span>**funções de criptografia e descriptografia**
</dt> <dd>

Funções de mensagens simplificadas usadas para codificar e criptografar (ou decodificar e descriptografar) dados. Como um conjunto, essas funções incluem suporte para criptografar e descriptografar dados simultaneamente.

Consulte também [*funções de mensagens simplificadas*](s-gly.md).

</dd> <dt>

<span id="_security_enhanced_content_type_gly"></span><span id="_SECURITY_ENHANCED_CONTENT_TYPE_GLY"></span>**tipo de conteúdo avançado**
</dt> <dd>

Uma classe de dados contida em uma \# mensagem PKCS 7 que contém dados (possivelmente criptografados), além de aprimoramentos de criptografia, como hashes ou assinaturas. Os tipos de dados aprimorados definidos pelo PKCS \# 7 incluem dados assinados, dados de envelopes, dados assinados e envelopos e dados resumidos (com hash).

</dd> <dt>

<span id="_security_enhanced_key_usage_gly"></span><span id="_SECURITY_ENHANCED_KEY_USAGE_GLY"></span>**uso avançado de chave**
</dt> <dd>

EKU Uma extensão de certificado e um valor de propriedade estendida de certificado. Um EKU especifica os usos para os quais um certificado é válido.

</dd> <dt>

<span id="_security_enveloped_data_content_type_gly"></span><span id="_SECURITY_ENVELOPED_DATA_CONTENT_TYPE_GLY"></span>**tipo de conteúdo de dados envelopado**
</dt> <dd>

Um \# conteúdo avançado do PKCS 7 que consiste em conteúdo criptografado (de qualquer tipo) e chaves de criptografia de conteúdo (para um ou mais destinatários). A combinação de conteúdo criptografado e chave de criptografia para um destinatário é chamada de *envelope digital* para esse destinatário. Esse tipo de mensagem deve ser usado quando você deseja manter o conteúdo do segredo da mensagem e permitir que apenas pessoas ou entidades especificadas recuperem o conteúdo.

</dd> <dt>

<span id="_security_exchange_key_gly"></span><span id="_SECURITY_EXCHANGE_KEY_GLY"></span>**chave do Exchange**
</dt> <dd>

Consulte *par de chaves do Exchange*.

</dd> <dt>

<span id="_security_exchange_key_pair_gly"></span><span id="_SECURITY_EXCHANGE_KEY_PAIR_GLY"></span>**par de chaves do Exchange**
</dt> <dd>

Um par de chaves pública/privada usado para criptografar chaves de sessão para que elas possam ser armazenadas e trocadas com segurança com outros usuários. Os pares de chaves do Exchange são criados chamando a função **CryptGenKey** .

Compare o [*par de chaves de assinatura*](s-gly.md).

</dd> <dt>

<span id="_security_external_store_gly"></span><span id="_SECURITY_EXTERNAL_STORE_GLY"></span>**repositório externo**
</dt> <dd>

Um repositório de certificados que mantém seus certificados, CRLs e CTLs em um local externo à memória armazenada em cache, como em um banco de dados em um servidor de rede. Um repositório externo não lê e decodifica seus certificados, CRLs e CTL quando a função **CertOpenStore** é chamada. A leitura e a decodificação são adiadas até que um método de enumeração ou de localização seja chamado.

</dd> </dl>

 

 



