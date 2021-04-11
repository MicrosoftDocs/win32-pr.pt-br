---
title: Nível de autenticação
description: O nível de autenticação controla a quantidade de segurança que um cliente ou servidor deseja de seu SSP.
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250661e4a8da42ffd91f37e282a39fbb52b6328a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292849"
---
# <a name="authentication-level"></a>Nível de autenticação

O nível de autenticação controla a quantidade de segurança que um cliente ou servidor deseja de seu SSP. O nível de autenticação é definido passando um \_ valor xxx de nível de autenticação RPC C apropriado \_ \_ \_ para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) por meio do parâmetro *dwAuthnLevel* . Os níveis de autenticação do cliente e do servidor são comparados durante o handshake, e a configuração de proteção de segurança de nível superior é usada para a conexão.

Os diferentes níveis de autenticação são descritos da seguinte maneira, da proteção de segurança de nível mais baixo para a mais alta:

<dl> <dt>

<span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>Nenhum (RPC \_ C \_ Authn \_ nível \_ nenhum)
</dt> <dd>

Nenhuma autenticação é executada durante a comunicação entre o cliente e o servidor. Todas as configurações de segurança são ignoradas. Esse nível de autenticação poderá ser definido somente se o [nível de serviço de autenticação](com-authentication-service-constants.md) for RPC \_ C \_ Authn \_ None.

</dd> <dt>

<span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Padrão ( \_ padrão de \_ nível de autenticação RPC C \_ \_ )
</dt> <dd>

COM escolhe o nível de autenticação usando sua negociação de cobertura de segurança normal. Ele nunca escolherá um nível de autenticação de nenhum.

</dd> <dt>

<span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Conectar ( \_ conexão em \_ nível de autenticação RPC C \_ \_ )
</dt> <dd>

O handshake de autenticação normal ocorre entre o cliente e o servidor, e uma chave de sessão é estabelecida, mas essa chave nunca é usada para comunicação entre o cliente e o servidor. Toda a comunicação após o handshake não é segura.

</dd> <dt>

<span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Chamada ( \_ chamada de \_ nível de autenticação RPC C \_ \_ )
</dt> <dd>

Somente os cabeçalhos do início de cada chamada são assinados. O restante dos dados trocados entre o cliente e o servidor não é assinado nem criptografado. A maioria dos SSPs não dá suporte a esse nível de autenticação e o promove silenciosamente para o pacote.

</dd> <dt>

<span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Pacote (RPC \_ C \_ Authn \_ nível \_ PKT)
</dt> <dd>

O cabeçalho de cada pacote é assinado, mas não criptografado. Os próprios pacotes não são assinados ou criptografados.

</dd> <dt>

<span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Integridade do pacote ( \_ integridade do PCT do nível de autenticação RPC C \_ \_ \_ \_ )
</dt> <dd>

Cada pacote de dados é assinado em sua totalidade, mas não é criptografado. Como todos os dados são assinados pelo remetente, o destinatário pode ter certeza de que nenhum dos dados foi adulterado durante o trânsito.

</dd> <dt>

<span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Privacidade de pacote ( \_ privacidade do PCT do nível de autenticação RPC C \_ \_ \_ \_ )
</dt> <dd>

Cada pacote de dados é assinado e criptografado. Isso ajuda a proteger toda a comunicação entre o cliente e o servidor.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[AuthenticationLevel](authenticationlevel.md)
</dt> <dt>

[LegacyAuthenticationLevel](legacyauthenticationlevel.md)
</dt> </dl>

 

 




