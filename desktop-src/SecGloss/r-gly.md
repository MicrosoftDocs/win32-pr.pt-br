---
description: Contém definições de termos de segurança que começam com a letra R.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ce589e18-02ac-42c2-b76b-776deb686bbd
title: R (Glossário de Segurança)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a566a939746cd65c6336e8f31ff05a7ee3f0a3b7954e9d790d3f15a8163f138b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895285"
---
# <a name="r-security-glossary"></a>R (Glossário de Segurança)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) L [](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q R [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_rc2_gly"></span><span id="_SECURITY_RC2_GLY"></span>**RC2**
</dt> <dd>

O [*nome do algoritmo CryptoAPI*](c-gly.md) para o algoritmo RC2.

Consulte também o *algoritmo de bloco RC2*.

</dd> <dt>

<span id="_security_rc2_block_algorithm_gly"></span><span id="_SECURITY_RC2_BLOCK_ALGORITHM_GLY"></span>**Algoritmo de bloco RC2**
</dt> <dd>

Um algoritmo [*de criptografia*](e-gly.md) de dados com base na codificação de bloco simétrico rc2 de 64 bits. RC2 é especificado pelos tipos de provedor \_ PROV RSA \_ FULL. [*CryptoAPI*](c-gly.md) faz referência a esse algoritmo por seu identificador (CALG \_ RC2), nome (RC2) e classe (ALG \_ CLASS DATA \_ \_ ENCRYPT).

</dd> <dt>

<span id="_security_rc4_gly"></span><span id="_SECURITY_RC4_GLY"></span>**RC4**
</dt> <dd>

O [*nome do algoritmo CryptoAPI*](c-gly.md) para o algoritmo RC4.

Consulte também algoritmo *de fluxo RC4*.

</dd> <dt>

<span id="_security_rc4_stream_algorithm_gly"></span><span id="_SECURITY_RC4_STREAM_ALGORITHM_GLY"></span>**Algoritmo de fluxo RC4**
</dt> <dd>

Um algoritmo [*de criptografia*](e-gly.md) de dados com base na codificação de fluxo simétrico RC4. RC4 é especificado pelos tipos de provedor \_ PROV RSA \_ FULL. [*CryptoAPI*](c-gly.md) faz referência a esse algoritmo por seu identificador (CALG \_ RC4), nome (RC4) e classe (ALG \_ CLASS DATA \_ \_ ENCRYPT).

</dd> <dt>

<span id="_security_rdn_gly"></span><span id="_SECURITY_RDN_GLY"></span>**Rdn**
</dt> <dd>

Consulte *o nome diferenciado relativo*.

</dd> <dt>

<span id="_security_reader_gly"></span><span id="_SECURITY_READER_GLY"></span>**Leitor**
</dt> <dd>

Um dispositivo padrão dentro do [*subsistema de cartão*](s-gly.md) inteligente. Um IFD (dispositivo de interface) que dá suporte à entrada/saída bidirecional para um cartão inteligente. Ele pode estar associado a um sistema inteiro, a um ou mais grupos de leitor ou a um terminal específico. O subsistema de cartão inteligente permite que um leitor seja dedicado ao terminal ao qual ele é atribuído. No entanto, atualmente, há apenas um terminal em um computador.

</dd> <dt>

<span id="_security_reader_driver_gly"></span><span id="_SECURITY_READER_DRIVER_GLY"></span>**driver de leitor**
</dt> <dd>

Um driver específico que mapeia serviços de driver para um dispositivo de leitor de hardware específico. Ele deve comunicar eventos de [](s-gly.md) inserção e remoção de cartão para o driver de classe de cartão inteligente para encaminhamento para o gerenciador de recursos de cartão inteligente e deve fornecer recursos de troca de dados para o cartão por qualquer protocolo bruto, T=0, T=1 ou PTS.

</dd> <dt>

<span id="_security_reader_group_gly"></span><span id="_SECURITY_READER_GROUP_GLY"></span>**grupo de leitor**
</dt> <dd>

