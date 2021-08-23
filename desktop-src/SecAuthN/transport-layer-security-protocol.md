---
description: O Schannel dá suporte às versões 1,0, 1,1 e 1,2 do protocolo TLS.
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: Protocolo TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed6bc76b6a491105607c3110cda32723bbba75fdf55abe97f7667f397060209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915588"
---
# <a name="transport-layer-security-protocol"></a>Protocolo TLS

O Schannel dá suporte às versões 1,0, 1,1 e 1,2 do [*protocolo TLS*](../secgloss/t-gly.md). O protocolo TLS é um padrão do setor projetado para ajudar a proteger a privacidade das informações comunicadas pela Internet. O TLS pressupõe que um transporte orientado a conexão, normalmente, TCP, esteja em uso. O protocolo TLS permite que aplicativos cliente/servidor detectem os seguintes riscos de segurança:

-   Violação de mensagem
-   Interceptação de mensagem
-   Falsificação de mensagem

A especificação completa do protocolo TLS está disponível no site da IETF: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) .

## <a name="organization-of-tls"></a>Organização do TLS

As etapas a seguir estão envolvidas no uso de TLS para comunicação de cliente/servidor:

 **Para usar o TLS para comunicação de cliente/servidor**

1.  Negociação de handshake e Cipher Suite
2.  Autenticação de partes
3.  Troca de informações relacionadas à chave
4.  Troca de dados de aplicativos

As etapas que compõem o TLS são divididas em dois protocolos que, juntos, fornecem segurança de conexão:

-   [Protocolo de handshake TLS](tls-handshake-protocol.md)— (etapas 1 a 3)
-   [Protocolo de registro TLS](tls-record-protocol.md)— (etapa 4)

## <a name="sspi-with-tls-implementations"></a>SSPI com implementações de TLS

Como o TLS não tem uma especificação de GSSAPI, os implementadores de TLS podem não estar familiarizados com as funções SSPI. Os aplicativos chamam as funções SSPI para enumerar pacotes disponíveis, criar e trabalhar com identificadores para credenciais, criar contextos de segurança e garantir a privacidade da integridade da mensagem.

Para dar suporte às funções SSPI usadas por aplicativos de modo de usuário, as funções listadas em [funções implementadas por SSP/APS de modo de usuário](/windows/desktop/SecAuthN/authentication-functions) precisam ser suportadas por implementações de TLS, como schannel.dll.

Para obter detalhes sobre as funções SSPI e funções do SSP, consulte [funções de autenticação](authentication-functions.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de codificação TLS](tls-cipher-suites.md)
</dt> <dt>

[TLS vs. SSL](tls-versus-ssl.md)
</dt> </dl>

 

 
