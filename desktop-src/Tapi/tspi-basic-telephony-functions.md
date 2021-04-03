---
description: Todos os provedores de serviço devem implementar funções de telefonia básicas.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Funções de telefonia básicas do TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6276be51482620af32650ad1625eea97bddb8e5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837179"
---
# <a name="tspi-basic-telephony-functions"></a>Funções de telefonia básicas do TSPI

Todos os provedores de serviço devem implementar funções de telefonia básicas. Veja a seguir uma lista dessas funções por categoria. Uma função é identificada como *assíncrona* se ela indicar conclusão em uma mensagem de resposta para o aplicativo. Se a função sempre retornar seu resultado imediatamente, a função será considerada *síncrona*.

-   [Endereços](#addresses)
-   [Respondendo chamadas de entrada](#answering-incoming-calls)
-   [Chamar drop Functions](#call-drop-functions)
-   [Estados de chamada e eventos](#call-states-and-events)
-   [Status da linha e recursos](#line-status-and-capabilities)
-   [Negociação de versão de linha](#line-version-negotiation)
-   [Fazendo chamadas](#making-calls)
-   [Abrindo e fechando dispositivos de linha](#opening-and-closing-line-devices)
-   [Negociação de versão do telefone](#phone-version-negotiation)
-   [Inicialização e desligamento do TSP](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a>Inicialização e desligamento do TSP



|                                                           |                                                           |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [**TUISPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | Instala um TSP. Synchronous.                              |
| [**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | Instala o TSP. Obsoleto com a versão 2,0. Synchronous. |
| [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | Inicializa o TSP. Synchronous.                         |
| [**TSPI \_ providerShutdown**](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | Desliga o provedor de serviços.                          |
| [**TUISPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | Remove um TSP. Synchronous.                               |
| [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | Remove um TSP. Obsoleto com a versão 2,0. Synchronous.    |



 

## <a name="phone-version-negotiation"></a>Negociação de versão do telefone



|                                                                           |                                                                                         |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | Retorna a versão SPI mais alta com a qual o provedor de serviços pode operar para este dispositivo. |



 

## <a name="line-version-negotiation"></a>Negociação de versão de linha



|                                                                         |                                                                                                 |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | Permite que um aplicativo negocie uma versão do TSPI para usar com um determinado dispositivo de linha. Synchronous. |



 

## <a name="line-status-and-capabilities"></a>Status da linha e recursos



|                                                                     |                                                                                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | Retorna os recursos de um determinado dispositivo de linha. Synchronous.                                                                                                  |
| [**TSPI \_ lineGetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | Retorna a configuração de um dispositivo de fluxo de mídia. Synchronous.                                                                                                   |
| [**TSPI \_ lineGetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | Retorna o status atual do dispositivo de linha aberta especificado. Synchronous.                                                                                         |
| [**TSPI \_ lineSetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | Define a configuração do dispositivo de fluxo de mídia especificado. Synchronous.                                                                                      |
| [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | Especifica as alterações de status para as quais o aplicativo precisa ser notificado. Synchronous.                                                                      |
| [**TSPI \_ lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | Recupera uma ID de dispositivo associada à linha aberta, ao endereço ou à chamada especificada. Synchronous.                                                                  |
| [**TSPI \_ lineGetIcon**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | Permite que um aplicativo recupere um ícone para exibição para o usuário. Synchronous.                                                                                |
| [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | Faz com que o provedor do dispositivo de linha especificado exiba uma caixa de diálogo que permite ao usuário configurar parâmetros relacionados ao dispositivo de linha. Synchronous. |
| [**TUISPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | Exibe uma caixa de diálogo que permite ao usuário alterar as informações de configuração de um dispositivo de linha. Synchronous.                                                    |



 

## <a name="addresses"></a>Endereços



|                                                                 |                                                                                          |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | Retorna os recursos de telefonia de um endereço. Synchronous.                           |
| [**TSPI \_ lineGetAddressStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | Retorna o status atual de um endereço especificado. Synchronous.                              |
| [**TSPI \_ lineGetNumAddressIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | Recupera o número de identificadores de endereço com suporte na linha indicada.             |
| [**TSPI \_ lineGetAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | Recupera a ID de endereço de um endereço especificado usando um formato alternativo. Synchronous. |



 

## <a name="opening-and-closing-line-devices"></a>Abrindo e fechando dispositivos de linha



|                                           |                                                                                                            |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | Abre um dispositivo de linha especificado para fornecer monitoramento e/ou controle subsequente da linha. Synchronous. |
| [**TSPI \_ lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | Fecha um dispositivo de linha aberto especificado. Synchronous.                                                        |



 

## <a name="call-states-and-events"></a>Estados de chamada e eventos



|                                                             |                                                                                     |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | Retorna informações fixas sobre uma chamada. Synchronous.                                |
| [**TSPI \_ lineGetCallStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | Retorna informações de status de chamada completas para a chamada especificada. Synchronous.       |
| [**TSPI \_ lineSetAppSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | Define o campo específico do aplicativo da estrutura de informações de uma chamada. Synchronous. |



 

## <a name="making-calls"></a>Fazendo chamadas



|                                                 |                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | Faz uma chamada de saída e retorna um identificador de chamada para ela. Assíncrono. |
| [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | Disca (partes de um ou mais) endereços de discagem. Assíncrono.         |



 

## <a name="answering-incoming-calls"></a>Respondendo chamadas de entrada



|                                             |                                         |
|---------------------------------------------|-----------------------------------------|
| [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | Responde a uma chamada de entrada. Assíncrono. |



 

## <a name="call-drop-functions"></a>Chamar drop Functions



|                                         |                                                                           |
|-----------------------------------------|---------------------------------------------------------------------------|
| [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | Desconecta uma chamada ou abandona uma tentativa de chamada em andamento. Assíncrono. |



 

 

 
