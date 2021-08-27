---
description: Usando a dizimação para otimizar o desempenho da combinação
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: Usando a dizimação para otimizar o desempenho da combinação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2218566ab31d159f6d0ab74320aa45eb5780bdc3de151de8a7c642016441bacf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049607"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a>Usando a dizimação para otimizar o desempenho da combinação

> [!IMPORTANT]
> A otimização descrita nesta seção é altamente dependente do hardware subjacente. A menos que você possa garantir que tipo de hardware gráfico será usado com o aplicativo, isso poderá prejudicar gravemente a aparência da imagem de vídeo.

 

A HDTV requer muita potência de processamento, que, em sistemas mais novos, é fornecida principalmente pela placa gráfica. Mas mesmo que a placa gráfica e o decodificador possam dar suporte a resoluções de 1920x1080, o usuário nem sempre terá seu monitor definido para essa resolução. Nesse caso, o chip gráfico é necessário para criar uma imagem 1920 x 1080 e, em seguida, reduzir a resolução antes de enviá-la para o buffer de quadros.

Como isso é um desperdício de energia de processamento, a VMR fornece uma maneira de dizimar (reduzir) a imagem no momento em que ela está sendo renderizada na superfície do DirectDraw. Isso eliminará a cópia de memória extra necessária se a imagem precisar ser ressada depois que ela tiver sido renderizada.

**VMR-7:** Para habilitar a dizimação, [**chame IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) com o sinalizador MixerPref \_ DecimateOutput.

**VMR-9:** Para habilitar a dizimação, chame [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) com o sinalizador MixerPref9 \_ DecimateOutput.

O **método SetMixingPrefs** deve ser chamado antes que a VMR seja conectada. Os sinalizadores de preferência de combinação não podem ser alterados depois que o grafo está em execução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o modo de combinação de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



