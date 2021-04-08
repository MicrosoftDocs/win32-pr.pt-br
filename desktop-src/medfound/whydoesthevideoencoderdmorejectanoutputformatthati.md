---
description: Por que o codificador de vídeo rejeita um formato de saída que tento definir, quando recuperei o formato do mesmo objeto?
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: Por que o codificador de vídeo rejeita um formato de saída que tento definir, quando recuperei o formato do mesmo objeto?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680908ec814fe322585c1ac97d3bb79deddaf034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010797"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a>Por que o codificador de vídeo rejeita um formato de saída que tento definir, quando recuperei o formato do mesmo objeto?

Diferentemente dos tipos de saída do codificador de áudio, as saídas com suporte enumeradas pelos codificadores de vídeo não são concluídas como entregues. Você deve definir a taxa de bits do fluxo no membro **dwBitrate** da estrutura **VIDEOINFOHEADER** para corresponder ao valor definido para a propriedade [MFPKEY \_ RAVG](mfpkey-ravgproperty.md) .

Depois que todas as opções forem definidas da maneira desejada, você deverá recuperar os dados privados do codec e acrescentá-los à estrutura **VIDEOINFOHEADER** . Para obter mais informações, consulte [usando dados privados do codec de vídeo](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Perguntas frequentes](frequentlyaskedquestions.md)
</dt> </dl>

 

 



