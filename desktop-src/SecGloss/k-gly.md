---
description: Contém definições de termos de segurança que começam com a letra K.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f17042c3-ba1a-408f-af55-5f171b0dee33
title: K (Glossário de segurança)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c92abf9b3df1eb49f0caaee90ccbce8755d003478683aba35570d9ea99fa2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895589"
---
# <a name="k-security-glossary"></a>K (Glossário de segurança)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J K [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_kca_gly"></span><span id="_SECURITY_KCA_GLY"></span>**KCA**
</dt> <dd>

Confira *autoridade de certificação de chave*.

</dd> <dt>

<span id="_security_kdc_gly"></span><span id="_SECURITY_KDC_GLY"></span>**KDC**
</dt> <dd>

Consulte *centro de distribuição de chaves*.

</dd> <dt>

<span id="_security_kea_gly"></span><span id="_SECURITY_KEA_GLY"></span>**KEA**
</dt> <dd>

Consulte *algoritmo de troca de chaves*.

</dd> <dt>

<span id="_security_kerberos_protocol_gly"></span><span id="_SECURITY_KERBEROS_PROTOCOL_GLY"></span>**Protocolo Kerberos**
</dt> <dd>

Um protocolo que define como os clientes interagem com um serviço de autenticação de rede. Os clientes obtêm tíquetes do centro de distribuição de chaves do Kerberos (KDC) e apresentam esses tíquetes para servidores quando as conexões são estabelecidas. Os tíquetes Kerberos representam as credenciais de rede do cliente.

</dd> <dt>

<span id="_security_key_blob_gly"></span><span id="_SECURITY_KEY_BLOB_GLY"></span>**BLOB de chaves**
</dt> <dd>

Um BLOB que contém uma chave privada criptografada. Os BLOBs de chave fornecem uma maneira de armazenar chaves fora do CSP. Os BLOBs de chave são criados exportando uma chave existente do CSP chamando a função **CryptExportKey** . Posteriormente, o BLOB de chave pode ser importado para um provedor (geralmente um CSP diferente em um computador diferente) chamando a função **CryptImportKey** . Isso cria uma chave no CSP que é uma duplicata da que foi exportada.

Consulte também [*blob de chave simples*](s-gly.md), [*blob de chave pública*](p-gly.md)e [*blob de chave privada*](p-gly.md).

</dd> <dt>

<span id="_security_key_blob_format_gly"></span><span id="_SECURITY_KEY_BLOB_FORMAT_GLY"></span>**formato de BLOB de chave**
</dt> <dd>

O formato do BLOB de chave quando uma chave pública ou de sessão é exportada de um CSP. O formato é especificado pelo tipo de provedor do CSP de exportação. Um BLOB de chave é criado chamando **CryptExportKey**.

Consulte também [*blob de chave pública*](p-gly.md) e [*blob de chave simples*](s-gly.md).

</dd> <dt>

<span id="_security_key_certification_authority_gly"></span><span id="_SECURITY_KEY_CERTIFICATION_AUTHORITY_GLY"></span>**autoridade de certificação de chave**
</dt> <dd>

(KCA) Uma entidade confiável que normalmente mantém um banco de dados seguro de mensagens compostas assinadas com a chave privada do KCA. Em implementações práticas, as mensagens compostas consistem no nome do usuário, na chave pública do usuário e em qualquer outra informação importante sobre o usuário. Quando o aplicativo receptor Obtém uma mensagem assinada de um usuário, o aplicativo pode verificar a chave pública recebida com a mensagem comparando-a à chave pública armazenada no banco de dados KCA.

</dd> <dt>

<span id="_security_key_container_gly"></span><span id="_SECURITY_KEY_CONTAINER_GLY"></span>**contêiner de chave**
</dt> <dd>

Uma parte do banco de dados de chave que contém todos os pares de chaves (pares de chaves de assinatura e de troca) que pertencem a um usuário específico. Cada contêiner tem um nome exclusivo que é usado ao chamar a função **CryptAcquireContext** para obter um identificador para o contêiner.

</dd> <dt>

<span id="_security_key_database_gly"></span><span id="_SECURITY_KEY_DATABASE_GLY"></span>**banco de dados principal**
</dt> <dd>

Um banco de dados que contém as chaves de criptografia persistentes para um CSP específico. O banco de dados contém um ou mais contêineres de chave, que armazenam individualmente todos os pares de chaves de criptografia para um usuário específico.

Consulte também *contêiner de chave*.

</dd> <dt>

<span id="_security_key_distribution_center_gly"></span><span id="_SECURITY_KEY_DISTRIBUTION_CENTER_GLY"></span>**centro de distribuição de chaves**
</dt> <dd>

