---
description: Na arquitetura TAPI, todos os TSPs são executados no contexto do TAPISRV, que é implementado como um processo de serviço no SVCHOST.
ms.assetid: f47662f9-2fca-4044-ab26-617e5b1f9eae
title: Arquitetura do MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7cf5d95cf568e17b53c575f6c2f8963baa4b698cc69243ee1a23e9306ad6b31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002844"
---
# <a name="msp-architecture"></a>Arquitetura do MSP

Na arquitetura TAPI, todos os TSPs são executados no contexto do TAPISRV, que é implementado como um processo de serviço no SVCHOST. Os aplicativos TAPI estão em seu próprio processo. Os aplicativos TAPI Tapi3.dll e quaisquer MSPs necessários em seu próprio processo, e a DLL tapi se comunica com TAPISRV por meio de uma interface RPC privada. O diagrama a seguir ilustra a interação desses componentes.

![interações entre tapisrv, aplicativos tapi e msps](images/tsp-msp1.png)

Um MSP (provedor de serviços de mídia) fornece streaming de mídia usando as abstrações de Terminais, Fluxos e SubStreams.

Um Terminal é um sink ou fonte para um fluxo de mídia. Pode ser um objeto físico, como um alto-falante ou um microfone, ou pode ser uma abstração de um dispositivo, como uma janela de vídeo. O [Objeto terminal](terminal-object.md) expõe a interface [**ITTerminal.**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) A classe de terminal é descrita pelo GUID [**de Classe do Terminal.**](terminal-class.md) Um MSP pode definir suas próprias classes de terminal.

Fluxos dividir a mídia de uma chamada [](tapimediatype--constants.md) com base no tipo [](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)ou tipo de mídia, na direção do fluxo e no endereço de destino da mídia. Por exemplo, um fluxo de áudio de entrada de um modem é um objeto de fluxo, um fluxo de vídeo de saída para um endereço IP e porta é um objeto de fluxo, os fluxos de vídeo provenientes de um grupo de multicast IP também são considerados como um objeto de fluxo. O objeto Stream é representado pela interface [**ITStreamControl.**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)

SubStreams permitem um controle mais fino sobre a mídia. Por exemplo, no caso de multicast de IP, o objeto de fluxo de vídeo de entrada pode representar várias pessoas. O aplicativo provavelmente vai querer que cada participante tenha um renderdor separado. O fluxo de vídeo de entrada pode ser dividido em vários substreams, um para cada pessoa. Um substream corresponderia a uma pessoa e poderia ser configurado e controlado separadamente. O objeto SubStream é representado pela interface [**ITSubStreamControl.**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol)

Quando um aplicativo chama [**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) para configurar uma chamada, ele deve especificar o tipo de mídia necessária. Em uma chamada de saída, ela simplesmente informa a TAPI quando a chamada é criada. Por exemplo:

``` syntax
HRESULT hr = pAddress->CreateCall( 
       pszDestAddress, 
       lAddressType, 
       TAPIMEDIATYPE_AUDIO | TAPIMEDIATYPE_VIDEO, 
       &pCall 
       ); 
// If (hr != S_OK ) process the error here
```

Nesse caso, o aplicativo está criando uma chamada de áudio-vídeo de saída.

Os tipos de mídia passados indicam a mídia na quais o aplicativo está interessado durante o tempo de vida da chamada. Por exemplo, o aplicativo pode especificar áudio e vídeo ao criar a chamada, mas selecionar apenas terminais de áudio no início. O MSP começará a transmitir somente áudio, mas não rejeitará uma solicitação de vídeo local ou remota feita posteriormente no tempo de vida da chamada.

Quando o aplicativo chama [**ITBasicCallControl::Conexão**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), TAPI 3 chama [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) no TSP. Depois que uma chamada é estabelecida, o MSP e o TSP podem se comunicar conforme necessário.

Quando uma chamada está se desconectando, é decisão do MSP e do TSP comunicar-se sobre como destruir a chamada. Tapi3.dll chamará [**\_ lineDrop do TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) se o aplicativo chamar [**Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
