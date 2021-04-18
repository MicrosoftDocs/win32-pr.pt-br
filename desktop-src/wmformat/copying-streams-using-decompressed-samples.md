---
title: Copiando fluxos usando amostras descompactadas
description: Copiando fluxos usando amostras descompactadas
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- SDK do Windows Media Format, copiando fluxos
- ASF (Advanced Systems Format), copiando fluxos
- ASF (formato de sistemas avançados), copiando fluxos
- fluxos, copiando usando dados descompactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c5c0f98b02090d98814983ad518ee3cd7e5d8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798389"
---
# <a name="copying-streams-using-decompressed-samples"></a>Copiando fluxos usando amostras descompactadas

É altamente recomendável que você não copie fluxos de um arquivo para outro usando exemplos descompactados. O processo de descompactar e recompactar amostras diminuirá a qualidade da saída. Se você precisar descompactar seus exemplos e, em seguida, copiá-los para outro fluxo, poderá encontrar alguma dificuldade com fluxos codificados de taxa de bits variável (VBR) com base em qualidade.

Quando o codec conclui a compactação de um fluxo de VBR com base na qualidade, ele registra a taxa de bits e a janela de buffer do conteúdo resultante. Quando você lê um arquivo que contém um fluxo codificado com a VBR com base em qualidade, o perfil obtido do leitor notará a taxa de bits e a janela de buffer, bem como a taxa de bits máxima e a janela de buffer máximo. Essa configuração no perfil normalmente significa um fluxo de taxa de bits de variável restrita de taxa de bits. Como resultado, quando você definir o perfil no gravador, ele esperará uma passagem de pré-processamento para o fluxo, pois os fluxos de VBR com taxa de bits restritas exigem codificação de duas passagens. Você deve tratar o fluxo como se fosse um fluxo de VBR de taxa de bits restrita e fornecer os exemplos para pré-processamento. Como você está usando os valores retornados após a codificação do conteúdo em um nível de qualidade específico, esses valores representam o nível de qualidade desejado. É claro que a qualidade da saída recodificada será, de certa forma, degradada, como resultado da nova codificação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Copiando dados de um arquivo para outro**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Copiando fluxos sem descompactar os dados**](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




