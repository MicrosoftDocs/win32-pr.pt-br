---
title: Lendo fluxos com pixels não quadrados
description: Lendo fluxos com pixels não quadrados
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- SDK do Windows Media Format, lendo fluxos de vídeo
- SDK do Windows Media Format, fluxos de vídeo
- SDK do Windows Media Format, pixels não quadrados
- SDK do Windows Media Format, pixels (não quadrado)
- ASF (Advanced Systems Format), lendo fluxos de vídeo
- ASF (formato de sistemas avançados), lendo fluxos de vídeo
- ASF (Advanced Systems Format), fluxos de vídeo
- ASF (formato de sistemas avançados), fluxos de vídeo
- ASF (Advanced Systems Format), pixels não quadrados
- ASF (formato de sistemas avançados), pixels não quadrados
- ASF (Advanced Systems Format), pixels (não quadrado)
- ASF (formato de sistemas avançados), pixels (não quadrado)
- lendo fluxos de vídeo
- fluxos de vídeo, lendo
- fluxos de vídeo, pixels não quadrados
- pixels não quadrados
- pixels (não quadrado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfc14019e9822aefedb7600adc4209317293b2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813676"
---
# <a name="reading-streams-with-non-square-pixels"></a>Lendo fluxos com pixels não quadrados

Os aplicativos de leitor que precisam lidar corretamente com pixels não quadrados devem examinar os atributos de nível de fluxo no cabeçalho do ASF e as extensões de unidade de dados em cada exemplo. Há dois casos em que o retângulo de saída deve ser ajustado para compensar os pixels não quadrados.

Quando o conteúdo de origem tiver sido capturado de um dispositivo como uma câmera DV (Digital Video) com pixels não quadrados em seu CCD, um aplicativo leitor deverá ajustar seu retângulo de saída de vídeo para que a imagem seja exibida corretamente em um monitor de computador com pixels quadrados.

Quando o aplicativo de leitor gera vídeo que será reproduzido em uma televisão NTSC, por exemplo, por meio de uma conexão de S-Video na placa de vídeo, você deve ajustar o retângulo de vídeo para que a imagem seja exibida corretamente nos pixels não quadrados da televisão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Para ler e gravar fluxos de vídeo com pixels não quadrados**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




