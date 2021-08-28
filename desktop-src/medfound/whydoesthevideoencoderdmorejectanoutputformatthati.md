---
description: Por que o codificador de vídeo rejeita um formato de saída que tento definir quando recuperei o formato do mesmo objeto?
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: Por que o codificador de vídeo rejeita um formato de saída que tento definir quando recuperei o formato do mesmo objeto?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2e744285140df13a9aa251983ab801033c481d1452029c955ee3a39235fcea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112886"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a>Por que o codificador de vídeo rejeita um formato de saída que tento definir quando recuperei o formato do mesmo objeto?

Ao contrário dos tipos de saída do codificador de áudio, as saídas com suporte enumeradas pelos codificadores de vídeo não são concluídas como entregues. Você deve definir a taxa de bits do fluxo no membro **dwBitrate** da estrutura **VIDEOINFOHEADER** para corresponder ao valor definido para a [propriedade MFPKEY \_ LTDG.](mfpkey-ravgproperty.md)

Depois que todas as opções são definidas da maneira que você deseja, você deve recuperar os dados particulares do codec e aendá-los à estrutura **VIDEOINFOHEADER.** Para obter mais informações, consulte [Using Video Codec Private Data](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Perguntas frequentes](frequentlyaskedquestions.md)
</dt> </dl>

 

 



