---
description: As funções de serviço de linha suplementares são listadas por categoria nos tópicos a seguir.
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: Funções de serviço de linha suplementares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f2bdd609f092adebd5270a4cc8a3fe35bedce17ad57d8e4e85b5875001255f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476339"
---
# <a name="supplementary-line-service-functions"></a>Funções de serviço de linha suplementares

As funções de serviço de linha suplementares são listadas por categoria nos tópicos a seguir. Uma função será identificada [*como assíncrona*](a-tapgloss.md) se indicar a conclusão em uma mensagem REPLY para o aplicativo. Se a função sempre retornar seu resultado para o aplicativo imediatamente, a função será considerada [*síncrona.*](s-tapgloss.md)

Veja a seguir um grupo funcional das funções de serviço de linha suplementar:

-   [Agentes](#agents)
-   [Prioridade do aplicativo](#application-priority)
-   [Modo de portador e taxa](#bearer-mode-and-rate)
-   [Chamar aceitar e redirecionar](#call-accept-and-redirect)
-   [Conclusão da chamada](#call-completion)
-   [Conferência de chamada](#call-conference)
-   [Encaminhamento de chamadas](#call-forwarding)
-   [Espera de chamada](#call-hold)
-   [Chamar parque](#call-park)
-   [Retirada de chamada](#call-pickup)
-   [Rejeição de chamada](#call-reject)
-   [Transferência de chamada](#call-transfer)
-   [Monitoramento e coleta de dígitos](#digit-monitoring-and-gathering)
-   [Gerando dígitos e tons de banda](#generating-inband-digits-and-tones)
-   [Fazendo chamadas](basic-telephony-services-reference.md)
-   [Controle de mídia](#media-control)
-   [Monitoramento de mídia](#media-monitoring)
-   [Proxies](#proxies)
-   [Qualidade de Serviço](#quality-of-service)
-   [Enviando informações para a parte remota](#sending-information-to-remote-party)
-   [Gerenciamento do provedor de serviços](#service-provider-management)
-   [Configurando um terminal para conversas telefônicas](#setting-a-terminal-for-phone-conversations)
-   [Monitoramento de tom](#tone-monitoring)

Também há diversas [funções de serviço](#miscellaneous) de linha suplementar.

## <a name="bearer-mode-and-rate"></a>Modo de Portador e Taxa



| Função                                       | Descrição                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | Solicita uma alteração nos parâmetros de chamada de uma chamada existente. Synchronous. |



 

## <a name="media-monitoring"></a>Monitoramento de mídia



| Função                                     | Descrição                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**Linemonitormedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | Habilita ou desabilita a notificação de modo de mídia em uma chamada especificada. Synchronous. |



 

## <a name="digit-monitoring-and-gathering"></a>Monitoramento e coleta de dígitos



| Função                                       | Descrição                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | Habilita ou desabilita a notificação de detecção de dígitos em uma chamada especificada. Synchronous. |
| [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | Executa a coleta em buffer de dígitos em uma chamada. Synchronous.                  |



 

## <a name="tone-monitoring"></a>Monitoramento de tom



| Função                                     | Descrição                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | Especifica quais tons detectar em uma chamada especificada. Synchronous. |



 

## <a name="media-control"></a>Controle de mídia



| Função                                           | Descrição                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**lineSetMediaControl**](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | Configura o fluxo de mídia de uma chamada para controle de mídia. Synchronous.                                                        |
| [**lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | Define os modos de mídia da chamada especificada em sua [**estrutura LINECALLINFO.**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) Synchronous. |



 

## <a name="generating-inband-digits-and-tones"></a>Gerando dígitos e tons de inband



| Função                                         | Descrição                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**Linegeneratedigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | Gera dígitos de banda em uma chamada. Synchronous.               |
| [**Linegeneratetone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | Gera um determinado conjunto de tons inband em uma chamada. Synchronous. |



 

## <a name="call-accept-and-redirect"></a>Chamar Aceitar e Redirecionar



| Função                             | Descrição                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | Aceita uma chamada oferecida e começa a alertar o chamador (ringback) e a parte chamada (anel). Assíncrono. |
| [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | Redireciona uma chamada de oferta para outro endereço. Assíncrono.                                              |



 

## <a name="call-reject"></a>Rejeitar chamada



| Função                     | Descrição                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [**Linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) | Desconecta uma chamada ou abandonará uma tentativa de chamada em andamento. Assíncrono. |



 

## <a name="call-hold"></a>Espera de chamada



| Função                         | Descrição                                           |
|----------------------------------|-------------------------------------------------------|
| [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)     | Coloca a chamada especificada em espera. Assíncrono. |
| [**lineUnhold**](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | Recupera uma chamada mantida. Assíncrono.                  |



 

## <a name="securing-calls"></a>Proteger chamadas



| Função                                 | Descrição                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**lineSecureCall**](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | Proteja uma chamada existente contra interferência de outros eventos, como avisos de chamada em conexões de dados. Assíncrono. |



 

## <a name="call-transfer"></a>Transferência de chamada



| Função                                             | Descrição                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**Linesetuptransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | Prepara uma chamada especificada para transferência para outro endereço. Assíncrono.                                       |
| [**Linecompletetransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | Transfere uma chamada que foi configurada para transferência para outra chamada ou entra em uma conferência de três vias. Assíncrono. |
| [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | Transfere uma chamada para outra parte. Assíncrono.                                                               |
| [**Lineswaphold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | Troca a chamada ativa pela chamada atualmente em espera de consulta. Assíncrono.                              |



 

## <a name="call-conference"></a>Conferência de chamada



| Função                                                         | Descrição                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Linesetupconference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | Prepara uma determinada chamada para a adição de outra parte. Assíncrono.                                                                                                                               |
| [**Lineprepareaddtoconference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | Prepara-se para adicionar uma parte a uma chamada de conferência existente colocando a chamada de conferência em um estado de espera e criando uma chamada de consultoria que pode ser adicionada posteriormente à chamada de conferência. Assíncrono. |
| [**Lineaddtoconference**](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | Adiciona uma chamada de consultoria a uma chamada de conferência existente. Assíncrono.                                                                                                                               |
| [**lineRemoveFromConference**](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | Remove uma parte de uma chamada de conferência. Assíncrono.                                                                                                                                                |



 

## <a name="call-park"></a>Chamar Parque



| Função                         | Descrição                                          |
|----------------------------------|------------------------------------------------------|
| [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark)     | Fazer a ressalção de uma determinada chamada em outro endereço. Assíncrono. |
| [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | Recupera uma chamada de ressalvação. Assíncrono.               |



 

## <a name="call-forwarding"></a>Encaminhamento de chamada



| Função                           | Descrição                                             |
|------------------------------------|---------------------------------------------------------|
| [**Lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) | Define ou cancela solicitações de encaminhamento de chamada. Assíncrono. |



 

## <a name="call-pickup"></a>Retirada de chamada



| Função                         | Descrição                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) | Escolhe um alerta de chamada em um endereço de destino especificado e retorna um alça de chamada para a chamada escolhida ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) também pode ser usado para espera de chamada). Assíncrono. |



 

## <a name="sending-information-to-remote-party"></a>Enviando informações para a parte remota



| Função                                                   | Descrição                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**lineReleaseUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | Libera informações de usuário-usuário, permitindo que o sistema sobrescreva esse armazenamento com novas informações. Assíncrono. |
| [**lineSendUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | Envia informações do usuário para a parte remota na chamada especificada. Assíncrono.                                |



 

## <a name="call-completion"></a>Conclusão da chamada



| Função                                         | Descrição                                      |
|--------------------------------------------------|--------------------------------------------------|
| [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | Coloca uma solicitação de conclusão de chamada. Assíncrono.  |
| [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | Cancela uma solicitação de conclusão de chamada. Assíncrono. |



 

## <a name="setting-a-terminal-for-phone-conversations"></a>Definindo um terminal para Telefone conversas



| Função                                   | Descrição                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**Linesetterminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | Especifica o dispositivo terminal para o qual a linha, os eventos de endereço ou os eventos de fluxo de mídia de chamada especificados são roteados. Assíncrono. |



 

## <a name="application-priority"></a>Prioridade do aplicativo



| Função                                         | Descrição                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**lineGetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | Recupera informações de prioridade de telefonia assistida e/ou entrega para um aplicativo. Synchronous. |
| [**lineSetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | Define a prioridade de telefonia assistida e/ou entrega para um aplicativo. Synchronous.              |



 

## <a name="service-provider-management"></a>Gerenciamento do Provedor de Serviços



| Função                                           | Descrição                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [**lineAddProvider**](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | Instala um provedor de serviços de telefonia. Synchronous.                   |
| [**lineConfigProvider**](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | Exibe a caixa de diálogo de configuração de um provedor de serviços. Synchronous. |
| [**lineRemoveProvider**](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | Remove um provedor de serviços de telefonia existente. Synchronous.          |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | Recupera uma lista de provedores de serviços instalados. Synchronous.         |



 

## <a name="agents"></a>Agentes



| Função                                                     | Descrição                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | Permite que o aplicativo acesse funções específicas do manipulador proprietário do manipulador de agente associado ao endereço. Assíncrono. |
| [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | Obtém a lista de atividades das quais um aplicativo seleciona as funções que um agente está executando. Assíncrono.                    |
| [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | Obtém os recursos relacionados ao agente com suporte no dispositivo de linha especificado. Assíncrono.                                            |
| [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | Obtém a lista de grupos de agentes nos quais um agente pode fazer logoff no distribuidor de chamada automática. Assíncrono.                      |
| [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | Obtém o status relacionado ao agente no endereço especificado. Assíncrono.                                                                |
| [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | Define o código de atividade do agente associado a um endereço específico. Assíncrono.                                                        |
| [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | Define os grupos de agentes em que o agente está conectado em um endereço específico. Assíncrono.                                              |
| [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | Define o estado do agente associado a um endereço específico. Assíncrono.                                                                |



 

## <a name="proxies"></a>Proxies



| Função                                       | Descrição                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | Usado por um manipulador de solicitação de proxy registrado para gerar mensagens TAPI. Synchronous.  |
| [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | Indica a conclusão de uma solicitação de proxy por um manipulador de proxy registrado. Synchronous. |



 

## <a name="quality-of-service"></a>Qualidade de Serviço



| Função                                                           | Descrição                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**lineSetCallQualityOfService**](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | Solicita uma alteração da qualidade dos parâmetros de serviço para uma chamada existente. Assíncrono. |



 

## <a name="miscellaneous"></a>Diversos



| Função                                             | Descrição                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**lineSetCallData**](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | Define o **membro CallData** da [**estrutura LINECALLINFO.**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) Assíncrono. |
| [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | Define os sons que o usuário escuta quando uma chamada é sem resposta ou em espera. Assíncrono.               |
| [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | Define o status do dispositivo de linha. Assíncrono.                                                            |



 

 

 