Um grupo lógico de leitores. Os grupos de leitor podem ser definidos pelo sistema ou criados por usuários ou administradores. Grupos de leitores são usados por funções de cartão inteligente que podem agir sobre grupos de leitores. Para evitar colisões de nomeação com grupos definidos pelo usuário, a Microsoft reserva o uso de qualquer nome que contenha o cifrão ($).

</dd> <dt>

<span id="_security_reader_helper_driver_gly"></span><span id="_SECURITY_READER_HELPER_DRIVER_GLY"></span>**driver auxiliar de leitor**
</dt> <dd>

Fornece rotinas comuns de suporte ao driver de cartão inteligente e suporte ao protocolo T=0 e T=1 adicionais para drivers específicos, conforme necessário.

</dd> <dt>

<span id="_security_reference_count_gly"></span><span id="_SECURITY_REFERENCE_COUNT_GLY"></span>**contagem de referências**
</dt> <dd>

Um valor inteiro usado para manter o controle de um objeto COM. Quando um objeto é criado, sua contagem de referência é definida como um. Sempre que uma interface é vinculada ao objeto, sua contagem de referência é incrementada; quando a conexão de interface é destruída, a contagem de referência é decrementada. O objeto é destruído quando a contagem de referência atinge zero. Todas as interfaces para esse objeto não são válidas.

</dd> <dt>

<span id="_security_relative_distinguished_name_gly"></span><span id="_SECURITY_RELATIVE_DISTINGUISHED_NAME_GLY"></span>**nome diferenciado relativo**
</dt> <dd>

(RDN) Uma entidade incluída como a entidade em uma solicitação de um certificado. Os elementos em um RDN são definidos por seus atributos e não precisam incluir um nome. Em relação ao [*CryptoAPI*](c-gly.md), um RDN é definido por uma estrutura cert RDN, que, por sua vez, aponta para uma matriz de estruturas de atributo \_ \_ CERT RDN \_ ATTR. Cada estrutura de atributo especifica um único atributo.

</dd> <dt>

<span id="_security_relative_identifier_gly"></span><span id="_SECURITY_RELATIVE_IDENTIFIER_GLY"></span>**identificador relativo**
</dt> <dd>

(RID) A parte de um SID [*(identificador*](s-gly.md) de segurança) que identifica um usuário ou grupo em relação à autoridade que emitiu o SID.

</dd> <dt>

<span id="_security_relocated_store_gly"></span><span id="_SECURITY_RELOCATED_STORE_GLY"></span>**loja realocada**
</dt> <dd>

Um [*armazenamento de*](c-gly.md) certificados que foi movido de seu local de registro padrão para um local diferente no Registro.

</dd> <dt>

<span id="_security_remote_store_gly"></span><span id="_SECURITY_REMOTE_STORE_GLY"></span>**armazenamento remoto**
</dt> <dd>

Um [*armazenamento de certificados*](c-gly.md) localizado em outro computador, como um servidor de arquivos ou algum outro computador remoto compartilhado.

</dd> <dt>

<span id="_security_reply_apdu_gly"></span><span id="_SECURITY_REPLY_APDU_GLY"></span>**APDU de resposta**
</dt> <dd>

Uma [*APDU (unidade de*](a-gly.md) dados de protocolo de aplicativo) enviada em resposta a um APDU recebido.

</dd> <dt>

<span id="_security_repudiation_gly"></span><span id="_SECURITY_REPUDIATION_GLY"></span>**Repúdio**
</dt> <dd>

A capacidade de um usuário negar falsamente ter executado uma ação, enquanto outras partes não podem provar o contrário. Por exemplo, um usuário que excluiu um arquivo e que pode negar com êxito ter feito isso.

</dd> <dt>

<span id="_security_resource_manager_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_GLY"></span>**gerenciador de recursos**
</dt> <dd>

O módulo do [*subsistema de cartão*](s-gly.md) inteligente que gerencia o acesso a vários leitores e cartões inteligentes. O gerenciador de recursos identifica e rastreia recursos, aloca leitores e recursos em vários aplicativos e dá suporte a primitivos de transação para acessar os serviços disponíveis em um determinado cartão.

</dd> <dt>

<span id="_security_resource_manager_api_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_API_GLY"></span>**API do gerenciador de recursos**
</dt> <dd>