KDC Um serviço de rede que fornece tíquetes de sessão e chaves de sessão temporárias usados no protocolo de autenticação Kerberos v5. O KDC é executado como um processo privilegiado em todos os controladores de domínio.

Consulte também *protocolo Kerberos*.

</dd> <dt>

<span id="_security_key_exchange_algorithm_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_GLY"></span>**algoritmo de troca de chaves**
</dt> <dd>

Um algoritmo usado para criptografar e descriptografar chaves do Exchange (chaves de sessão simétricas). Alguns algoritmos de troca de chave comuns incluem Diffie-Hellman e KEA, o algoritmo de troca de chave especificado por um tipo de provedor do PROV \_ Fortezza. O algoritmo KEA é uma versão aprimorada do algoritmo Diffie-Hellman. Cada tipo de provedor pode especificar apenas um algoritmo de troca de chave.

</dd> <dt>

<span id="_security_key_exchange_algorithm_name_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_NAME_GLY"></span>**algoritmo de Exchange de chave**
</dt> <dd>

(KEA) O algoritmo de troca de chave especificado por um tipo de provedor do PROV \_ Fortezza. Esse algoritmo é uma versão aprimorada do algoritmo de Diffie-Hellman.

</dd> <dt>

<span id="_security_key_exchange_certificate_gly"></span><span id="_SECURITY_KEY_EXCHANGE_CERTIFICATE_GLY"></span>**certificado de troca de chave**
</dt> <dd>

Um certificado usado para criptografar informações enviadas a outra entidade. O certificado de troca de chave de autoridade de certificação (CA) pode ser usado por um cliente para criptografar as informações enviadas para a autoridade de certificação.

</dd> <dt>

<span id="_security_key_exchange_functions_gly"></span><span id="_SECURITY_KEY_EXCHANGE_FUNCTIONS_GLY"></span>**funções de troca de chaves**
</dt> <dd>

Um conjunto de funções usadas para trocar ou transmitir chaves. As funções de troca de chaves também podem ser usadas para implementar trocas de chave de três fases totalmente autenticadas.

</dd> <dt>

<span id="_security_key_exchange_key_pair_gly"></span><span id="_SECURITY_KEY_EXCHANGE_KEY_PAIR_GLY"></span>**par de chaves-troca de chaves**
</dt> <dd>

Consulte [*par de chaves do Exchange*](e-gly.md).

</dd> <dt>

<span id="_security_key_exchange_private_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PRIVATE_KEY_GLY"></span>**chave privada de troca de chaves**
</dt> <dd>

A chave privada de um par de chaves do Exchange.

Consulte também [*par de chaves do Exchange*](e-gly.md).

</dd> <dt>

<span id="_security_key_exchange_protocol_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PROTOCOL_GLY"></span>**Protocolo de troca de chaves**
</dt> <dd>

Um protocolo pelo qual duas partes trocam informações para estabelecer um segredo compartilhado. O segredo compartilhado é normalmente usado como uma chave de criptografia simétrica.

</dd> <dt>

<span id="_security_key_exchange_public_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PUBLIC_KEY_GLY"></span>**chave pública de troca de chaves**
</dt> <dd>

A chave pública de um par de chaves do Exchange.

Consulte também [*par de chaves do Exchange*](e-gly.md).

</dd> <dt>

<span id="_security_key_generation_functions_gly"></span><span id="_SECURITY_KEY_GENERATION_FUNCTIONS_GLY"></span>**funções de geração de chave**
</dt> <dd>

Um conjunto de funções usadas por aplicativos para gerar e personalizar chaves de criptografia. Essas funções incluem suporte completo para a alteração de modos de encadeamento, vetores de inicialização e outros recursos de criptografia.

</dd> <dt>

<span id="_security_key_length_gly"></span><span id="_SECURITY_KEY_LENGTH_GLY"></span>**comprimento da chave**
</dt> <dd>

Valores especificados por alguns provedores que indicam o comprimento dos pares de chaves pública/privada e chaves de sessão usados com esse provedor.

</dd> <dt>

<span id="_security_key_pair_gly"></span><span id="_SECURITY_KEY_PAIR_GLY"></span>**par de chaves**
</dt> <dd>

Uma chave privada e sua chave pública relacionada.

</dd> <dt>

<span id="_security_key_storage_provider_gly"></span><span id="_SECURITY_KEY_STORAGE_PROVIDER_GLY"></span>**provedor de armazenamento de chaves**
</dt> <dd>

KSP Um módulo de software independente que implementa a funcionalidade para criar, gerenciar, armazenar e recuperar [*chaves privadas*](p-gly.md).

</dd> <dt>

<span id="_security_ksp_gly"></span><span id="_SECURITY_KSP_GLY"></span>**KSP**
</dt> <dd>

Consulte *provedor de armazenamento de chaves*.

</dd> </dl>

 

 



