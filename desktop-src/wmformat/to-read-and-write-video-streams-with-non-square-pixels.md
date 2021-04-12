---
title: Para ler e gravar fluxos de vídeo com pixels não quadrados
description: Para ler e gravar fluxos de vídeo com pixels não quadrados
ms.assetid: fe66d13e-61cf-4bb6-9ca2-aafeabe320ec
keywords:
- SDK do Windows Media Format, lendo fluxos de vídeo
- Windows Media Format SDK, gravando fluxos de vídeo
- SDK do Windows Media Format, fluxos de vídeo
- SDK do Windows Media Format, pixels não quadrados
- SDK do Windows Media Format, pixels (não quadrado)
- ASF (Advanced Systems Format), lendo fluxos de vídeo
- ASF (formato de sistemas avançados), lendo fluxos de vídeo
- ASF (Advanced Systems Format), gravando fluxos de vídeo
- ASF (formato de sistemas avançados), gravando fluxos de vídeo
- ASF (Advanced Systems Format), fluxos de vídeo
- ASF (formato de sistemas avançados), fluxos de vídeo
- ASF (Advanced Systems Format), pixels não quadrados
- ASF (formato de sistemas avançados), pixels não quadrados
- ASF (Advanced Systems Format), pixels (não quadrado)
- ASF (formato de sistemas avançados), pixels (não quadrado)
- lendo fluxos de vídeo
- gravando fluxos de vídeo
- fluxos de vídeo, lendo
- fluxos de vídeo, gravando
- fluxos de vídeo, pixels não quadrados
- pixels não quadrados
- pixels (não quadrado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6b3e3ba67ba42dfc144e7f95ddd042dea0f84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292132"
---
# <a name="to-read-and-write-video-streams-with-non-square-pixels"></a>Para ler e gravar fluxos de vídeo com pixels não quadrados

Os monitores de computador têm pixels quadrados, mas outros tipos de telas de vídeo, incluindo televisões NTSC, têm pixels retangulares ou não quadrados. Além disso, alguns dispositivos de entrada, como câmeras de vídeo digital (DV), têm cobrado dois dispositivos com pixels não quadrados. Quando você está gravando arquivos que são baseados em dados de origem de pixel não quadrado ou que são destinados para exibição em dispositivos com pixels não quadrados, as informações de taxa de proporção de pixel devem ser incluídas no arquivo ASF. Os aplicativos de leitor devem examinar essas informações e usá-las para ajustar a taxa de proporção do retângulo de vídeo conforme necessário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tópicos avançados**](advanced-topics.md)
</dt> <dt>

[**Lendo fluxos com pixels não quadrados**](reading-streams-with-non-square-pixels.md)
</dt> <dt>

[**Gravando fluxos com pixels não quadrados**](writing-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




