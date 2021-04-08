---
description: Contém definições de termos de segurança que começam com a letra L.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 65dd9a04-fc7c-4179-95ff-dac7dad4668f
title: L (Glossário de segurança)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33ee054c2bcf414ef289cc381ac13ef970da6dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829146"
---
# <a name="l-security-glossary"></a>L (Glossário de segurança)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) L [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_ldap_gly"></span><span id="_SECURITY_LDAP_GLY"></span>**LDAP**
</dt> <dd>

Consulte *Lightweight Directory Access Protocol*

</dd> <dt>

<span id="_security_lightweight_directory_access_protocol_gly"></span><span id="_SECURITY_LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL_GLY"></span>**Protocolo Lightweight Directory Access**
</dt> <dd>

Um subconjunto mais facilmente implementado do padrão X. 500 DAP para serviços de diretório.

</dd> <dt>

<span id="_security_little_endian_gly"></span><span id="_SECURITY_LITTLE_ENDIAN_GLY"></span>**little-endian**
</dt> <dd>

Um formato de memória ou de dados no qual o byte menos significativo é armazenado no endereço inferior ou chega primeiro.

Consulte também [*big endian*](b-gly.md).

</dd> <dt>

<span id="_security_locally_unique_identifier_gly"></span><span id="_SECURITY_LOCALLY_UNIQUE_IDENTIFIER_GLY"></span>**identificador local exclusivo**
</dt> <dd>

LUID Um valor de 64 bits com garantia de ser exclusivo no sistema operacional que o gerou até que o sistema seja reiniciado.

</dd> <dt>

<span id="_security_local_registration_authority_gly"></span><span id="_SECURITY_LOCAL_REGISTRATION_AUTHORITY_GLY"></span>**autoridade de registro local**
</dt> <dd>

(LRA) Um intermediário entre um Publicador e uma [*autoridade de certificação*](c-gly.md) (CA). O LRA pode, por exemplo, verificar as credenciais de um Publicador antes de enviá-las para a autoridade de certificação.

</dd> <dt>

<span id="_security_local_security_authority_gly"></span><span id="_SECURITY_LOCAL_SECURITY_AUTHORITY_GLY"></span>**Autoridade de segurança local**
</dt> <dd>

LSA Um subsistema protegido que autentica e registra os usuários no sistema local. O LSA também mantém informações sobre todos os aspectos da segurança local em um sistema, coletivamente conhecido como a diretiva de segurança local do sistema.

</dd> <dt>

<span id="_security_logical_store_gly"></span><span id="_SECURITY_LOGICAL_STORE_GLY"></span>**repositório lógico**
</dt> <dd>

Consulte [*repositório virtual*](v-gly.md).

</dd> <dt>

<span id="_security_logon_data_gly"></span><span id="_SECURITY_LOGON_DATA_GLY"></span>**dados de logon**
</dt> <dd>

Informações apresentadas ao sistema por uma [*entidade de segurança*](s-gly.md) para autenticação.

</dd> <dt>

<span id="_security_logon_identifier_gly"></span><span id="_SECURITY_LOGON_IDENTIFIER_GLY"></span>**identificador de logon**
</dt> <dd>

Um LUID que identifica uma *sessão de logon*. Uma ID de logon é válida até que o usuário faça logoff. Uma ID de logon é exclusiva enquanto o computador está em execução; nenhuma outra sessão de logon terá a mesma ID de logon. No entanto, o conjunto de possíveis IDs de logon é redefinido quando o computador é iniciado. Para recuperar a ID de logon de um [*token de acesso*](a-gly.md), chame a função **GetTokenInformation** para TokenStatistics; a ID de logon está no membro **authenticationid** .

</dd> <dt>

<span id="_security_logon_session_gly"></span><span id="_SECURITY_LOGON_SESSION_GLY"></span>**sessão de logon**
</dt> <dd>

Uma sessão de logon começa sempre que um usuário faz logon em um computador. Todos os processos em uma sessão de logon têm o mesmo [*token de acesso*](a-gly.md)primário. O token de acesso contém informações sobre o contexto de segurança da sessão de logon, incluindo o SID do usuário, o *identificador de logon* e o *Sid de logon*.

</dd> <dt>

<span id="_security_logon_sid_gly"></span><span id="_SECURITY_LOGON_SID_GLY"></span>**SID de logon**
</dt> <dd>

Um SID ( [*identificador de segurança*](s-gly.md) ) que identifica uma *sessão de logon*. Você pode usar o SID de logon em uma [*DACL*](d-gly.md) para controlar o acesso durante uma sessão de logon. Um SID de logon é válido até que o usuário faça logoff. Um SID de logon é exclusivo enquanto o computador está em execução; nenhuma outra sessão de logon terá o mesmo SID de logon. No entanto, o conjunto de possíveis SIDs de logon é redefinido quando o computador é iniciado. Para recuperar o SID de logon de um [*token de acesso*](a-gly.md), chame a função **GetTokenInformation** para tokenGroups.

</dd> <dt>

<span id="_security_low_level_message_functions_gly"></span><span id="_SECURITY_LOW_LEVEL_MESSAGE_FUNCTIONS_GLY"></span>**funções de mensagem de nível baixo**
</dt> <dd>

Funções de gerenciamento de mensagens que operam em um nível mais alto do que as funções criptográficas base. Essas funções fornecem funcionalidade para codificar dados para transmissão e para decodificar dados recebidos. As funções de mensagens de nível baixo fornecem mais flexibilidade do que as funções de mensagens simplificadas, mas exigem mais chamadas de função.

Consulte também [*funções de mensagens simplificadas*](s-gly.md).

</dd> <dt>

<span id="_security_lsa_gly"></span><span id="_SECURITY_LSA_GLY"></span>**LSA**
</dt> <dd>

Consulte *autoridade de segurança local*.

</dd> <dt>

<span id="_security_luid_gly"></span><span id="_SECURITY_LUID_GLY"></span>**LUID**
</dt> <dd>

Consulte *identificador local exclusivo*.

</dd> </dl>

 

 



