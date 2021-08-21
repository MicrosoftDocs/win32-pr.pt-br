---
description: MSYUV é um codec de conversor de espaço de cor YUV para RGB.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: Codec do Conversor de Espaço em Cores MSYUV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189ff787ee5b28311dd0357c245c7a6ca251d207f2448fc08a88fb856d7c2fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075736"
---
# <a name="msyuv-color-space-converter-codec"></a>Codec do Conversor de Espaço em Cores MSYUV

MSYUV é um codec de conversor de espaço de cor YUV para RGB. Ele permite a reprodução de dados de origem de vídeo em formatos YUV em clientes cujo adaptador de exibição de vídeo não pode ser usado para conversões YUV para RGB em hardware. O codec participa de grafos de filtro por meio do [filtro wrapper do descompactador AVI.](avi-decompressor-filter.md)

Câmeras de conferência digital com interfaces 1394 ou USB podem produzir dados de imagem em vários formatos YUV. Se o hardware de exibição não dá suporte à conversão DE YUV para RGB na placa ou se o recurso de conversão de hardware não puder ser usado por algum outro motivo, os dados da imagem YUV deverão ser convertidos no formato RGB antes de serem enviados para o Renderdor de Vídeo.

Devido ao requisito do [Renderador](video-renderer-filter.md)de Vídeo para um tipo de entrada RGB no momento da conexão, esse filtro pode ser inserido em um upstream de grafo do Renderador de Vídeo durante a criação automática de grafo. Especificamente, se o construtor Graph detectar um formato YUV no tipo de mídia do pin de saída do filtro upstream, o Construtor do Graph inserirá o Descompactador AVI, que carregará o codec MSYUV e o configurará inicialmente para executar a conversão em RGB. Depois que o grafo faz a primeira transição para um estado de execução ou pausado, o filtro do Renderador de Vídeo pode detectar se o adaptador de exibição de vídeo pode executar a conversão em hardware. Se puder, o Descompactador AVI será notificado e reconfigurará o MSYUV para operar no "modo de passagem", o que faz com que o codec ignore a conversão e copie os dados da imagem YUV diretamente para uma superfície de sobreposição do DirectDraw na memória de vídeo.

Como os Renderadores de Combinação de Vídeo (VMR-7 e VMR-9) nunca usam GDI, eles não exigem um tipo RGB no momento da conexão e o Conversor de Espaço de Cor MSYUV nunca é inserido antes da VMR em um grafo.

O MSYUV converte formatos YUV empacotados em RGB, conforme mostrado na lista a seguir:

-   Formatos de entrada: UYVY, YUY2, YVYU
-   Formatos de saída: RGB 8, RGB 16, RGB 24, RGB 32

O Codec do Conversor de Espaço em Cores MSYUV é um codec do VCM (Gerenciador de Compactação de Vídeo). Ele é usado em DirectShow por meio do [filtro de descompactador AVI.](avi-decompressor-filter.md) Para um conversor de cores de uso mais geral, use o [**DSP do Conversor de Cores.**](../medfound/colorconverter.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msyuv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 
