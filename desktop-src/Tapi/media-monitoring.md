---
description: Quando uma chamada está no estado conectado, os dados podem ser transportados pela chamada. O tipo de mídia de chamada fornece uma indicação do tipo de dados (por exemplo, seu DataType ou protocolo de nível superior) desse fluxo de mídia.
ms.assetid: 3281387e-3f72-4fda-8199-b3ce6e45e910
title: Monitoramento de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb54989306fd80c48c0b99c9f8285a83b40bed25
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105789849"
---
# <a name="media-monitoring"></a>Monitoramento de mídia

Quando uma chamada está no estado *conectado* , os dados podem ser transportados pela chamada. O tipo de mídia de chamada fornece uma indicação do tipo de dados (por exemplo, seu DataType ou protocolo de nível superior) desse fluxo de mídia.

A TAPI permite que os aplicativos sejam fornecidos com uma notificação sobre alterações no tipo de mídia de uma chamada. A notificação fornece uma indicação do novo tipo de mídia da chamada. O provedor de serviços decide como ele deseja fazer essa determinação. Por exemplo, o provedor de serviços pode usar o processamento de sinais do fluxo de mídia para determinar o tipo de mídia, ou poderia depender de padrões de toque distintos atribuídos a fluxos de mídia diferentes ou em elementos de informações passados em um protocolo de sinalização fora de banda. Independentemente de como a determinação do tipo de mídia é alcançada, o aplicativo é simplesmente informado sobre alterações de tipo de mídia em uma chamada existente.

Para obter mais informações e uma lista de tipos ou modos de mídia TAPI definidos no momento, consulte [ \_ constantes LINEMEDIAMODE](linemediamode--constants.md). Os provedores de serviço podem implementar tipos de mídia específicos do provedor para dispositivos altamente especializados. As informações sobre elas serão encontradas na documentação do dispositivo.

Os tipos de mídia definidos pela TAPI incluem:

-   Desconhecido. O tipo de mídia da chamada não é conhecido no momento; a chamada não é classificada.
-   Voz interativa. A energia de voz foi detectada na chamada, e a chamada é tratada como uma chamada de voz interativa com uma pessoa no final do aplicativo.
-   Voz automatizada. A energia de voz foi detectada na chamada, e a chamada é tratada como uma chamada de voz, mas sem nenhuma pessoa no fim do aplicativo, como com um aplicativo de secretária eletrônica.
-   Modem de dados. Uma sessão de modem na chamada. Os protocolos de modem atuais exigem que a estação chamada inicie o handshake. Para uma chamada de modem de dados de entrada, o aplicativo normalmente pode não fazer nenhuma detecção positiva. Como o provedor de serviços faz essa determinação é sua escolha. Por exemplo, um período de silêncio logo após responder a uma chamada de entrada pode ser usado como uma heurística para decidir que isso pode ser uma chamada de modem de dados.
-   Fax G3. Uma sessão de fax do grupo 3 na chamada.
-   Fax G4. Uma sessão de fax do grupo 4 na chamada.
-   TDD. O fluxo de mídia da chamada usa os dispositivos de telefonia para o protocolo surdo.
-   Dados digitais. Um fluxo de dados digital de formato não especificado.
-   Teletex, videotex, telex, misto. Elas correspondem aos serviços telemática dos mesmos nomes.
-   Editor. Uma sessão de interface de serviços de vídeo analógico na chamada. A ADSI aprimora chamadas de voz com informações alfanuméricas baixadas para o telefone e o uso de botões suaves no telefone.

Um aplicativo pode habilitar ou desabilitar o monitoramento de mídia em uma chamada especificada com [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia). O aplicativo especifica quais tipos de mídia estão interessados no monitoramento e quando o monitoramento de mídia está habilitado, a detecção de uma alteração de tipo de mídia faz com que o aplicativo seja notificado com a mensagem de [**linha \_ MONITORMEDIA**](line-monitormedia.md) . Essa mensagem fornece o identificador de chamada no qual a alteração do tipo de mídia foi detectada, bem como o novo tipo de mídia.

Há uma distinção entre o tipo de mídia de uma chamada, conforme relatado por [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) e os relatórios de tipo de mídia por mensagens de linha \_ MONITORMEDIA. O tipo de mídia de uma chamada é determinado exclusivamente pelos aplicativos proprietários da chamada e não é alterado automaticamente pelos eventos de monitoramento de mídia. A única exceção é a determinação inicial do tipo de mídia que pode ser executada pela biblioteca de vínculo dinâmico TAPI para selecionar o primeiro proprietário de uma chamada. Você poderia argumentar que, nesse caso, a biblioteca é o proprietário da chamada.

O monitoramento de tipo de mídia padrão é executado para os tipos de mídia para os quais o dispositivo de linha foi aberto. Isso permite que um tipo de mídia de chamada de entrada seja determinado antes que a chamada seja entregue a um aplicativo com base no que o aplicativo exige. O escopo do monitoramento de mídia de uma chamada é associado pelo tempo de vida da chamada. O monitoramento de mídia em uma chamada termina assim que a chamada *se desconecta* ou fica *ociosa*.

Um aplicativo pode obter identificadores de dispositivo para várias classes de dispositivo associadas a uma linha aberta chamando [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid). Essa função usa um identificador de linha, endereço ou identificador de chamada e uma descrição de classe de dispositivo. Ele retorna o identificador de dispositivo para o dispositivo da classe de dispositivo fornecida que está associada ao dispositivo, endereço ou chamada de linha aberta. Se a classe de dispositivo for "TAPI/linha", o identificador de dispositivo do dispositivo de linha será retornado. Se a classe de dispositivo for "MCI/Wave", o identificador de dispositivo de um dispositivo MCI WaveAudio será retornado (se houver suporte), que permite atividades como a gravação ou reprodução de áudio pela chamada na linha.

O aplicativo pode usar o identificador de dispositivo retornado com a API de mídia correspondente para consultar os recursos do dispositivo e, subsequentemente, abrir o dispositivo de mídia. Por exemplo, se seu aplicativo precisar usar a linha como um dispositivo de forma de onda, ele deverá primeiro chamar [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) e/ou [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) para determinar os recursos de forma de onda do dispositivo. O formato de dados típico de forma de onda com suporte de telefonia no América do Norte é a lei m de 8 bits às 8000 amostras por segundo, embora o driver de dispositivo wave possa converter essa taxa de amostra e companding em outros formatos de áudio multimídia mais comuns.

Para abrir um dispositivo de linha subsequentemente para reprodução de áudio usando a API de onda, um aplicativo chama [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen). A implementação de **waveOutOpen** é específica do dispositivo e há uma variedade de opções para implementar essa função.

 

 