Um conjunto de Windows funções que fornecem acesso direto aos serviços do gerenciador de recursos.

</dd> <dt>

<span id="_security_resource_manager_context_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_CONTEXT_GLY"></span>**contexto do gerenciador de recursos**
</dt> <dd>

O contexto usado pelo gerenciador de recursos ao acessar o banco de dados de cartão inteligente. O contexto do gerenciador de recursos é usado principalmente pelas funções de consulta e gerenciamento ao acessar o banco de dados. O escopo do contexto do gerenciador de recursos pode ser o usuário atual ou o sistema.

</dd> <dt>

<span id="_security_revocation_list_gly"></span><span id="_SECURITY_REVOCATION_LIST_GLY"></span>**lista de revogação**
</dt> <dd>

Consulte [*Lista de certificados revogados.*](c-gly.md)

</dd> <dt>

<span id="_security_rid_gly"></span><span id="_SECURITY_RID_GLY"></span>**Livrar**
</dt> <dd>

Consulte *o identificador relativo*.

</dd> <dt>

<span id="_security_root_authority_gly"></span><span id="_SECURITY_ROOT_AUTHORITY_GLY"></span>**autoridade raiz**
</dt> <dd>

A [*AC (autoridade*](c-gly.md) de certificação) na parte superior de uma hierarquia de AC. A autoridade raiz certifica as AAs no próximo nível da hierarquia.

</dd> <dt>

<span id="_security_root_certificate_gly"></span><span id="_SECURITY_ROOT_CERTIFICATE_GLY"></span>**certificado raiz**
</dt> <dd>

Um certificado de AC [*(autoridade*](c-gly.md) de certificação) auto-assinada que identifica uma AC. Ele é chamado de certificado raiz porque é o certificado para a AC raiz. A AC raiz deve assinar seu próprio certificado de autoridade de certificação porque, por definição, não há autoridade de certificação mais alta para assinar seu certificado de autoridade de certificação.

</dd> <dt>

<span id="_security_rsa_gly"></span><span id="_SECURITY_RSA_GLY"></span>**Rsa**
</dt> <dd>

RSA Data Security, Inc., um desenvolvedor principal e editor de PKCS (public [*key cryptography standards).*](p-gly.md) O "RSA" no nome significa os nomes dos três desenvolvedores e proprietários da empresa: Rivest, Shimir e Adleman.

</dd> <dt>

<span id="_security_rsa_keyx_gly"></span><span id="_SECURITY_RSA_KEYX_GLY"></span>**RSA \_ KEYX**
</dt> <dd>

O [*nome do algoritmo CryptoAPI*](c-gly.md) para o algoritmo de troca de chaves RSA. CryptoAPI também faz referência a esse algoritmo por seu identificador de algoritmo (CALG \_ RSA \_ KEYX) e classe (ALG \_ CLASS KEY \_ \_ EXCHANGE).

</dd> <dt>

<span id="_security_rsa_sign_gly"></span><span id="_SECURITY_RSA_SIGN_GLY"></span>**RSA \_ SIGN**
</dt> <dd>

O nome do algoritmo CryptoAPI para o algoritmo de assinatura RSA. CryptoAPI também faz referência a esse algoritmo por seu identificador de algoritmo (CALG RSA SIGN) e \_ \_ classe (ALG \_ CLASS \_ SIGNATURE).

</dd> <dt>

<span id="_security_rsa_public_key_algorithm_gly"></span><span id="_SECURITY_RSA_PUBLIC_KEY_ALGORITHM_GLY"></span>**Algoritmo chave pública RSA**
</dt> <dd>

Um algoritmo de troca de chaves e assinatura com base na popular criptografia de Chave Pública RSA. Esse algoritmo é usado pelos tipos de provedor \_ PROV RSA \_ FULL, PROV \_ RSA \_ SIG, PROV MS EXCHANGE e \_ \_ PROV \_ SSL. CryptoAPI faz referência a esse algoritmo por seus identificadores (CALG RSA KEYX e \_ CALG RSA SIGN), nomes (RSA KEYX e RSA SIGN) e \_ classe \_ \_ \_ \_ (ALG \_ CLASS KEY \_ \_ EXCHANGE).

</dd> </dl>

 

 



