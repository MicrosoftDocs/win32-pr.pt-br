---
description: processando o Codec DMO entrada e saída
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: processando o Codec DMO entrada e saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e3b159ea9e8a323a8e980b9dbba227aa2a62d76316b90e09f45592044091f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035084"
---
# <a name="processing-codec-dmo-input-and-output"></a>processando o Codec DMO entrada e saída

quando você tiver configurado o tipo de entrada e o tipo de saída para uma DMO, poderá começar a processar os exemplos de dados. você passa amostras para o DMO para processamento usando o método **IMediaObject::P rocessinput** e, em seguida, recupera o exemplo processado chamando **IMediaObject::P rocessoutput**. Você deve definir carimbos e durações de tempo precisos para todos os exemplos de entrada passados. Os carimbos de data/hora não são estritamente necessários, mas ajudam a manter a sincronização de áudio/vídeo. Se você não tiver carimbos de data/hora para suas amostras, é melhor deixá-las fora do que usar valores incertos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 



