---
description: Entrada e saída de MFT do codec de processamento
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Entrada e saída de MFT do codec de processamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af3a16fa1855574f1b7618bc0d41bf85c15412f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164894"
---
# <a name="processing-codec-mft-input-and-output"></a>Entrada e saída de MFT do codec de processamento

Quando você tiver configurado o tipo de entrada e o tipo de saída para um MFT, você poderá começar a processar exemplos de dados. Você passa amostras para o MFT para processamento usando o método [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e, em seguida, recupera o exemplo processado chamando [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Você deve definir carimbos e durações de tempo precisos para todos os exemplos de entrada passados. Os carimbos de data/hora não são estritamente necessários, mas ajudam a manter a sincronização de áudio/vídeo. Se você não tiver carimbos de data/hora para suas amostras, é melhor deixá-las fora do que usar valores incertos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



