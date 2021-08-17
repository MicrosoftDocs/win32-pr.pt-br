---
description: As funções de serviço de telefone suplementares são listadas por categoria nos tópicos a seguir.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: Funções de serviço Telefone suplementares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ee0e32260ac3821fd06e7e8962ab2a6186fb42f1140eb6cd8f705709f2dfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861414"
---
# <a name="supplementary-phone-service-functions"></a>Funções de serviço Telefone suplementares

As funções de serviço de telefone suplementares são listadas por categoria nos tópicos a seguir. Uma função será identificada [*como assíncrona*](a-tapgloss.md) se indicar a conclusão em uma mensagem REPLY para o aplicativo. Se a função sempre retornar seu resultado para o aplicativo imediatamente, a função será considerada [*síncrona.*](s-tapgloss.md)

Veja a seguir um grupo funcional das funções de serviço de telefone suplementares:

-   [Botões](#buttons)
-   [Áreas de dados](#data-areas)
-   [Exibição](#display)
-   [Dispositivos Hookswitch](#hookswitch-devices)
-   [Lâmpadas](#lamps)
-   [Abrindo e fechando dispositivos de telefone](#opening-and-closing-phone-devices)
-   [Telefone inicialização e desligamento](#phone-initialization-and-shutdown)
-   [Telefone status e funcionalidades](#phone-status-and-capabilities)
-   [Telefone de versão](#phone-version-negotiation)
-   [Anel](#ring)
-   [Status](#status)

## <a name="phone-initialization-and-shutdown"></a>Telefone Inicialização e desligamento



| Função                                       | Descrição                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [**Phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | Inicializa a abstração de telefone TAPI para uso pelo aplicativo de invocação. Synchronous. |
| [**Phoneshutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | Desliga o uso de um aplicativo da abstração de telefone da TAPI. Synchronous.            |



 

## <a name="phone-version-negotiation"></a>Telefone Negociação de versão



| Função                                                     | Descrição                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Phonenegotiateapiversion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Permite que um aplicativo negocie uma versão tapi a ser usada. Synchronous. |



 

## <a name="opening-and-closing-phone-devices"></a>Abrindo e fechando Telefone dispositivos



| Função                         | Descrição                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | Abre o dispositivo de telefone especificado, dando ao aplicativo privilégios de proprietário ou monitor. Synchronous. |
| [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | Fecha um dispositivo de telefone aberto especificado. Synchronous.                                                        |



 

## <a name="phone-status-and-capabilities"></a>Telefone Status e funcionalidades



| Função                                       | Descrição                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Phonegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | Retorna os recursos de um determinado dispositivo de telefone. Synchronous.                                                                                                   |
| [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | Retorna uma ID do dispositivo para a classe de dispositivo especificada associada ao dispositivo de telefone especificado. Synchronous.                                                          |
| [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | Permite que um aplicativo recupere um ícone para exibição para o usuário. Synchronous.                                                                                  |
| [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | Faz com que o provedor do dispositivo de telefone especificado exibe uma caixa de diálogo que permite que o usuário configure parâmetros relacionados ao dispositivo de telefone. Synchronous. |



 

## <a name="hookswitch-devices"></a>Dispositivos Hookswitch



| Função                                         | Descrição                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | Define o estado de gancho dos dispositivos hookswitch de um telefone aberto para um modo especificado. Assíncrono.      |
| [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | Consulta o modo hookswitch de um dispositivo hookswitch de um dispositivo de telefone aberto. Synchronous.          |
| [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | Define o volume de um dispositivo hookswitch do alto-falante de um dispositivo de telefone aberto. Assíncrono.           |
| [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | Retorna a configuração de volume de um dispositivo hookswitch do alto-falante de um dispositivo de telefone aberto. Synchronous. |
| [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | Define o ganho de um microfone do dispositivo hookswitch de um dispositivo de telefone aberto. Assíncrono.                 |
| [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | Retorna a configuração de ganho de um microfone do dispositivo hookswitch de um telefone aberto. Synchronous.              |



 

## <a name="display"></a>Exibir



| Função                                   | Descrição                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | Grava informações na exibição de um dispositivo de telefone aberto. Assíncrono. |
| [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | Retorna o conteúdo atual da exibição de um telefone. Synchronous.          |



 

## <a name="ring"></a>Anel



| Função                             | Descrição                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | Anéis de um dispositivo de telefone aberto de acordo com um determinado modo de anel. Assíncrono. |
| [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | Retorna o modo de anel atual de um dispositivo de telefone aberto. Synchronous.    |



 

## <a name="buttons"></a>Botões



| Função                                         | Descrição                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | Define as informações associadas a um botão em um dispositivo de telefone. Assíncrono. |
| [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | Retorna informações associadas a um botão em um dispositivo de telefone. Synchronous.   |



 

## <a name="lamps"></a>Lâmpadas



| Função                             | Descrição                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | Apaga uma lâmpada em um dispositivo de telefone aberto especificado em um determinado modo de iluminação de lâmpada. Assíncrono. |
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



 

 

 



