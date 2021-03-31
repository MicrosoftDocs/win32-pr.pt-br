---
title: Serviços de Área de Trabalho Remota funções de API
description: As funções a seguir são usadas com Serviços de Área de Trabalho Remota.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94a2168f5ad4501b9725b72923c98ea97cc707c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641269"
---
# <a name="remote-desktop-services-api-functions"></a>Serviços de Área de Trabalho Remota funções de API

As funções a seguir são usadas com Serviços de Área de Trabalho Remota.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

Recupera a sessão de Serviços de Área de Trabalho Remota associada a um processo especificado.

</dd> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dd>

Abre um identificador para o servidor de licença de Área de Trabalho Remota especificado.

</dd> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> <dd>

Fecha um identificador aberto para um servidor de licença Área de Trabalho Remota.

</dd> <dt>

[**TLSGetServerCertificate**](tlsgetservercertificate.md)
</dt> <dd>

Retorna o certificado do servidor de licença Área de Trabalho Remota.

</dd> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dd>

Inicia a enumeração por meio de todos os pacotes de chaves instalados em um servidor de licença Área de Trabalho Remota com base nos critérios de pesquisa.

</dd> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> <dd>

Continua de uma chamada anterior para a função [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) e encerra a enumeração.

</dd> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dd>

Continua de uma chamada anterior para a função [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) e retorna o próximo pacote de chaves instalado em um servidor de licença área de trabalho remota que corresponde aos critérios de pesquisa.

</dd> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dd>

Inicia a enumeração de licenças emitidas pelo servidor de licença Área de Trabalho Remota com base nos critérios de pesquisa.

</dd> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> <dd>

