---
description: O material a seguir fornece detalhes sobre as classes base do provedor de serviços de mídia.
ms.assetid: ef845c44-1ff5-42a1-8e91-38d66e6fe363
title: Referência de classes base TAPI 3 MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4cca24b69a645b18cc0950288e0de983b54355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169475"
---
# <a name="tapi-3-msp-base-classes-reference"></a>Referência de classes base TAPI 3 MSP

O material a seguir fornece detalhes sobre as classes base do provedor de serviços de mídia.



| Classes base do provedor de serviços de mídia (ordem alfabética) | Descrição                                                                                                                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CAudioCaptureTerminal](caudiocaptureterminal.md)       | Derivado de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa um terminal de captura de áudio estático para dispositivos Wave usando o filtro Wave do DirectShow. Definido em MSPtmac. h.               |
| [CAudioRenderTerminal](caudiorenderterminal.md)         | Derivado de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa um áudio estático de renderização de vídeo para dispositivos de onda usando o filtro de onda do DirectShow. Definido em MSPtrmar. h.              |
| [CBaseTerminal](cbaseterminal.md)                       | Uma classe base de terminal aplicável a terminais estáticos e dinâmicos. Ele é completamente genérico, portanto, qualquer implementação de terminal pode derivar dessa classe direta ou indiretamente. Definido em MSPterm. h |
| [**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)                       | Implementa o objeto de endereço MSP e dá suporte à interface [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) . Definido em MSPaddr. h.                                                                                |
| [CMSPArray](cmsparray.md)                               | Um modelo que implementa uma matriz inteligente que aumentará sob demanda. Definido em MSPutils. h.                                                                                                               |
| [**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)                     | Fornece uma implementação genérica do objeto de chamada e dá suporte à interface [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) . Definido em MSPcall. h.                                                       |
| [**CMSPCallMultiGraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)         | Define uma chamada que usa um grafo de filtro para cada fluxo. Definido em MSPcall. h.                                                                                                                          |
| [**CMSPStream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)                         | Expõe métodos que permitem a um aplicativo iniciar, pausar ou parar um subfluxo e selecionar ou cancelar a seleção de terminais. Definido em MSPstrm. h.                                                              |
| [CMSPThread](cmspthread.md)                             | Implementa o thread de trabalho do MSP. Definido em MSPthrd. h.                                                                                                                                               |
| [CSingleFilterTerminal](csinglefilterterminal.md)       | Uma classe base de terminal adicional aplicável a terminais estáticos e dinâmicos. Torna a implementação mais específica supondo que o terminal tenha um único filtro do DirectShow. Definido em MSPterm. h.    |
| [CVideoCaptureTerminal](cvideocaptureterminal.md)       | Derivado de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa um terminal de captura de vídeo estático usando um único filtro do DirectShow. Definido em MSPtmvc. h.                                  |



 

 

 
