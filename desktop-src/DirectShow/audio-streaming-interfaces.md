---
description: Interfaces de Streaming de Áudio
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Interfaces de Streaming de Áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1087ab127258fcd4f587cdd029d4604c35524689b5f0877476e1137e2ed924eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824466"
---
# <a name="audio-streaming-interfaces"></a>Interfaces de Streaming de Áudio

> [!Note]  
> Essas APIs foram preterida. Os aplicativos devem usar [**o filtro Grabber de**](sample-grabber-filter.md) exemplo ou implementar um filtro personalizado para obter dados de um DirectShow de filtro.

 



| Interface                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | Controla fluxos de mídia de áudio. Essa interface herda da interface [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) e é usada para criar um ou mais [**objetos IAudioStreamSample.**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) Ele também é usado para definir e recuperar o formato atual dos dados de fluxo.                                                                                                            |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | Recupera informações dos objetos de dados [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) subjacentes.                                                                                                                                                                                                                                                                                                        |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | Contém métodos que configuram e recuperam dados de memória em objetos de dados de áudio. Os objetos de dados de áudio fornecem os dados subjacentes que transmitem acesso a exemplos. Essa interface fornece uma maneira de inicializar buffers de memória e definir quantidades reais de dados de áudio nos objetos. Além disso, o [**método IMemoryData::GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) pode ser usado para recuperar dados de memória de áudio. |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | Fornece métodos que permitem aos aplicativos definir e obter os dados de áudio subjacentes que serão referenciados por fluxos de áudio. O formato de dados de áudio é definido na [**estrutura WAVEFORMATEX.**](/previous-versions/dd757713(v=vs.85))                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lista de interfaces de streaming multimídia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
