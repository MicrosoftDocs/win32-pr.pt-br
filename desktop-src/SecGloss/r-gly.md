---
description: Contém definições de termos de segurança que começam com a letra R.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ce589e18-02ac-42c2-b76b-776deb686bbd
title: R (Glossário de segurança)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc85a0da8aa4a0b985b8be040ef95e37068e8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761856"
---
# <a name="r-security-glossary"></a>R (Glossário de segurança)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q R [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_rc2_gly"></span><span id="_SECURITY_RC2_GLY"></span>**RC2**
</dt> <dd>

O nome do algoritmo do [*CryptoAPI*](c-gly.md) para o algoritmo RC2.

Consulte também *algoritmo de bloqueio RC2*.

</dd> <dt>

<span id="_security_rc2_block_algorithm_gly"></span><span id="_SECURITY_RC2_BLOCK_ALGORITHM_GLY"></span>**Algoritmo de bloco RC2**
</dt> <dd>

Um algoritmo de [*criptografia*](e-gly.md) de dados baseado na codificação de bloco simétrico de RC2 64 bits. O RC2 é especificado pelos \_ tipos de provedor completo RSA de Prov \_ . O [*CryptoAPI*](c-gly.md) faz referência a esse algoritmo por seu identificador (CALG \_ RC2), nome (RC2) e classe (alg \_ classe de criptografia de \_ dados \_ ).

</dd> <dt>

<span id="_security_rc4_gly"></span><span id="_SECURITY_RC4_GLY"></span>**RC4**
</dt> <dd>

O nome do algoritmo do [*CryptoAPI*](c-gly.md) para o algoritmo RC4.

Consulte também *algoritmo de fluxo RC4*.

</dd> <dt>

<span id="_security_rc4_stream_algorithm_gly"></span><span id="_SECURITY_RC4_STREAM_ALGORITHM_GLY"></span>**Algoritmo de fluxo RC4**
</dt> <dd>

Um algoritmo de [*criptografia*](e-gly.md) de dados baseado na codificação de fluxo simétrico RC4. O RC4 é especificado pelos \_ tipos de provedor completo RSA de Prov \_ . O [*CryptoAPI*](c-gly.md) faz referência a esse algoritmo por seu identificador (CALG \_ RC4), nome (RC4) e classe (alg \_ classe de criptografia de \_ dados \_ ).

</dd> <dt>

<span id="_security_rdn_gly"></span><span id="_SECURITY_RDN_GLY"></span>**RDN**
</dt> <dd>

Consulte *nome distinto relativo*.

</dd> <dt>

<span id="_security_reader_gly"></span><span id="_SECURITY_READER_GLY"></span>**leitora**
</dt> <dd>

Um dispositivo padrão no subsistema de [*cartão inteligente*](s-gly.md) . Um dispositivo de interface (IFD) que dá suporte à entrada/saída bidirecional para um cartão inteligente. Ele pode estar associado a um sistema inteiro, a um ou mais grupos de leitores ou a um terminal específico. O subsistema de cartão inteligente permite que um leitor seja dedicado ao terminal ao qual ele é atribuído. No entanto, no momento apenas um terminal existe em um computador.

</dd> <dt>

<span id="_security_reader_driver_gly"></span><span id="_SECURITY_READER_DRIVER_GLY"></span>**Driver de leitor**
</dt> <dd>

Um driver específico que mapeia os serviços de driver para um dispositivo de leitor de hardware específico. Ele deve comunicar eventos de inserção e remoção de cartão para o driver de classe de [*cartão inteligente*](s-gly.md) para encaminhamento ao Gerenciador de recursos de cartão inteligente e deve fornecer recursos de troca de dados para o cartão por qualquer protocolo bruto, t = 0, t = 1 ou pts.

</dd> <dt>

<span id="_security_reader_group_gly"></span><span id="_SECURITY_READER_GROUP_GLY"></span>**grupo de leitores**
</dt> <dd>

Um grupo lógico de leitores. Os grupos de leitores podem ser definidos pelo sistema ou criados por usuários ou administradores. Os grupos de leitores são usados por funções de cartão inteligente que podem agir sobre grupos de leitores. Para evitar conflitos de nomenclatura com grupos definidos pelo usuário, a Microsoft reserva o uso de qualquer nome que contenha o cifrão ($).

