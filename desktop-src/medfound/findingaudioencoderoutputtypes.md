---
description: Localizando tipos de saída do codificador de áudio
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: Localizando tipos de saída do codificador de áudio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80dd5aa5204887472e08c6ec5ff375a99b8788924ed0848764cde9ba4b5b97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061567"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a>Localizando tipos de saída do codificador de áudio (Microsoft Media Foundation)

Como você deve usar um formato de saída do codificador de áudio que é enumerado pelo codificador de áudio, você precisa ter uma maneira de encontrar o formato mais adequado às suas necessidades. O número de canais, bits por amostra e a taxa de amostragem da saída que você escolher devem corresponder aos valores do conteúdo compactado. No entanto, o codificador pode dar suporte a vários tipos dentro dessas restrições.

O fator de decisão para escolher um tipo é a taxa de bits do fluxo codificado; você deseja encontrar um tipo de mídia que corresponde à sua entrada e tem uma taxa de bits mais próxima possível de um valor de destino. Se você estiver enumerando tipos de saída de VBR de um passo, será o valor de qualidade que decidirá o tipo usado. Para obter mais informações sobre valores de qualidade em tipos de saída enumerados, consulte [enumerando tipos de áudio para modos de codificação específicos](enumeratingaudiotypesforspecificencodingmodes.md).

> [!Note]  
>    O codificador de áudio enumera alguns tipos que são duplicatas de outros tipos de quase todas as formas. Essas duplicatas existem para formatos em que o número de pacotes por segundo não atende aos requisitos de armazenamento em arquivos ASF quando sincronizado com vídeo. Áudio sincronizado com vídeo em um arquivo ASF deve ter 3 ou mais pacotes por segundo para taxas de bits inferiores a 32000 e 5 ou mais pacotes por segundo para taxas de bits maiores ou iguais a 32000.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando codificação de áudio](configuringaudioencoding.md)
</dt> <dt>

[Enumerando tipos de áudio para modos de codificação específicos](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



