---
description: Entrada e saída de MFT do codec de processamento
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Entrada e saída de MFT do codec de processamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cbec9b92ae11d8f1f3722f2cb2540a5b5b01bb5d680e448d298a36ec682ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101835"
---
# <a name="processing-codec-mft-input-and-output"></a>Entrada e saída de MFT do codec de processamento

Quando você tiver configurado o tipo de entrada e o tipo de saída para um MFT, você poderá começar a processar exemplos de dados. Você passa amostras para o MFT para processamento usando o método [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e, em seguida, recupera o exemplo processado chamando [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Você deve definir carimbos e durações de tempo precisos para todos os exemplos de entrada passados. Os carimbos de data/hora não são estritamente necessários, mas ajudam a manter a sincronização de áudio/vídeo. Se você não tiver carimbos de data/hora para suas amostras, é melhor deixá-las fora do que usar valores incertos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



