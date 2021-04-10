---
title: Formatos
description: Formatos
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- SDK do Windows Media Format, entradas
- SDK do Windows Media Format, fluxos
- SDK do Windows Media Format, saídas
- Windows Media Format SDK, formatos
- ASF (Advanced Systems Format), entradas
- ASF (formato de sistemas avançados), entradas
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- ASF (Advanced Systems Format), saídas
- ASF (formato de sistemas avançados), saídas
- ASF (Advanced Systems Format), formatos
- ASF (formato de sistemas avançados), formatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e7895c27af3eb99e96d7009b79ea8df0011208
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292561"
---
# <a name="formats"></a>Formatos

As informações em um formato descrevem tudo o que você precisa saber sobre um tipo específico de mídia. Cada formato tem um tipo principal, como áudio ou vídeo, e pode ter um subtipo. Os formatos contêm informações diferentes com base no tipo principal. Os formatos de áudio e vídeo exigem muito mais informações do que outros tipos.

Assim como os objetos do SDK do Windows Media Format diferenciam os números de entrada, os números de fluxo e os números de saída (consulte [entradas, fluxos e saídas](inputs-streams-and-outputs.md)), há distinções importantes entre formatos de entrada, formatos de fluxo e formatos de saída. Essas diferenças são descritas aqui:

## <a name="input-formats"></a>Formatos de entrada

Um formato de entrada descreve a mídia digital que você passa para o objeto gravador. Se um fluxo em um arquivo ASF for compactado com um codec, o codec dará suporte a apenas determinados formatos de entrada. Ao usar os codecs de áudio e vídeo do Windows Media, você pode enumerar os formatos de entrada com suporte usando o objeto Writer. Ao gravar um arquivo, você é responsável por selecionar um formato de entrada que corresponda à mídia de entrada.

Embora o formato de mídia de entrada tenha suporte do codec que compactará os dados, algumas configurações de formato de entrada não precisam corresponder ao formato de fluxo. Por exemplo, o formato de entrada para um fluxo de vídeo pode ter um tamanho de quadro diferente daquele definido no formato de fluxo. O codec executará conversões nesses casos.

## <a name="stream-formats"></a>Formatos de fluxo

Um formato de fluxo descreve a forma da mídia como é armazenada no arquivo ASF. O formato de fluxo é o formato descrito no perfil e pode ou não ser o mesmo que o formato de entrada e o formato de saída. Se um codec for usado para compactar os dados em um fluxo, o formato de fluxo será diferente dos formatos de entrada e saída.

Ao usar os codecs de áudio e vídeo do Windows Media, você deve obter uma lista de formatos de fluxo com suporte do codec para garantir que não esteja tentando especificar um formato ao qual o código não dá suporte. Algumas configurações de formato, como a intensidade de cor e tamanho de um quadro de vídeo, devem ser configuradas manualmente após o formato do codec ser recuperado.

## <a name="output-formats"></a>Formatos de saída

Um formato de saída descreve a mídia digital que o leitor (ou leitor síncrono) entrega para seu aplicativo. Se um fluxo em um arquivo ASF for compactado com um codec, o codec dará suporte apenas a determinados formatos de saída. Ao usar os codecs de áudio e vídeo do Windows Media, você pode enumerar os formatos de saída com suporte usando o objeto leitor. Cada um dos codecs de mídia do Windows tem um formato de saída padrão, mas você pode selecionar qualquer formato de saída com suporte para entrega de exemplo.

Embora o formato de mídia de saída deva ser suportado pelo codec que expactou os dados, algumas configurações de formato de saída não precisam corresponder ao formato de fluxo. Por exemplo, o formato de saída para um fluxo de vídeo pode ter um tamanho de quadro diferente daquele definido no formato de fluxo. O codec executará conversões nesses casos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](concepts.md)
</dt> </dl>

 

 