</dd> <dt>

<span id="_security_reader_helper_driver_gly"></span><span id="_SECURITY_READER_HELPER_DRIVER_GLY"></span>**Driver auxiliar de leitor**
</dt> <dd>

Fornece rotinas comuns de suporte a driver de cartão inteligente e T = 0 e T = 1 suporte de protocolo a drivers específicos, conforme necessário.

</dd> <dt>

<span id="_security_reference_count_gly"></span><span id="_SECURITY_REFERENCE_COUNT_GLY"></span>**contagem de referência**
</dt> <dd>

Um valor inteiro usado para controlar um objeto COM. Quando um objeto é criado, sua contagem de referência é definida como um. Toda vez que uma interface é associada ao objeto, sua contagem de referência é incrementada; Quando a conexão de interface é destruída, a contagem de referência é decrementada. O objeto é destruído quando a contagem de referência chega a zero. Em seguida, todas as interfaces para esse objeto não são válidas.

</dd> <dt>

<span id="_security_relative_distinguished_name_gly"></span><span id="_SECURITY_RELATIVE_DISTINGUISHED_NAME_GLY"></span>**nome distinto relativo**
</dt> <dd>

RDN Uma entidade incluída como o assunto em uma solicitação de um certificado. Os elementos em um RDN são definidos por seus atributos e não precisam incluir um nome. Em relação ao [*CryptoAPI*](c-gly.md), um RDN é definido por uma \_ estrutura RDN de certificado que, por sua vez, aponta para uma matriz de \_ estruturas de \_ atributo attr de certificado. Cada estrutura de atributo especifica um único atributo.

</dd> <dt>

<span id="_security_relative_identifier_gly"></span><span id="_SECURITY_RELATIVE_IDENTIFIER_GLY"></span>**identificador relativo**
</dt> <dd>

ELIMINÁ A parte de um [*identificador de segurança*](s-gly.md) (SID) que identifica um usuário ou grupo em relação à autoridade que emitiu o Sid.

</dd> <dt>

<span id="_security_relocated_store_gly"></span><span id="_SECURITY_RELOCATED_STORE_GLY"></span>**armazenamento realocado**
</dt> <dd>

Um [*repositório de certificados*](c-gly.md) que foi movido de seu local de registro padrão para um local diferente no registro.

</dd> <dt>

<span id="_security_remote_store_gly"></span><span id="_SECURITY_REMOTE_STORE_GLY"></span>**armazenamento remoto**
</dt> <dd>

Um [*repositório de certificados*](c-gly.md) localizado em outro computador, como um servidor de arquivos ou outro computador remoto compartilhado.

</dd> <dt>

<span id="_security_reply_apdu_gly"></span><span id="_SECURITY_REPLY_APDU_GLY"></span>**responder APDU**
</dt> <dd>

Uma APDU ( [*unidade de dados do protocolo de aplicativo*](a-gly.md) ) enviada em resposta a um APDU recebido.

</dd> <dt>

<span id="_security_repudiation_gly"></span><span id="_SECURITY_REPUDIATION_GLY"></span>**repúdio**
</dt> <dd>

A capacidade de um usuário de negar falsamente de ter executado uma ação enquanto outras partes não podem provar o contrário. Por exemplo, um usuário que excluiu um arquivo e que pode negar com êxito fazer isso.

</dd> <dt>

<span id="_security_resource_manager_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_GLY"></span>**Gerenciador de recursos**
</dt> <dd>

O módulo do subsistema de [*cartão inteligente*](s-gly.md) que gerencia o acesso a vários leitores e cartões inteligentes. O Gerenciador de recursos identifica e rastreia recursos, aloca leitores e recursos em vários aplicativos e dá suporte a primitivos de transações para acessar os serviços disponíveis em um determinado cartão.

</dd> <dt>

<span id="_security_resource_manager_api_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_API_GLY"></span>**API do Gerenciador de recursos**
</dt> <dd>

Um conjunto de funções do Windows que fornece acesso direto aos serviços do Gerenciador de recursos.

