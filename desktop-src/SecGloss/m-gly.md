---
description: Contém definições de termos de segurança que começam com a letra M.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 4c4402e9-7455-4868-978f-3899a8fd86c1
title: M (Glossário de segurança)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63fc76d4b8b803d523c46012dcb10ed5380e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922107"
---
# <a name="m-security-glossary"></a>M (Glossário de segurança)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) M [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_mac_gly"></span><span id="_SECURITY_MAC_GLY"></span>**MAC**
</dt> <dd>

Consulte *Message Authentication Code*.

</dd> <dt>

<span id="_security_mac_key_gly"></span><span id="_SECURITY_MAC_KEY_GLY"></span>**Chave MAC**
</dt> <dd>

Uma chave de código de autenticação de mensagem usada com protocolos [*Schannel*](s-gly.md) .

</dd> <dt>

<span id="_security_master_key_gly"></span><span id="_SECURITY_MASTER_KEY_GLY"></span>**chave mestra**
</dt> <dd>

A chave usada pelo cliente e servidor para toda a geração de chave de sessão. A chave mestra é usada para gerar a chave de leitura do cliente, a chave de gravação do cliente, a chave de leitura do servidor e a chave de gravação do servidor. As chaves mestras podem ser exportadas como BLOBs de chave simples.

</dd> <dt>

<span id="_security_md2_gly"></span><span id="_SECURITY_MD2_GLY"></span>**MD2**
</dt> <dd>

O nome do algoritmo CryptoAPI para o algoritmo de hash MD2. Outros algoritmos de hash incluem *MD4*, *MD5* e [*Sha*](s-gly.md).

Consulte também *algoritmo MD2*.

</dd> <dt>

<span id="_security_md2_algorithm_gly"></span><span id="_SECURITY_MD2_ALGORITHM_GLY"></span>**Algoritmo MD2**
</dt> <dd>

MD2 Um algoritmo de hash que cria um valor de hash de 128 bits. O MD2 foi otimizado para uso com computadores de 8 bits. O CryptoAPI faz referência a esse algoritmo por seu tipo (CALG \_ md2), nome (Mac) e classe ( \_ hash de classe alg \_ ). O MD2 foi desenvolvido pela RSA Data Security, Inc.

Consulte também *algoritmo MD4*, *algoritmo MD5*.

</dd> <dt>

<span id="_security_md4_gly"></span><span id="_SECURITY_MD4_GLY"></span>**MD4**
</dt> <dd>

O nome do algoritmo CryptoAPI para o algoritmo de hash MD4. Outros algoritmos de hash incluem *MD2*, *MD5* e [*Sha*](s-gly.md).

Consulte *algoritmo MD4*.

</dd> <dt>

<span id="_security_md4_algorithm_gly"></span><span id="_SECURITY_MD4_ALGORITHM_GLY"></span>**Algoritmo MD4**
</dt> <dd>

MD4 Um algoritmo de hash que cria um valor de hash de 128 bits. O MD4 foi otimizado para computadores de 32 bits. Agora, ele é considerado desfeito porque as colisões podem ser encontradas com muita rapidez e facilidade. O MD4 foi desenvolvido pela RSA Data Security, Inc.

Consulte também *algoritmo MD2*, *algoritmo MD5*.

</dd> <dt>

<span id="_security_md5_gly"></span><span id="_SECURITY_MD5_GLY"></span>**MD5**
</dt> <dd>

O nome do algoritmo CryptoAPI para o algoritmo de hash MD5. Outros algoritmos de hash incluem *MD2*, *MD4* e [*Sha*](s-gly.md).

Consulte também *algoritmo MD5*.

</dd> <dt>

<span id="_security_md5_algorithm_gly"></span><span id="_SECURITY_MD5_ALGORITHM_GLY"></span>**Algoritmo MD5**
</dt> <dd>

