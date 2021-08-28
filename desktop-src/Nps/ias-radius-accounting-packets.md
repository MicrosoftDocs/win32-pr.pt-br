---
title: Registro em log com o servidor de políticas de rede
description: Registro em log com o servidor de políticas de rede
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c6446a6ece75a8da8e51ecab3ed4b6ebf256360e8d9032a676922b83b664d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778066"
---
# <a name="logging-with-network-policy-server"></a>Registro em log com o servidor de políticas de rede

> [!Note]  
> O IAS (Serviço de Autenticação da Internet) foi renomeado como NPS (Servidor de Políticas de Rede) a partir do Windows Server 2008. O conteúdo deste tópico se aplica a IAS e NPS. Em todo o texto, o NPS é usado para se referir a todas as versões do serviço, incluindo as versões originalmente conhecidas como IAS.

 

A tabela a seguir descreve apenas os aspectos mais importantes dos pacotes de contabilidade RADIUS. O documento Solicitação de Contabilidade RADIUS para Comentários ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) fornece informações detalhadas sobre esses pacotes.

Os pacotes de contabilidade RADIUS podem ser divididos nas categorias a seguir.



| Pacote de contabilidade  | Descrição                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accounting-On      | Enviado pelo NAS (Servidor de Acesso à Rede) para indicar que ele foi reiniciado.<br/> Contém nas-identifier/ipaddress.<br/>                                                                                        |
| Accounting-Off     | Enviado pelo NAS para indicar que ele está sendo desligado.<br/> Contém nas-identifier/ipaddress.<br/>                                                                                                            |
| Accounting-Start   | Enviado pelo NAS, depois que o usuário foi autenticado e autorizado, para indicar o início de uma sessão de usuário. <br/> Contém userid, nas-identifier/ipaddress, além de outras informações recebidas do NAS.<br/> |
| Accounting-Stop    | Enviado pelo NAS para indicar o fim de uma sessão de usuário.<br/> Contém userid, nas-identifier/ipaddress, além de outras informações recebidas do NAS.<br/>                                                      |
| Accounting-Interim | Pode ser enviado periodicamente pelo NAS para cada usuário que está conectado no NAS. <br/> Esse recurso geralmente é suportado em versões mais recentes do NAS.<br/>                                                     |



 

Os seguintes problemas são importantes a considerar ao coletar informações de contabilidade disponibilizadas por meio do RADIUS:

-   Em casos raros, os pacotes podem ser perdidos durante a transmissão e nunca podem alcançar o servidor RADIUS.
-   O servidor RADIUS não será notificado se o NAS for anulado.
-   O ISDN dá suporte a várias sessões e cada sessão gera um par de pacotes Accounting-Start/-Stop. Há um atributo de contabilidade chamado identificador de várias sessões que identifica claramente esses pacotes de várias sessões. Verifique o identificador de várias sessões além do identificador de sessão para calcular o número de sessões.

## <a name="requests-logged-by-nps"></a>Solicitações registradas pelo NPS

Por padrão, o NPS não registra nenhum dado. O NPS pode ser configurado usando a interface do usuário NPS (nps.msc) para registrar as solicitações a seguir.



| Pacote registrado          | Descrição                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Solicitação de contabilidade     | Qualquer um dos pacotes de contabilidade descritos na tabela anterior.<br/>                                                                    |
| Solicitação de autenticação | Enviado pelo NAS em nome do usuário que está se conectando.<br/> As entradas de log contêm apenas atributos de entrada.<br/>                    |
| Aceitação de autenticação  | Enviado pelo NPS para indicar que a conexão do usuário deve ser aceita.<br/> As entradas de log contêm apenas atributos de saída.<br/> |
| Rejeição de autenticação  | Enviado pelo NPS para indicar que a conexão do usuário deve ser rejeitada.<br/> As entradas de log contêm apenas atributos de saída.<br/> |



 

Os dados registrados pelo NPS podem ir para um arquivo de texto no servidor NPS ou para um banco de dados SQL central. Para obter mais informações sobre o log SQL NPS, [consulte SQL programação.](sql-programmability.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviço de Autenticação da Internet e Servidor de Política de Rede](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Autenticação RADIUS, autorização e contabilidade](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Trabalhando com um servidor de estado](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

