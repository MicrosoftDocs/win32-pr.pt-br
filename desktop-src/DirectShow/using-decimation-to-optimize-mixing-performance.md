---
description: Usando o Decimation para otimizar o desempenho de mixagem
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: Usando o Decimation para otimizar o desempenho de mixagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e9e4ddfe3bbba3eb5eeab91b7cf0e8b9cbfa03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829059"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a>Usando o Decimation para otimizar o desempenho de mixagem

> [!IMPORTANT]
> A otimização descrita nesta seção é altamente dependente do hardware subjacente. A menos que você possa garantir que tipo de hardware de gráficos será usado com o aplicativo, pode degradar seriamente a aparência da imagem de vídeo.

 

A HDTV requer muita capacidade de processamento, que em sistemas mais novos é fornecida principalmente pela placa gráfica. Mas mesmo se a placa gráfica e o decodificador puderem dar suporte a resoluções de 1920 x 1080, talvez o usuário nem sempre tenha seu monitor definido para essa resolução. Nesse caso, o chip de gráficos é necessário para criar uma imagem 1920 x 1080 e, em seguida, reduzir a resolução antes de enviá-la para o buffer de quadros.

Como esse é um desperdício de poder de processamento, o VMR fornece uma maneira de DECIMATE (reduzir) a imagem no momento em que ela está sendo processada na superfície do DirectDraw. Isso elimina a cópia de memória extra necessária se a imagem tiver que ser redimensionada depois de ser renderizada.

**VMR-7:** Para habilitar Decimation, chame [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) com o \_ sinalizador MixerPref DecimateOutput.

**VMR-9:** Para habilitar Decimation, chame [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) com o \_ sinalizador MixerPref9 DecimateOutput.

O método **SetMixingPrefs** deve ser chamado antes da conexão do VMR. Os sinalizadores de preferência de combinação não podem ser alterados após a execução do grafo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o modo de mixagem do VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