MD5 Um algoritmo de hash que cria um valor de hash de 128 bits. O MD5 foi otimizado para computadores de 32 bits. O CryptoAPI faz referência a esse algoritmo por seu identificador de algoritmo (CALG \_ MD5), nome (MD5) e classe ( \_ hash de classe alg \_ ). O MD5 foi desenvolvido pela RSA Data Security, Inc. e é especificado por PROV \_ RSA \_ Full, Prov \_ RSA \_ SIG, Prov \_ DSS, Prov \_ DSS \_ DH e Prov \_ MS \_ Exchange Provider Types.

Consulte também *algoritmo MD2*, *algoritmo MD4*.

</dd> <dt>

<span id="_security_message_gly"></span><span id="_SECURITY_MESSAGE_GLY"></span>**Mensagem**
</dt> <dd>

Todos os dados que foram codificados para transmissão ou recebimento de uma pessoa ou entidade. As mensagens podem ser criptografadas para privacidade, assinadas digitalmente para fins de autenticação ou ambos.

</dd> <dt>

<span id="_security_message_digest_gly"></span><span id="_SECURITY_MESSAGE_DIGEST_GLY"></span>**Resumo da mensagem**
</dt> <dd>

Consulte [*hash*](h-gly.md).

</dd> <dt>

<span id="_security_message_authentication_code_gly"></span><span id="_SECURITY_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**Message Authentication Code**
</dt> <dd>

Mac Um algoritmo de hash codificado que usa uma chave de sessão simétrica para ajudar a garantir que um bloco de dados tenha mantido sua integridade desde o momento em que foi enviado até o momento em que foi recebido. Ao usar esse tipo de algoritmo, o aplicativo de recebimento também deve possuir a chave de sessão para recalcular o valor de hash para que ele possa verificar se os dados base não foram alterados. O CryptoAPI referencia esse algoritmo por seu tipo ( \_ Mac CALG), Name (Mac) e classe (alg \_ Class \_ hash).

</dd> <dt>

<span id="_security_message_encoding_type_gly"></span><span id="_SECURITY_MESSAGE_ENCODING_TYPE_GLY"></span>**tipo de codificação de mensagem**
</dt> <dd>

Define como a mensagem é codificada. O tipo de codificação de mensagem é armazenado na palavra de ordem superior da estrutura do tipo de codificação. Os tipos de codificação definidos atualmente são \_ : \_ codificação ASN cript, \_ codificação ASN X509 \_ e \_ \_ codificação ASN PKCS 7 \_ .

</dd> <dt>

<span id="_security_message_management_functions_gly"></span><span id="_SECURITY_MESSAGE_MANAGEMENT_FUNCTIONS_GLY"></span>**funções de gerenciamento de mensagens**
</dt> <dd>

Funções que fornecem dois níveis de gerenciamento de mensagens: funções de mensagens de nível baixo e funções de mensagens simplificadas. As funções de mensagem de nível baixo fornecem mais flexibilidade do que as funções de mensagens simplificadas; no entanto, eles exigem mais chamadas de função.

</dd> <dt>

<span id="_security_message_signing_functions_gly"></span><span id="_SECURITY_MESSAGE_SIGNING_FUNCTIONS_GLY"></span>**funções de assinatura de mensagens**
</dt> <dd>

Funções usadas para assinar mensagens e dados.

Consulte também [*funções de mensagens simplificadas*](s-gly.md).

</dd> <dt>

<span id="_security_mpr_gly"></span><span id="_SECURITY_MPR_GLY"></span>**MPR**
</dt> <dd>

Consulte *vários roteadores do provedor*.

</dd> <dt>

<span id="_security_multiple_provider_router_gly"></span><span id="_SECURITY_MULTIPLE_PROVIDER_ROUTER_GLY"></span>**Roteador de vários provedores**
</dt> <dd>

MPR Um componente do sistema que manipula as comunicações entre o sistema e todos os provedores de rede. O MPR chama as funções de provedor de rede que são expostas por cada provedor de rede.

</dd> </dl>

 

 



