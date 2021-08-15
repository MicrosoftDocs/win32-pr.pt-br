---
title: Para ler e gravar vídeos Fluxos com pixels não quadrados
description: Para ler e gravar vídeos Fluxos com pixels não quadrados
ms.assetid: fe66d13e-61cf-4bb6-9ca2-aafeabe320ec
keywords:
- Windows SDK de Formato de Mídia, leitura de fluxos de vídeo
- Windows SDK de Formato de Mídia, escrevendo fluxos de vídeo
- Windows SDK de Formato de Mídia, fluxos de vídeo
- Windows SDK de Formato de Mídia, pixels não quadrados
- Windows SDK de Formato de Mídia, pixels (não quadrado)
- ASF (Advanced Systems Format), lendo fluxos de vídeo
- ASF (Formato de Sistemas Avançados), lendo fluxos de vídeo
- ASF (Advanced Systems Format), escrevendo fluxos de vídeo
- ASF (Formato de Sistemas Avançados), escrevendo fluxos de vídeo
- FORMATO DE SISTEMAS Avançados (ASF), fluxos de vídeo
- ASF (Formato de Sistemas Avançados), fluxos de vídeo
- ASF (Advanced Systems Format), pixels não quadrados
- ASF (Formato de Sistemas Avançados), pixels não quadrados
- ASF (Advanced Systems Format), pixels (não quadrado)
- ASF (Formato de Sistemas Avançados), pixels (não quadrado)
- lendo fluxos de vídeo
- escrevendo fluxos de vídeo
- fluxos de vídeo, leitura
- fluxos de vídeo, gravação
- fluxos de vídeo, pixels não quadrados
- pixels não quadrados
- pixels (não quadrado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdcd5ef5292cc06c78b10916177c48db04547dfcbda4505cfeec93951a054cbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699330"
---
# <a name="to-read-and-write-video-streams-with-non-square-pixels"></a>Para ler e gravar vídeos Fluxos com pixels não quadrados

Os monitores de computador têm pixels quadrados, mas outros tipos de telas de vídeo, incluindo os computadores NTSC, têm pixels retangulares ou não quadrados. Além disso, alguns dispositivos de entrada, como câmeras DV (Vídeo Digital), cobraram alguns dispositivos com pixels não quadrados. Quando você está escrevendo arquivos baseados em dados de origem de pixel não quadrados ou então destinados para exibição em dispositivos com pixels não quadrados, as informações de taxa de proporção de pixel devem ser incluídas no arquivo ASF. Os aplicativos de leitor devem examinar essas informações e usá-los para ajustar a taxa de proporção do retângulo de vídeo, conforme necessário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tópicos avançados**](advanced-topics.md)
</dt> <dt>

[**Lendo Fluxos com pixels não quadrados**](reading-streams-with-non-square-pixels.md)
</dt> <dt>

[**Escrevendo Fluxos com pixels não quadrados**](writing-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




