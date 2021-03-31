---
description: As interfaces de objeto de terminal fornecem a um aplicativo acesso para manipular dispositivos usados para criar ou receber fluxos de mídia.
ms.assetid: 08320d1c-1400-4746-b526-74b0789c5fc0
title: Interfaces de objeto de terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3286d9a2bf3c247f813d3a1f942b0490de0154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663585"
---
# <a name="terminal-object-interfaces"></a>Interfaces de objeto de terminal

As interfaces de [objeto de terminal](terminal-object.md) fornecem a um aplicativo acesso para manipular dispositivos usados para criar ou receber fluxos de mídia.

Essas interfaces são implementadas por um MSP e não estarão disponíveis se o endereço não tiver suporte de um provedor de serviços de mídia. Se existir um MSP associado, a interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) será exposta no [objeto de endereço](address-object.md).

As interfaces [**IEnumTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal) e [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) não são diretamente expostas no objeto terminal, mas estão intimamente relacionadas a ela e estão listadas aqui para conveniência de referência.



| Interface                                                                  | Descrição                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                           | Interface base para o objeto terminal. Ele fornece métodos para obter informações como a classe de terminal e a mídia com suporte. |
| [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                                 | Define e Obtém o formato de mídia do DirectShow.                                                                                            |
| [**ITBasicAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)                       | Fornece métodos para definir e obter características de terminal de áudio padrão, como volume.                                          |
| [**IEnumTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal)                                     | Enumera [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal).                                                                                      |
| [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass)                           | Enumera a [**classe terminal**](terminal-class.md).                                                                              |
| [**IEnumPluggableSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo)       | Enumera [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo).                                        |
| [**IEnumPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo) | Enumera [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo).                                                  |
| [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack)                                         | Recupera e define informações relativas a faixas de terminal de arquivo.                                                                   |
| [**ITASRTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itasrterminalevent)                           | Recupera a descrição de eventos de terminal de reconhecimento automático de fala.                                                        |
| [**ITFileTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent)                         | Recupera a descrição dos eventos de terminal do arquivo.                                                                                |
| [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal)                       | Enumera, cria ou remove faixas em terminais multitrack.                                                                   |



 



| Interface                                                                                      | Descrição                                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo)                           | Recupera informações relacionadas a um terminal conectável.                                                                       |
| [**ITPluggableTerminalClassRegistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalclassregistration)           | Cria, modifica ou exclui a entrada do registro para um terminal conectável.                                                   |
| [**ITPluggableTerminalInitialization**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalinitialization)                 | Executa a criação de objeto de terminal primário para terminais conectáveis, permitindo que o Gerenciador de terminal inicialize o terminal. |
| [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo)                 | Recupera o nome e o CLSID de uma classe terminal conectável.                                                                  |
| [**ITPluggableTerminalSuperclassRegistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalsuperclassregistration) | Recupera e define informações sobre uma superclasse de terminal (nome e CLSID).                                                 |
| [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink)                           | Notifica os aplicativos cliente sobre as alterações em um terminal conectável.                                                          |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)   | Registra e cancela o registro de um aplicativo cliente para notificação sobre eventos de terminal conectável.                             |



 



| Interface                                            | Descrição                                                        |
|------------------------------------------------------|--------------------------------------------------------------------|
| [**ITTTSTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itttsterminalevent)     | Recupera a descrição de eventos de terminal de conversão de texto em fala (TTS). |
| [**ITToneDetectionEvent**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittonedetectionevent) | Recupera informações sobre um evento de detecção de Tom.                |
| [**ITToneTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittoneterminalevent)   | Recupera a descrição dos eventos de terminal de Tom.                 |



 

 

 
