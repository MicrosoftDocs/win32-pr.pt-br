---
title: Copiando Fluxos usando exemplos descompactados
description: Copiando Fluxos usando exemplos descompactados
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- Windows SDK de Formato de Mídia, copiando fluxos
- ASF (Advanced Systems Format), copiando fluxos
- ASF (Formato de Sistemas Avançados), copiando fluxos
- fluxos, copiando usando dados descompactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e044d2a1d456c14c2e2d069e0a117ab6f6de218c062771da9c24bf887ddfdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848802"
---
# <a name="copying-streams-using-decompressed-samples"></a>Copiando Fluxos usando exemplos descompactados

É altamente recomendável que você não copie fluxos de um arquivo para outro usando exemplos descompactados. O processo de descompactar e recompactar amostras prejudicará a qualidade da saída. Se você precisar descompactar seus exemplos e, em seguida, copiá-los para outro fluxo, poderá encontrar alguma dificuldade com fluxos codificados em VBR (taxa de bits variável) baseada em qualidade.

Quando o codec termina de compactar um fluxo VBR baseado em qualidade, ele registra a taxa de bits e a janela de buffer do conteúdo resultante. Quando você ler um arquivo que contém um fluxo codificado com VBR baseado em qualidade, o perfil obtido do leitor observará a taxa de bits e a janela de buffer, bem como a taxa de bits máxima e a janela de buffer máxima. Essa configuração no perfil normalmente significa um fluxo de taxa de bits restrita de taxa de bits restrita. Como resultado, quando você definir o perfil no autor, ele esperará uma passagem de pré-processamento para o fluxo, porque fluxos de VBR restritos de taxa de bits exigem codificação de duas passs. Você deve tratar o fluxo como se fosse um fluxo VBR restrito de taxa de bits e entregar os exemplos para pré-processamento. Como você está usando os valores retornados após codificar o conteúdo em um nível de qualidade específico, esses valores representam o nível de qualidade desejado. É claro que a qualidade da saída codificada de novo será um pouco degradada de qualquer forma, como resultado da reencodagem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Copiando dados de um arquivo para outro**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Copiar Fluxos sem descompactar os dados**](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




