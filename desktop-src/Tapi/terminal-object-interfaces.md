---
description: As interfaces de Objeto do Terminal dão a um aplicativo acesso para manipular dispositivos usados para criar ou receber fluxos de mídia.
ms.assetid: 08320d1c-1400-4746-b526-74b0789c5fc0
title: Interfaces de objeto terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f8a80e088e6182416364798a4a8cfa5d3ebeafaa8d9ccb23c53bc56655d39a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118860524"
---
# <a name="terminal-object-interfaces"></a>Interfaces de objeto terminal

As [interfaces de Objeto](terminal-object.md) do Terminal dão a um aplicativo acesso para manipular dispositivos usados para criar ou receber fluxos de mídia.

Essas interfaces são implementadas por um MSP e não estarão disponíveis se o endereço não tiver suporte de um provedor de serviços de mídia. Se existir um MSP associado, a interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) será exposta no [Objeto de Endereço](address-object.md).

As interfaces [**IEnumTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal) e [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) não são expostas diretamente no Objeto terminal, mas estão fortemente relacionadas a ele e são listadas aqui para conveniência de referência.



| Interface                                                                  | Descrição                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                           | Interface base para o objeto terminal. Ele fornece métodos para obter informações como classe de terminal e mídia com suporte. |
| [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                                 | Define e obtém DirectShow de mídia.                                                                                            |
| [**ITBasicAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)                       | Fornece métodos para definir e obter características padrão do terminal de áudio, como volume.                                          |
| [**IEnumTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal)                                     | Enumera [**ITTerminal.**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                                                                      |
| [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass)                           | Enumera a [**classe terminal**](terminal-class.md).                                                                              |
| [**IEnumPluggableSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo)       | Enumera [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo).                                        |
| [**IEnumPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo) | Enumera [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo).                                                  |
| [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack)                                         | Recupera e define informações sobre faixas de terminal de arquivo.                                                                   |
| [**ITASRTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itasrterminalevent)                           | Recupera a descrição dos eventos de terminal de Reconhecimento Automático de Fala.                                                        |
| [**ITFileTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent)                         | Recupera a descrição dos eventos do terminal de arquivo.                                                                                |
| [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal)                       | Enumera, cria ou remove faixas em terminais multitrack.                                                                   |



 



| Interface                                                                                      | Descrição                                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo)                           | Recupera informações sobre um terminal plug-able.                                                                       |
| [**ITPluggableTerminalClassRegistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalclassregistration)           | Cria, modifica ou exclui a entrada do Registro para um terminal que pode ser conectado.                                                   |
| [**ITPluggableTerminalInitialization**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalinitialization)                 | Executa a criação de objeto de terminal primário para terminais que podem ser conectados, permitindo que o Gerenciador do Terminal inicialize o terminal. |
| [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo)                 | Recupera o nome e o CLSID de uma classe de terminal que pode ser plugável.                                                                  |
| [**ITPluggableTerminalSuperclassRegistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalsuperclassregistration) | Recupera e define informações sobre uma superclasse de terminal (nome e CLSID).                                                 |
| [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink)                           | Notifica os aplicativos cliente sobre alterações em um terminal que pode ser conectado.                                                          |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)   | Registra e registra um aplicativo cliente para notificação sobre eventos de terminal que podem ser conectados.                             |



 



| Interface                                            | Descrição                                                        |
|------------------------------------------------------|--------------------------------------------------------------------|
| [**ITTTSTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itttsterminalevent)     | Recupera a descrição de eventos de terminal de TTS (texto em fala). |
| [**ITToneDetectionEvent**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittonedetectionevent) | Recupera informações sobre um evento de detecção de tom.                |
| [**ITToneTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittoneterminalevent)   | Recupera a descrição dos eventos de terminal de tom.                 |



 

 

 
