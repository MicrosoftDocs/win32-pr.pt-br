---
description: Na arquitetura TAPI, todos os TSPs são executados no contexto de TAPISRV, que é implementado como um processo de serviço no SVCHOST.
ms.assetid: f47662f9-2fca-4044-ab26-617e5b1f9eae
title: Arquitetura MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8c1229ddce90f79c122c47572b4567d230b0b4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370558"
---
# <a name="msp-architecture"></a>Arquitetura MSP

Na arquitetura TAPI, todos os TSPs são executados no contexto de TAPISRV, que é implementado como um processo de serviço no SVCHOST. Os aplicativos TAPI residem em seu próprio processo. Os aplicativos TAPI carregam Tapi3.dll e qualquer MSPs necessária em seu próprio processo, e a DLL TAPI se comunica com o TAPISRV por meio de uma interface RPC privada. O diagrama a seguir ilustra a interação desses componentes.

![interações entre TapiSrv, aplicativos TAPI e MSPs](images/tsp-msp1.png)

Um MSP (provedor de serviços de mídia) fornece streaming de mídia usando as abstrações de terminais, fluxos e subfluxos.

Um terminal é um coletor ou origem para um fluxo de mídia. Pode ser um objeto físico, como um orador ou um microfone, ou pode ser uma abstração de um dispositivo, como uma janela de vídeo. O [objeto terminal](terminal-object.md) expõe a interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) . A classe de terminal é descrita pelo GUID de [**classe de terminal**](terminal-class.md) . Um MSP pode definir suas próprias classes de terminal.

Os fluxos dividem a mídia de uma chamada com base no tipo ou tipo de [**mídia**](tapimediatype--constants.md) , na [**direção**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)do fluxo e no endereço de destino da mídia. Por exemplo, um fluxo de áudio de entrada de um modem é um objeto de fluxo, um fluxo de vídeo de saída para um endereço IP e a porta é um objeto de fluxo, os fluxos de vídeo provenientes de um grupo de multicast IP também são considerados como um objeto de fluxo. O objeto de fluxo é representado pela interface [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) .

Os subfluxos permitem um controle mais preciso sobre a mídia. Por exemplo, no caso de multicast IP, o objeto de fluxo de vídeo de entrada pode representar várias pessoas. O aplicativo provavelmente desejará que cada participante tenha um processador separado. O fluxo de vídeo de entrada pode ser dividido em vários subfluxos, um para cada pessoa. Um subfluxo corresponderia a uma pessoa e pode ser configurado e controlado separadamente. O objeto de substream é representado pela interface [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) .

Quando um aplicativo chama [**ITAddress:: createcall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) para configurar uma chamada, ele deve especificar o tipo de mídia necessário. Em uma chamada de saída, ele simplesmente informa a TAPI quando a chamada é criada. Por exemplo:

``` syntax
HRESULT hr = pAddress->CreateCall( 
       pszDestAddress, 
       lAddressType, 
       TAPIMEDIATYPE_AUDIO | TAPIMEDIATYPE_VIDEO, 
       &pCall 
       ); 
// If (hr != S_OK ) process the error here
```

Nesse caso, o aplicativo está criando uma chamada de vídeo de saída de áudio.

Os tipos de mídia passados indicam a mídia em que o aplicativo está interessado durante o tempo de vida da chamada. Por exemplo, o aplicativo pode especificar áudio e vídeo ao criar a chamada, mas selecionar somente terminais de áudio no início. O MSP começará a transmitir apenas o áudio, mas não rejeitará uma solicitação de vídeo local ou remota feita posteriormente no tempo de vida da chamada.

Quando o aplicativo chama [**ITBasicCallControl:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), a TAPI 3 chama [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) no tsp. Depois que uma chamada é estabelecida, o MSP e o TSP podem se comunicar conforme necessário.

Quando uma chamada está desconectando, cabe ao MSP e ao TSP se comunicarem sobre a subdivisão da chamada. Tapi3.dll chamará [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) se o aplicativo chamar [**Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
