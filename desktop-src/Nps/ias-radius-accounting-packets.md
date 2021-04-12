---
title: Registrando em log com o servidor de políticas de rede
description: Registrando em log com o servidor de políticas de rede
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5117ce15731ea656913b47525387a48a39aa414c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294294"
---
# <a name="logging-with-network-policy-server"></a>Registrando em log com o servidor de políticas de rede

> [!Note]  
> O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008. O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

 

A tabela a seguir descreve apenas os aspectos mais importantes dos pacotes de contabilização RADIUS. O documento solicitação de comentários de contabilidade RADIUS ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) fornece informações detalhadas sobre esses pacotes.

Os pacotes de contabilização RADIUS podem ser divididos nas categorias a seguir.



| Pacote de contabilidade  | Descrição                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accounting-On      | Enviado pelo NAS (servidor de acesso à rede) para indicar que ele foi reiniciado.<br/> Contém nas-Identifier/IPAddress.<br/>                                                                                        |
| Accounting-Off     | Enviado pelo NAS para indicar que está sendo desligado.<br/> Contém nas-Identifier/IPAddress.<br/>                                                                                                            |
| Accounting-Start   | Enviado pelo NAS, depois que o usuário foi autenticado e autorizado, para indicar o início de uma sessão de usuário. <br/> Contém userid, nas-Identifier/IPAddress, além de outras informações recebidas do NAS.<br/> |
| Accounting-Stop    | Enviado pelo NAS para indicar o fim de uma sessão de usuário.<br/> Contém userid, nas-Identifier/IPAddress, além de outras informações recebidas do NAS.<br/>                                                      |
| Accounting-Interim | Pode ser enviado periodicamente pelo NAS para cada usuário conectado no NAS. <br/> Esse recurso geralmente tem suporte em versões mais recentes do NAS.<br/>                                                     |



 

Os seguintes problemas são importantes para considerar ao coletar informações de contabilidade disponibilizadas por meio do RADIUS:

-   Em casos raros, os pacotes podem ser perdidos durante a transmissão e talvez nunca cheguem ao servidor RADIUS.
-   O servidor RADIUS não será notificado se o NAS abortar.
-   A ISDN dá suporte a várias sessões e cada sessão gera um par de pacotes de início/término de contabilidade. Há um atributo de contabilidade chamado identificador de várias sessões que identifica claramente esses pacotes de várias sessões. Verifique o identificador de várias sessões, além do identificador de sessão, para calcular o número de sessões.

## <a name="requests-logged-by-nps"></a>Solicitações registradas pelo NPS

Por padrão, o NPS não registra nenhum dado. O NPS pode ser configurado, usando a interface do usuário do NPS (NPS. msc), para registrar as solicitações a seguir.



| Pacote registrado          | Descrição                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Solicitação de contabilidade     | Qualquer um dos pacotes de contabilidade descritos na tabela anterior.<br/>                                                                    |
| Solicitação de autenticação | Enviado pelo NAS em nome do usuário que está se conectando.<br/> As entradas de log contêm apenas atributos de entrada.<br/>                    |
| Aceitação de autenticação  | Enviado pelo NPS para indicar que a conexão do usuário deve ser aceita.<br/> As entradas de log contêm apenas atributos de saída.<br/> |
| Rejeição de autenticação  | Enviado pelo NPS para indicar que a conexão do usuário deve ser rejeitada.<br/> As entradas de log contêm apenas atributos de saída.<br/> |



 

Os dados registrados pelo NPS podem ir para um arquivo de texto no servidor NPS ou em um banco de dados SQL central. Para obter mais informações sobre o log SQL do NPS, consulte [programação do SQL](sql-programmability.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviço de autenticação da Internet e servidor de políticas de rede](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Autenticação, autorização e contabilização RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Trabalhando com um servidor de estado](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

