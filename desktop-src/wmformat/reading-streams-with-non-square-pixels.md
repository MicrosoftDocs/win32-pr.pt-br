---
title: Leitura Fluxos com pixels não quadrados
description: Leitura Fluxos com pixels não quadrados
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- Windows SDK de Formato de Mídia, leitura de fluxos de vídeo
- Windows SDK de Formato de Mídia, fluxos de vídeo
- Windows SDK de Formato de Mídia, pixels não quadrados
- Windows SDK de Formato de Mídia, pixels (não quadrado)
- ASF (Advanced Systems Format), lendo fluxos de vídeo
- ASF (Formato de Sistemas Avançados), lendo fluxos de vídeo
- FORMATO DE SISTEMAS Avançados (ASF), fluxos de vídeo
- ASF (Formato de Sistemas Avançados), fluxos de vídeo
- ASF (Advanced Systems Format), pixels não quadrados
- ASF (Formato de Sistemas Avançados), pixels não quadrados
- ASF (Advanced Systems Format), pixels (não quadrado)
- ASF (Formato de Sistemas Avançados), pixels (não quadrado)
- lendo fluxos de vídeo
- fluxos de vídeo, leitura
- fluxos de vídeo, pixels não quadrados
- pixels não quadrados
- pixels (não quadrado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9173c7b5dca81f11a6e35afafe30efa33d86c604adcadb59a51b17ab8130422c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846023"
---
# <a name="reading-streams-with-non-square-pixels"></a>Leitura Fluxos com pixels não quadrados

Os aplicativos de leitor que precisam lidar corretamente com pixels não quadrados devem examinar os atributos de nível de fluxo no header do ASF e as extensões de unidade de dados em cada amostra. Há dois casos em que o retângulo de saída deve ser ajustado para compensar pixels não quadrados.

Quando o conteúdo de origem é capturado de um dispositivo como uma câmera DV (vídeo digital) com pixels não quadrados em seu CCD, um aplicativo de leitor deve ajustar seu retângulo de saída de vídeo para que a imagem seja exibida corretamente em um monitor de computador com pixels quadrados.

Quando o aplicativo de leitor exibe um vídeo que será gravado em uma tv NTSC, por exemplo, por meio de uma conexão S-Video out na placa de vídeo, você deve ajustar o retângulo de vídeo para que a imagem seja exibida corretamente nos pixels não quadrados da tv.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Para ler e gravar vídeos Fluxos com pixels não quadrados**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