</dd> <dt>

<span id="_security_resource_manager_context_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_CONTEXT_GLY"></span>**contexto do Gerenciador de recursos**
</dt> <dd>

O contexto usado pelo Gerenciador de recursos ao acessar o banco de dados do cartão inteligente. O contexto do Gerenciador de recursos é usado principalmente pelas funções de consulta e gerenciamento ao acessar o banco de dados. O escopo do contexto do Gerenciador de recursos pode ser o usuário atual ou o sistema.

</dd> <dt>

<span id="_security_revocation_list_gly"></span><span id="_SECURITY_REVOCATION_LIST_GLY"></span>**lista de revogação**
</dt> <dd>

Consulte [*lista de certificados revogados*](c-gly.md).

</dd> <dt>

<span id="_security_rid_gly"></span><span id="_SECURITY_RID_GLY"></span>**ELIMINÁ**
</dt> <dd>

Consulte *identificador relativo*.

</dd> <dt>

<span id="_security_root_authority_gly"></span><span id="_SECURITY_ROOT_AUTHORITY_GLY"></span>**autoridade raiz**
</dt> <dd>

A [*autoridade de certificação*](c-gly.md) (CA) na parte superior de uma hierarquia de autoridade de certificação. A autoridade raiz certifica CAs no próximo nível da hierarquia.

</dd> <dt>

<span id="_security_root_certificate_gly"></span><span id="_SECURITY_ROOT_CERTIFICATE_GLY"></span>**certificado raiz**
</dt> <dd>

Um certificado de AC ( [*autoridade de certificação*](c-gly.md) ) autoassinado que identifica uma autoridade de certificação. Ele é chamado de certificado raiz porque é o certificado para a autoridade de certificação raiz. A AC raiz deve assinar seu próprio certificado de autoridade de certificação porque, por definição, não há nenhuma autoridade de certificação mais alta para assinar seu certificado de autoridade de certificação.

</dd> <dt>

<span id="_security_rsa_gly"></span><span id="_SECURITY_RSA_GLY"></span>**RSA**
</dt> <dd>

RSA Data Security, Inc., um grande desenvolvedor e editor de [*padrões de criptografia de chave pública*](p-gly.md) (PKCS). O "RSA" no nome representa os nomes dos três desenvolvedores e dos proprietários da empresa: Rivest, Shamir e Adleman.

</dd> <dt>

<span id="_security_rsa_keyx_gly"></span><span id="_SECURITY_RSA_KEYX_GLY"></span>**\_KEYX RSA**
</dt> <dd>

O nome do algoritmo [*CryptoAPI*](c-gly.md) para o algoritmo de troca de chave RSA. O CryptoAPI também faz referência a esse algoritmo por seu identificador de algoritmo (CALG \_ RSA \_ KEYX) e classe (alg \_ Class \_ Key \_ Exchange).

</dd> <dt>

<span id="_security_rsa_sign_gly"></span><span id="_SECURITY_RSA_SIGN_GLY"></span>**sinal da RSA \_**
</dt> <dd>

O nome do algoritmo CryptoAPI para o algoritmo de assinatura RSA. O CryptoAPI também faz referência a esse algoritmo por seu identificador de algoritmo (CALG \_ RSA \_ Sign) e classe ( \_ assinatura de classe alg \_ ).

</dd> <dt>

<span id="_security_rsa_public_key_algorithm_gly"></span><span id="_SECURITY_RSA_PUBLIC_KEY_ALGORITHM_GLY"></span>**Algoritmo de chave pública RSA**
</dt> <dd>

Um algoritmo de troca de chaves e assinatura baseado na popular codificação de chave pública RSA. Esse algoritmo é usado pelo PROV \_ RSA \_ Full, Prov \_ RSA \_ SIG, PROV \_ MS \_ Exchange e Prov \_ SSL Provider Types. O CryptoAPI referencia esse algoritmo por seus identificadores (CALG \_ RSA \_ KEYX e CALG \_ RSA \_ Sign), nomes (RSA \_ KEYX e RSA \_ Sign) e classe (alg \_ Class \_ Key \_ Exchange).

</dd> </dl>

 

 



