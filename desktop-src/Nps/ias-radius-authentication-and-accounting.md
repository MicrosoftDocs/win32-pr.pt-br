---
title: Autenticação, autorização e contabilização RADIUS
description: O NPS dá suporte total ao protocolo RADIUS (serviço RADIUS). O protocolo RADIUS é o padrão de fato para a autenticação de usuário remota e está documentado em RFC 2865 e RFC 2866.
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b0395b6bc147da4f78bb718cda714014b9b665f5a26a8d20fa29402ee8dec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063477"
---
# <a name="radius-authentication-authorization-and-accounting"></a>Autenticação, autorização e contabilização RADIUS

> [!Note]  
> o IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008. O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

 

O NPS dá suporte total ao protocolo RADIUS (serviço RADIUS). O protocolo RADIUS é o padrão de fato para a autenticação de usuário remota e está documentado em [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) e [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

## <a name="radius-authentication-and-authorization"></a>Autenticação e autorização RADIUS

O diagrama a seguir mostra um cliente de autenticação ("usuário") que se conecta a um NAS (servidor de acesso à rede) por meio de uma conexão dial-up, usando o protocolo PPP (PPP). Para autenticar o usuário, o NAS entra em contato com um servidor remoto que executa o NPS. O NAS e o servidor NPS se comunicam usando o protocolo RADIUS.

![autenticação de usuário remoto](images/ias01.png)

Um NAS Opera como um cliente de um servidor ou servidores que dão suporte ao protocolo RADIUS. Os servidores que oferecem suporte ao protocolo RADIUS são geralmente chamados de servidores RADIUS. O cliente RADIUS, ou seja, o NAS, passa informações sobre o usuário para servidores RADIUS designados e, em seguida, atua na resposta que os servidores retornam. A solicitação enviada pelo NAS para o servidor RADIUS a fim de autenticar o usuário geralmente é chamada de "solicitação de autenticação".

Se um servidor RADIUS autenticar o usuário com êxito, o servidor RADIUS retornará informações de configuração para o NAS para que ele possa fornecer serviço de rede ao usuário. Essas informações de configuração são compostas por "autorizações" e contêm, entre outras, o tipo de serviço que o NAS pode fornecer ao usuário (por exemplo, PPP ou telnet).

Enquanto o servidor RADIUS está processando a solicitação de autenticação, ele pode executar funções de autorização, como verificar o número de telefone do usuário e verificar se o usuário já tem uma sessão em andamento. O servidor RADIUS pode determinar se o usuário já tem uma sessão em andamento contatando um servidor de estado.

Para obter mais informações sobre autenticação e autorização RADIUS, consulte [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).

## <a name="radius-accounting"></a>Contabilização RADIUS

O servidor RADIUS também coleta uma variedade de informações enviadas pelo NAS que podem ser usadas para contabilidade e para relatórios sobre a atividade de rede. O cliente RADIUS envia informações para servidores RADIUS designados quando o usuário faz logon e faz logoff. O cliente RADIUS pode enviar informações de uso adicionais periodicamente enquanto a sessão está em andamento. As solicitações enviadas pelo cliente para o servidor para registrar logon/logoff e informações de uso geralmente são chamadas de "solicitações de contabilização".

Para obter mais informações sobre estatísticas RADIUS, consulte [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

## <a name="radius-proxy"></a>Proxy RADIUS

Um servidor RADIUS pode atuar como um cliente proxy para outros servidores RADIUS. Nesses casos, o servidor RADIUS contatado pelo NAS passa a solicitação de autenticação ou de contabilização para outro servidor RADIUS que realmente realiza a autenticação ou a tarefa de contabilidade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviço de autenticação da Internet e servidor de políticas de rede](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Pacotes de contabilização RADIUS](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Trabalhando com um servidor de estado](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 