---
description: Processando entrada e saída do codec DMO
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: Processando entrada e saída do codec DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c6781d877f4c863161537fcc5b6a746691cfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296531"
---
# <a name="processing-codec-dmo-input-and-output"></a>Processando entrada e saída do codec DMO

Quando você tiver configurado o tipo de entrada e o tipo de saída para um DMO, poderá começar a processar os exemplos de dados. Você passa amostras para o DMO para processamento usando o método **IMediaObject::P rocessinput** e, em seguida, recupera o exemplo processado chamando **IMediaObject::P rocessoutput**. Você deve definir carimbos e durações de tempo precisos para todos os exemplos de entrada passados. Os carimbos de data/hora não são estritamente necessários, mas ajudam a manter a sincronização de áudio/vídeo. Se você não tiver carimbos de data/hora para suas amostras, é melhor deixá-las fora do que usar valores incertos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 



