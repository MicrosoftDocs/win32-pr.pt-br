---
description: As funções de telefonia básicas são listadas por categoria nas tabelas a seguir.
ms.assetid: 09d10789-bc36-47c7-b77d-8698ae75541a
title: Referência de serviços de telefonia básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1282a406ea6746f1bb3af11d65164d8af0ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789466"
---
# <a name="basic-telephony-services-reference"></a>Referência de serviços de telefonia básicos

As funções de telefonia básicas são listadas por categoria nas tabelas a seguir. Uma função é identificada como [*assíncrona*](a-tapgloss.md) se ela indicar conclusão em uma mensagem de resposta para o aplicativo. Se a função sempre retornar seu resultado ao aplicativo imediatamente, a função será considerada [*síncrona*](s-tapgloss.md).

A seguir está um agrupamento funcional das funções básicas de serviço de telefonia:

-   [Formatos de endereço](#address-formats)
-   [Endereços](#addresses)
-   [Respondendo chamadas de entrada](#answering-incoming-calls)
-   [Chamar drop Functions](#call-drop-functions)
-   [Manipulação de identificador de chamada](#call-handle-manipulation)
-   [Controle de privilégio de chamada](#call-privilege-control)
-   [Estados de chamada e eventos](#call-states-and-events)
-   [Status da linha e recursos](#line-status-and-capabilities)
-   [Negociação de versão de linha](#line-version-negotiation)
-   [Informações de localização e país/região](#location-and-countryregion-information)
-   [Fazendo chamadas](#making-calls)
-   [Abrindo e fechando dispositivos de linha](#opening-and-closing-line-devices)
-   [Solicitar serviços de destinatário](#request-recipient-services)
-   [Inicialização e desligamento TAPI](#tapi-initialization-and-shutdown)
-   [Suporte à proteção de Tarifa](#toll-saver-support)

## <a name="tapi-initialization-and-shutdown"></a>Inicialização e desligamento TAPI



| Função                                     | Descrição                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) | Inicializa a abstração de linha TAPI para uso pelo aplicativo de invocação. Synchronous. |
| [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)         | Desliga o uso do aplicativo da abstração de linha da TAPI. Synchronous.               |



 

## <a name="line-version-negotiation"></a>Negociação de versão de linha



| Função                                                   | Descrição                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) | Permite que um aplicativo negocie uma versão TAPI para usar o. Synchronous. |



 

## <a name="line-status-and-capabilities"></a>Status da linha e recursos



| Função                                               | Descrição                                                                                                                                                    |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)               | Retorna os recursos de um determinado dispositivo de linha. Synchronous.                                                                                                  |
| [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)           | Retorna a configuração de um dispositivo de fluxo de mídia. Synchronous.                                                                                                   |
| [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)   | Retorna o status atual do dispositivo de linha aberta especificado. Synchronous.                                                                                         |
| [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)           | Define a configuração do dispositivo de fluxo de mídia especificado. Synchronous.                                                                                      |
| [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages) | Especifica as alterações de status para as quais o aplicativo precisa ser notificado. Synchronous.                                                                      |
| [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) | Retorna as configurações de mensagem de status da linha atual do aplicativo e do endereço. Synchronous.                                                                       |
| [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)                         | Recupera uma ID de dispositivo associada à linha aberta, ao endereço ou à chamada especificada. Synchronous.                                                                  |
| [**lineGetIcon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon)                     | Permite que um aplicativo recupere um ícone para exibição para o usuário. Synchronous.                                                                                |
| [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)           | Faz com que o provedor do dispositivo de linha especificado exiba uma caixa de diálogo que permite ao usuário configurar parâmetros relacionados ao dispositivo de linha. Synchronous. |
| [**lineConfigDialogEdit**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialogedit)   | Exibe uma caixa de diálogo que permite ao usuário alterar as informações de configuração de um dispositivo de linha. Synchronous.                                                    |



 

## <a name="addresses"></a>Endereços



| Função                                             | Descrição                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)     | Retorna os recursos de telefonia de um endereço. Synchronous.                           |
| [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) | Retorna o status atual de um endereço especificado. Synchronous.                              |
| [**lineGetAddressID**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressid)         | Recupera a ID de endereço de um endereço especificado usando um formato alternativo. Synchronous. |



 

## <a name="opening-and-closing-line-devices"></a>Abrindo e fechando dispositivos de linha



| Função                       | Descrição                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------|
| [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)   | Abre um dispositivo de linha especificado para fornecer monitoramento e/ou controle subsequente da linha. Synchronous. |
| [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) | Fecha um dispositivo de linha aberto especificado. Synchronous.                                                        |



 

## <a name="address-formats"></a>Formatos de endereço



| Função                                                 | Descrição                                                                                       |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)     | Traduz entre um endereço em formato canônico e um endereço no formato de discagem. Synchronous. |
| [**lineSetCurrentLocation**](/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation) | Define o local usado como contexto para a conversão de endereços. Synchronous.                       |
| [**lineSetTollList**](/windows/desktop/api/Tapi/nf-tapi-linesettolllist)               | Manipula a lista de chamadas. Synchronous.                                                           |
| [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)     | Retorna recursos de conversão de endereços. Synchronous.                                            |



 

## <a name="call-states-and-events"></a>Estados de chamada e eventos



| Função                                         | Descrição                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)       | Retorna informações fixas sobre uma chamada. Synchronous.                                |
| [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)   | Retorna informações de status de chamada completas para a chamada especificada. Synchronous.       |
| [**lineSetAppSpecific**](/windows/desktop/api/Tapi/nf-tapi-linesetappspecific) | Define o campo específico do aplicativo da estrutura de informações de uma chamada. Synchronous. |



 

## <a name="making-calls"></a>Fazendo chamadas



| Função                             | Descrição                                                            |
|--------------------------------------|------------------------------------------------------------------------|
| [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) | Faz uma chamada de saída e retorna um identificador de chamada para ela. Assíncrono. |
| [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)         | Disca (partes de um ou mais) endereços de discagem. Assíncrono.         |



 

## <a name="answering-incoming-calls"></a>Respondendo chamadas de entrada



| Função                         | Descrição                             |
|----------------------------------|-----------------------------------------|
| [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) | Responde a uma chamada de entrada. Assíncrono. |



 

## <a name="toll-saver-support"></a>Suporte à proteção de Tarifa



| Função                                   | Descrição                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings) | Indica o número de anéis após o qual as chamadas de entrada devem ser respondidas. Synchronous.                   |
| [**lineGetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linegetnumrings) | Retorna o número mínimo de anéis solicitados com [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings). Synchronous. |



 

## <a name="call-privilege-control"></a>Controle de privilégio de chamada



| Função                                             | Descrição                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege) | Define o privilégio do aplicativo para o privilégio especificado. Synchronous. |



 

## <a name="call-drop-functions"></a>Chamar drop Functions



| Função                                         | Descrição                                                               |
|--------------------------------------------------|---------------------------------------------------------------------------|
| [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)                     | Desconecta uma chamada ou abandona uma tentativa de chamada em andamento. Assíncrono. |
| [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) | Desaloca o identificador de chamada especificado. Synchronous.                       |



 

## <a name="call-handle-manipulation"></a>Manipulação de identificador de chamada



| Função                                                   | Descrição                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)                         | As mãos chamam a propriedade e/ou alteram os privilégios de um aplicativo para uma chamada. Synchronous.                                    |
| [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)                 | Retorna identificadores de chamada para chamadas em uma linha ou endereço especificado para os quais o aplicativo ainda não tem identificadores. Synchronous. |
| [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls) | Retorna uma lista de identificadores de chamada que fazem parte da mesma chamada de conferência que a chamada especificada como um parâmetro. Synchronous.    |



 

## <a name="location-and-countryregion-information"></a>Informações de localização e país/região



| Função                                           | Descrição                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**lineTranslateDialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog) | Exibe uma caixa de diálogo que permite ao usuário alterar o local e as informações do cartão de chamada. Synchronous. |
| [**lineGetCountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)           | Recupera regras de discagem e outras informações sobre um determinado país/região. Synchronous.              |



 

## <a name="request-recipient-services"></a>Solicitar serviços de destinatário

As duas funções a seguir são usadas apenas no suporte à telefonia assistida.



| Função                                                             | Descrição                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient) | Registra ou cancela o registro do aplicativo como um destinatário de solicitação para o modo de solicitação especificado. Synchronous. |
| [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)                             | Obtém a próxima solicitação da biblioteca de vínculo dinâmico de telefonia. Synchronous.                                  |



 

 

 



