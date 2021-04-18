---
description: As funções de serviço de telefone suplementar são listadas por categoria nos tópicos a seguir.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: Funções de serviço de telefone suplementar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c39441a924a4f9787d22bf8db596882e7f257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757199"
---
# <a name="supplementary-phone-service-functions"></a>Funções de serviço de telefone suplementar

As funções de serviço de telefone suplementar são listadas por categoria nos tópicos a seguir. Uma função será identificada como [*assíncrona*](a-tapgloss.md) se ela indicar conclusão em uma mensagem de resposta para o aplicativo. Se a função sempre retornar seu resultado ao aplicativo imediatamente, a função será considerada [*síncrona*](s-tapgloss.md).

A seguir está um agrupamento funcional das funções de serviço de telefone suplementar:

-   [Botões](#buttons)
-   [Áreas de dados](#data-areas)
-   [Exibição](#display)
-   [Dispositivos Hookswitch](#hookswitch-devices)
-   [Lâmpadas](#lamps)
-   [Abrindo e fechando dispositivos de telefone](#opening-and-closing-phone-devices)
-   [Inicialização e desligamento do telefone](#phone-initialization-and-shutdown)
-   [Status e recursos do telefone](#phone-status-and-capabilities)
-   [Negociação de versão do telefone](#phone-version-negotiation)
-   [Anel](#ring)
-   [Status](#status)

## <a name="phone-initialization-and-shutdown"></a>Inicialização e desligamento do telefone



| Função                                       | Descrição                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | Inicializa a abstração de telefone TAPI para uso pelo aplicativo de invocação. Synchronous. |
| [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | Desliga o uso de um aplicativo da abstração de telefone da TAPI. Synchronous.            |



 

## <a name="phone-version-negotiation"></a>Negociação de versão do telefone



| Função                                                     | Descrição                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Permite que um aplicativo negocie uma versão TAPI para usar o. Synchronous. |



 

## <a name="opening-and-closing-phone-devices"></a>Abrindo e fechando dispositivos de telefone



| Função                         | Descrição                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | Abre o dispositivo de telefone especificado, concedendo ao aplicativo o proprietário ou o monitor privilégios. Synchronous. |
| [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | Fecha um dispositivo de telefone aberto especificado. Synchronous.                                                        |



 

## <a name="phone-status-and-capabilities"></a>Status e recursos do telefone



| Função                                       | Descrição                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | Retorna os recursos de um determinado dispositivo de telefone. Synchronous.                                                                                                   |
| [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | Retorna uma ID de dispositivo para a classe de dispositivo determinada associada ao dispositivo de telefone especificado. Synchronous.                                                          |
| [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | Permite que um aplicativo recupere um ícone para exibição para o usuário. Synchronous.                                                                                  |
| [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | Faz com que o provedor do dispositivo de telefone especificado exiba uma caixa de diálogo que permite ao usuário configurar parâmetros relacionados ao dispositivo de telefone. Synchronous. |



 

## <a name="hookswitch-devices"></a>Dispositivos Hookswitch



| Função                                         | Descrição                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | Define o estado do gancho de dispositivos Hookswitch de um telefone aberto para um modo especificado. Assíncrono.      |
| [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | Consulta o modo Hookswitch de um dispositivo Hookswitch de um dispositivo de telefone aberto. Synchronous.          |
| [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | Define o volume do alto-falante de um dispositivo Hookswitch de um dispositivo de telefone aberto. Assíncrono.           |
| [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | Retorna a configuração de volume do alto-falante de um dispositivo Hookswitch de um dispositivo de telefone aberto. Synchronous. |
| [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | Define o lucro do MIC de um dispositivo Hookswitch de um dispositivo de telefone aberto. Assíncrono.                 |
| [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | Retorna a configuração de obter do MIC de um dispositivo Hookswitch de um telefone aberto. Synchronous.              |



 

## <a name="display"></a>Monitor



| Função                                   | Descrição                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | Grava informações na exibição de um dispositivo de telefone aberto. Assíncrono. |
| [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | Retorna o conteúdo atual da exibição de um telefone. Synchronous.          |



 

## <a name="ring"></a>Anel



| Função                             | Descrição                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | Toca um dispositivo de telefone aberto de acordo com um determinado modo de toque. Assíncrono. |
| [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | Retorna o modo de toque atual de um dispositivo de telefone aberto. Synchronous.    |



 

## <a name="buttons"></a>Botões



| Função                                         | Descrição                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | Define as informações associadas a um botão em um dispositivo de telefone. Assíncrono. |
| [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | Retorna informações associadas a um botão em um dispositivo de telefone. Synchronous.   |



 

## <a name="lamps"></a>Lâmpadas



| Função                             | Descrição                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | Ilumina uma lâmpada em um dispositivo de telefone aberto especificado em um determinado modo de iluminação. Assíncrono. |
| [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | Retorna o modo de lâmpada atual da lâmpada especificada. Synchronous.                           |



 

## <a name="data-areas"></a>Áreas de dados



| Função                             | Descrição                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | Baixa um buffer de dados para uma determinada área de dados no dispositivo de telefone. Assíncrono.      |
| [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | Carrega o conteúdo de uma determinada área de dados no dispositivo de telefone para um buffer. Synchronous. |



 

## <a name="status"></a>Status



| Função                                                 | Descrição                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | Especifica as alterações de status para as quais o aplicativo deseja ser notificado. Synchronous. |
| [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | Retorna as alterações de status para as quais o aplicativo deseja ser notificado. Synchronous.   |
| [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | Retorna o status completo de um dispositivo de telefone aberto. Synchronous.                         |



 

 

 



