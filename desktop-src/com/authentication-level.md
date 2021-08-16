---
title: Nível de autenticação
description: O nível de autenticação controla a segurança que um cliente ou servidor deseja de seu SSP.
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c468408a22f1ea0c0fae67d7ce3d5f5b40f8a6342538614c1619acd40574ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311146"
---
# <a name="authentication-level"></a>Nível de autenticação

O nível de autenticação controla a segurança que um cliente ou servidor deseja de seu SSP. O nível de autenticação é definido passando um valor AUTHN LEVEL xxx de RPC C apropriado para \_ \_ \_ \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) por meio do parâmetro *dwAuthnLevel.* Os níveis de autenticação do cliente e do servidor são comparados durante o handshake e a configuração de proteção de segurança de nível superior é usada para a conexão.

Os diferentes níveis de autenticação são descritos da seguinte maneira, da proteção de segurança de nível mais baixo ao mais alto:

<dl> <dt>

<span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>None (RPC \_ C \_ AUTHN \_ LEVEL \_ NONE)
</dt> <dd>

Nenhuma autenticação é executada durante a comunicação entre o cliente e o servidor. Todas as configurações de segurança são ignoradas. Esse nível de autenticação só poderá ser definido se o nível [de serviço de autenticação](com-authentication-service-constants.md) for RPC \_ C \_ AUTHN \_ NONE.

</dd> <dt>

<span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Padrão (RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT)
</dt> <dd>

O COM escolhe o nível de autenticação usando sua negociação normal de garantia de segurança. Ele nunca escolherá um nível de autenticação Nenhum.

</dd> <dt>

<span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Conexão (RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT)
</dt> <dd>

O handshake de autenticação normal ocorre entre o cliente e o servidor e uma chave de sessão é estabelecida, mas essa chave nunca é usada para comunicação entre o cliente e o servidor. Toda a comunicação após o handshake não é sesseure.

</dd> <dt>

<span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Chamada (RPC \_ C CHAMADA DE NÍVEL \_ AUTHN) \_ \_
</dt> <dd>

Somente os headers do início de cada chamada são assinados. O restante dos dados trocados entre o cliente e o servidor não está assinado nem criptografado. A maioria dos SSPs não suporta esse nível de autenticação e o promove silenciosamente para o Pacote.

</dd> <dt>

<span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Pacote (RPC \_ C \_ AUTHN \_ LEVEL \_ PKT)
</dt> <dd>

O header de cada pacote é assinado, mas não criptografado. Os pacotes em si não são assinados ou criptografados.

</dd> <dt>

<span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Integridade do pacote (INTEGRIDADE PKT NO NÍVEL de \_ \_ AUTHN \_ \_ RPC \_ C)
</dt> <dd>

Cada pacote de dados é assinado em sua totalidade, mas não é criptografado. Como todos os dados são assinados pelo remetente, o destinatário pode ter certeza de que nenhum dos dados foi adulterado durante o trânsito.

</dd> <dt>

<span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Privacidade do pacote (RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY)
</dt> <dd>

Cada pacote de dados é assinado e criptografado. Isso ajuda a proteger toda a comunicação entre o cliente e o servidor.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Authenticationlevel](authenticationlevel.md)
</dt> <dt>

[LegacyAuthenticationLevel](legacyauthenticationlevel.md)
</dt> </dl>

 

 




