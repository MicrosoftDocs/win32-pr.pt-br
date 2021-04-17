---
description: As funções de serviço de linha suplementar são listadas por categoria nos tópicos a seguir.
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: Funções de serviço de linha suplementar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a29831369fd6b886d57cfae075b5b8bf7a83b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782899"
---
# <a name="supplementary-line-service-functions"></a>Funções de serviço de linha suplementar

As funções de serviço de linha suplementar são listadas por categoria nos tópicos a seguir. Uma função será identificada como [*assíncrona*](a-tapgloss.md) se ela indicar conclusão em uma mensagem de resposta para o aplicativo. Se a função sempre retornar seu resultado ao aplicativo imediatamente, a função será considerada [*síncrona*](s-tapgloss.md).

A seguir está um agrupamento funcional das funções de serviço de linha suplementar:

-   [Agentes](#agents)
-   [Prioridade do aplicativo](#application-priority)
-   [Modo e taxa de portador](#bearer-mode-and-rate)
-   [Aceitar e redirecionar chamada](#call-accept-and-redirect)
-   [Conclusão da chamada](#call-completion)
-   [Conferência de chamada](#call-conference)
-   [Encaminhamento de chamadas](#call-forwarding)
-   [Espera de chamada](#call-hold)
-   [Entre em contato com o parque](#call-park)
-   [Chamar retirada](#call-pickup)
-   [Rejeitar chamada](#call-reject)
-   [Transferência de chamada](#call-transfer)
-   [Monitoramento e coleta de dígitos](#digit-monitoring-and-gathering)
-   [Gerando dígitos de banda e tons](#generating-inband-digits-and-tones)
-   [Fazendo chamadas](basic-telephony-services-reference.md)
-   [Controle de mídia](#media-control)
-   [Monitoramento de mídia](#media-monitoring)
-   [Proxies](#proxies)
-   [Qualidade de Serviço](#quality-of-service)
-   [Enviando informações para a parte remota](#sending-information-to-remote-party)
-   [Gerenciamento do provedor de serviços](#service-provider-management)
-   [Configurando um terminal para conversas por telefone](#setting-a-terminal-for-phone-conversations)
-   [Monitoramento de Tom](#tone-monitoring)

Há também funções de serviço de linha suplementar [diversas](#miscellaneous) .

## <a name="bearer-mode-and-rate"></a>Modo e taxa de portador



| Função                                       | Descrição                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | Solicita uma alteração nos parâmetros de chamada de uma chamada existente. Synchronous. |



 

## <a name="media-monitoring"></a>Monitoramento de mídia



| Função                                     | Descrição                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | Habilita ou desabilita a notificação do modo de mídia em uma chamada especificada. Synchronous. |



 

## <a name="digit-monitoring-and-gathering"></a>Monitoramento e coleta de dígitos



| Função                                       | Descrição                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | Habilita ou desabilita a notificação de detecção de dígitos em uma chamada especificada. Synchronous. |
| [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | Executa a coleta de dígitos em buffer em uma chamada. Synchronous.                  |



 

## <a name="tone-monitoring"></a>Monitoramento de Tom



| Função                                     | Descrição                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | Especifica quais tons detectar em uma chamada especificada. Synchronous. |



 

## <a name="media-control"></a>Controle de mídia



| Função                                           | Descrição                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**lineSetMediaControl**](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | Configura o fluxo de mídia de uma chamada para o controle de mídia. Synchronous.                                                        |
| [**lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | Define os modos de mídia da chamada especificada em sua estrutura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) . Synchronous. |



 

## <a name="generating-inband-digits-and-tones"></a>Gerando dígitos de banda e tons



| Função                                         | Descrição                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | Gera dígitos de inband em uma chamada. Synchronous.               |
| [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | Gera um determinado conjunto de tons de faixas em uma chamada. Synchronous. |



 

## <a name="call-accept-and-redirect"></a>Aceitar e redirecionar chamada



| Função                             | Descrição                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | Aceita uma chamada oferecida e começa a emitir um alerta tanto para o chamador (em um toque) quanto para a parte chamada (anel). Assíncrono. |
| [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | Redireciona uma chamada de oferta para outro endereço. Assíncrono.                                              |



 

## <a name="call-reject"></a>Rejeitar chamada



| Função                     | Descrição                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) | Desconecta uma chamada ou abandona uma tentativa de chamada em andamento. Assíncrono. |



 

## <a name="call-hold"></a>Espera de chamada



| Função                         | Descrição                                           |
|----------------------------------|-------------------------------------------------------|
| [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)     | Coloca a chamada especificada em retenção rígida. Assíncrono. |
| [**lineUnhold**](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | Recupera uma chamada mantida. Assíncrono.                  |



 

## <a name="securing-calls"></a>Protegendo chamadas



| Função                                 | Descrição                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**lineSecureCall**](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | Protege uma chamada existente da interferência por outros eventos, como alarmes de espera de chamada em conexões de dados. Assíncrono. |



 

## <a name="call-transfer"></a>Transferência de chamada



| Função                                             | Descrição                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | Prepara uma chamada especificada para transferência para outro endereço. Assíncrono.                                       |
| [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | Transfere uma chamada que foi configurada para transferência para outra chamada ou que entra em uma conferência de três vias. Assíncrono. |
| [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | Transfere uma chamada para outra entidade. Assíncrono.                                                               |
| [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | Troca a chamada ativa pela chamada atualmente em retenção de consulta. Assíncrono.                              |



 

## <a name="call-conference"></a>Conferência de chamada



| Função                                                         | Descrição                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | Prepara uma determinada chamada para a adição de outra parte. Assíncrono.                                                                                                                               |
| [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | Prepara para adicionar uma entidade a uma chamada de conferência existente colocando a chamada de conferência em estado de espera e criando uma chamada de consulta que pode ser adicionada posteriormente à chamada de conferência. Assíncrono. |
| [**lineAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | Adiciona uma chamada de consulta a uma chamada de conferência existente. Assíncrono.                                                                                                                               |
| [**lineRemoveFromConference**](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | Remove uma entidade de uma chamada de conferência. Assíncrono.                                                                                                                                                |



 

## <a name="call-park"></a>Entre em contato com o parque



| Função                         | Descrição                                          |
|----------------------------------|------------------------------------------------------|
| [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark)     | Parques de uma determinada chamada em outro endereço. Assíncrono. |
| [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | Recupera uma chamada estacionada. Assíncrono.               |



 

## <a name="call-forwarding"></a>Encaminhamento de chamadas



| Função                           | Descrição                                             |
|------------------------------------|---------------------------------------------------------|
| [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) | Define ou cancela solicitações de encaminhamento de chamada. Assíncrono. |



 

## <a name="call-pickup"></a>Chamar retirada



| Função                         | Descrição                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) | Pega um alerta de chamada em um endereço de destino especificado e retorna um identificador de chamada para a chamada de retirada ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) também pode ser usado para espera de chamada). Assíncrono. |



 

## <a name="sending-information-to-remote-party"></a>Enviando informações para a parte remota



| Função                                                   | Descrição                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**lineReleaseUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | Libera informações do usuário usuário, permitindo que o sistema Substitua esse armazenamento por novas informações. Assíncrono. |
| [**lineSendUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | Envia informações do usuário ao usuário para a parte remota na chamada especificada. Assíncrono.                                |



 

## <a name="call-completion"></a>Conclusão da chamada



| Função                                         | Descrição                                      |
|--------------------------------------------------|--------------------------------------------------|
| [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | Coloca uma solicitação de conclusão de chamada. Assíncrono.  |
| [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | Cancela uma solicitação de conclusão de chamada. Assíncrono. |



 

## <a name="setting-a-terminal-for-phone-conversations"></a>Configurando um terminal para conversas por telefone



| Função                                   | Descrição                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | Especifica o dispositivo de terminal para o qual a linha especificada, os eventos de endereço ou os eventos de fluxo de mídia de chamada são roteados. Assíncrono. |



 

## <a name="application-priority"></a>Prioridade do aplicativo



| Função                                         | Descrição                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**lineGetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | Recupera informações de prioridade de telefonia assistida e/ou de entrega para um aplicativo. Synchronous. |
| [**lineSetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | Define a prioridade de telefonia de entrega e/ou assistida para um aplicativo. Synchronous.              |



 

## <a name="service-provider-management"></a>Gerenciamento do provedor de serviços



| Função                                           | Descrição                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [**lineAddProvider**](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | Instala um provedor de serviços de telefonia. Synchronous.                   |
| [**lineConfigProvider**](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | Exibe a caixa de diálogo de configuração de um provedor de serviços. Synchronous. |
| [**lineRemoveProvider**](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | Remove um provedor de serviços de telefonia existente. Synchronous.          |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | Recupera uma lista de provedores de serviços instalados. Synchronous.         |



 

## <a name="agents"></a>Agentes



| Função                                                     | Descrição                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | Permite que o aplicativo acesse funções específicas do manipulador proprietário do manipulador do agente associado ao endereço. Assíncrono. |
| [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | Obtém a lista de atividades da qual um aplicativo seleciona as funções que um agente está executando. Assíncrono.                    |
| [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | Obtém os recursos relacionados ao agente com suporte no dispositivo de linha especificado. Assíncrono.                                            |
| [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | Obtém a lista de grupos de agentes nos quais um agente pode fazer logon no distribuidor de chamada automática. Assíncrono.                      |
| [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | Obtém o status relacionado ao agente no endereço especificado. Assíncrono.                                                                |
| [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | Define o código de atividade do agente associado a um endereço específico. Assíncrono.                                                        |
| [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | Define os grupos de agentes nos quais o agente está conectado em um endereço específico. Assíncrono.                                              |
| [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | Define o estado do agente associado a um endereço específico. Assíncrono.                                                                |



 

## <a name="proxies"></a>Proxies



| Função                                       | Descrição                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | Usado por um manipulador de solicitação proxy registrado para gerar mensagens TAPI. Synchronous.  |
| [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | Indica a conclusão de uma solicitação de proxy por um manipulador de proxy registrado. Synchronous. |



 

## <a name="quality-of-service"></a>Qualidade de Serviço



| Função                                                           | Descrição                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**lineSetCallQualityOfService**](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | Solicita uma alteração da qualidade dos parâmetros de serviço para uma chamada existente. Assíncrono. |



 

## <a name="miscellaneous"></a>Diversos



| Função                                             | Descrição                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**lineSetCallData**](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | Define o membro **calldata** da estrutura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) . Assíncrono. |
| [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | Define os sons que o usuário ouve quando uma chamada não é respondida ou está em espera. Assíncrono.               |
| [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | Define o status do dispositivo de linha. Assíncrono.                                                            |



 

 

 



