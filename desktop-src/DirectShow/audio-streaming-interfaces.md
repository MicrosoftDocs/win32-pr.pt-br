---
description: Interfaces de streaming de áudio
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Interfaces de streaming de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68210beef0b05fcfc89ae5005c485fbc4b74d40f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500658"
---
# <a name="audio-streaming-interfaces"></a>Interfaces de streaming de áudio

> [!Note]  
> Essas APIs são preteridas. Os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um grafo de filtro do DirectShow.

 



| Interface                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | Controla fluxos de mídia de áudio. Essa interface herda da interface [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) e é usada para criar um ou mais objetos [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) . Ele também é usado para definir e recuperar o formato atual dos dados de fluxo.                                                                                                            |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | Recupera informações dos objetos de dados [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) subjacentes.                                                                                                                                                                                                                                                                                                        |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | Contém métodos que definem e recuperam dados de memória em objetos de dados de áudio. Os objetos de dados de áudio fornecem os dados subjacentes que o fluxo de amostra de acesso. Essa interface fornece uma maneira de inicializar buffers de memória e definir as quantidades reais de dados de áudio nos objetos. Além disso, o método [**IMemoryData:: GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) pode ser usado para recuperar dados de memória de áudio. |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | Fornece métodos que permitem que os aplicativos definam e obtenham os dados de áudio subjacentes aos quais os fluxos de áudio serão referenciados. O formato de dados de áudio é definido na estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lista de interfaces de streaming de multimídia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