Continua de uma chamada anterior para a função [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e encerra a enumeração.

</dd> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dd>

Continua de uma chamada anterior para a função [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e retorna a próxima licença instalada em um servidor de licença área de trabalho remota que corresponde aos critérios de pesquisa.

</dd> <dt>

[**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

Fecha a extremidade do cliente de um canal virtual.

</dd> <dt>

[**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

Um ponto de entrada definido pelo aplicativo para a DLL do lado do cliente de um aplicativo que usa Serviços de Área de Trabalho Remota canais virtuais.

</dd> <dt>

[**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

Inicializa o acesso de uma DLL de cliente para Serviços de Área de Trabalho Remota canais virtuais.

</dd> <dt>

[*VirtualChannelInitEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

Uma função de retorno de chamada definida pelo aplicativo que Serviços de Área de Trabalho Remota chamadas para notificar a DLL de cliente dos eventos de canal virtual.

</dd> <dt>

[**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

Abre a extremidade do cliente de um canal virtual.

</dd> <dt>

[*VirtualChannelOpenEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

Uma função de retorno de chamada definida pelo aplicativo que Serviços de Área de Trabalho Remota chamadas para notificar a DLL do cliente de eventos para um canal virtual específico.

</dd> <dt>

[**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

Envia dados da extremidade do cliente de um canal virtual para um aplicativo de parceiro na extremidade do servidor.

</dd> <dt>

[**WTSCloseServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

Fecha um identificador aberto para um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).

</dd> <dt>

[**WTSConnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

Conecta uma sessão de Serviços de Área de Trabalho Remota a uma sessão existente no computador local.

</dd> <dt>

[**WTSCreateListener**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

Cria um novo ouvinte Serviços de Área de Trabalho Remota ou configura um ouvinte existente.

</dd> <dt>

[**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

Desconecta o usuário conectado da sessão de Serviços de Área de Trabalho Remota especificada sem fechar a sessão.

</dd> <dt>

[**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

Habilita ou desabilita [sessões filho](child-sessions.md).

</dd> <dt>

[**WTSEnumerateListeners**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

Enumera todos os ouvintes Serviços de Área de Trabalho Remota em um servidor Host da Sessão RD.

</dd> <dt>

[**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

Recupera informações sobre os processos ativos em um servidor de Host da Sessão RD especificado.

</dd> <dt>

[**WTSEnumerateProcessesEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

Recupera informações sobre os processos ativos no servidor de Host da Sessão RD especificado ou no servidor de Host de Virtualização de Área de Trabalho Remota (host de Virtualização RD).

</dd> <dt>

[**WTSEnumerateServers**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

Retorna uma lista de todos os servidores de Host da Sessão RD dentro do domínio especificado.

</dd> <dt>

[**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

Recupera uma lista de sessões em um servidor Host da Sessão RD.

</dd> <dt>

[**WTSEnumerateSessionsEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

Recupera uma lista de sessões em um servidor de Host da Sessão RD ou servidor host de virtualização de área de trabalho especificado.

</dd> <dt>

[**WTSFreeMemory**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

Libera memória alocada por uma função Serviços de Área de Trabalho Remota.

</dd> <dt>

[**WTSFreeMemoryEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

Libera memória que contém [**informações de \_ processo WTS por \_ \_ exemplo**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) , ou [**WTS informações de \_ sessão \_ \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) , alocadas por uma função serviços de área de trabalho remota.

</dd> <dt>

[**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

Recupera o identificador de sessão da sessão de console.

</dd> <dt>

[**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

Recupera o identificador de sessão filho, se presente.

</dd> <dt>

[**WTSGetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

Recupera o descritor de segurança de um ouvinte de Serviços de Área de Trabalho Remota.

</dd> <dt>

[**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

Determina se as sessões filhas estão habilitadas.

</dd> <dt>

[**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

Faz logoff de uma sessão de Serviços de Área de Trabalho Remota especificada.

</dd> <dt>

[**WTSOpenServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

Abre um identificador para o servidor de Host da Sessão RD especificado.

</dd> <dt>

[**WTSOpenServerEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

Abre um identificador para o servidor de Host da Sessão RD especificado ou para o servidor host de virtualização de área de trabalho remota.

</dd> <dt>

[**WTSQueryListenerConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

Recupera informações de configuração para um ouvinte de Serviços de Área de Trabalho Remota.

</dd> <dt>

[**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

Recupera informações de sessão para a sessão especificada no servidor de Host da Sessão RD especificado.

</dd> <dt>

[**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

Recupera informações de configuração para o usuário especificado no controlador de domínio ou servidor de Host da Sessão RD especificado.

</dd> <dt>

[**WTSQueryUserToken**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

Obtém o token de acesso primário do usuário conectado especificado pela ID de sessão.

</dd> <dt>

[**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

Registra a janela especificada para receber notificações de alteração de sessão.

</dd> <dt>

[**WTSRegisterSessionNotificationEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

Registra a janela especificada para receber notificações de alteração de sessão.

</dd> <dt>

[**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

Exibe uma caixa de mensagem na área de trabalho do cliente de uma sessão de Serviços de Área de Trabalho Remota especificada.

</dd> <dt>

[**WTSSetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

Configura o descritor de segurança de um ouvinte Serviços de Área de Trabalho Remota.

</dd> <dt>

[**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

Modifica as informações de configuração para o usuário especificado no controlador de domínio ou servidor de Host da Sessão RD especificado.

</dd> <dt>

[**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

Desliga (e, opcionalmente, reinicia) o servidor de Host da Sessão RD especificado.

</dd> <dt>

[**WTSStartRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

Inicia o controle remoto de outra sessão de Serviços de Área de Trabalho Remota. Você deve chamar essa função de uma sessão remota.

</dd> <dt>

[**WTSStopRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

Interrompe uma sessão de controle remoto.

</dd> <dt>

[**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

Encerra o processo especificado no servidor de Host da Sessão RD especificado.

</dd> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

Cancela o registro da janela especificada para que ela não receba outras notificações de alteração de sessão.

</dd> <dt>

[**WTSUnRegisterSessionNotificationEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

Cancela o registro da janela especificada para que ela não receba outras notificações de alteração de sessão.

</dd> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Fecha um identificador de canal virtual aberto.

</dd> <dt>

[**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

Abre um identificador para a extremidade do servidor de um canal virtual especificado.

</dd> <dt>

[**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

Cria um canal virtual de maneira semelhante a [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Exclui todos os dados de entrada na fila enviados do cliente para o servidor em um canal virtual especificado.

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Exclui todos os dados de saída na fila enviados do servidor para o cliente em um canal virtual especificado.

</dd> <dt>

[**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Retorna informações sobre um canal virtual especificado.

</dd> <dt>

[**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Lê dados da extremidade do servidor de um canal virtual.

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Grava dados na extremidade do servidor de um canal virtual.

</dd> <dt>

[**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

Aguarda um evento de Serviços de Área de Trabalho Remota antes de retornar ao chamador.

</dd> </dl>

 

 