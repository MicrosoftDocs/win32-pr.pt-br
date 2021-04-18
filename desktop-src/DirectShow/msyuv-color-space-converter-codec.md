---
description: MSYUV é um codec de conversor de espaço de cores YUV a RGB.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: Codec de conversor de espaço de cores MSYUV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838e7cd749042b2fb97adaf0b2b4cd0378a81c07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796263"
---
# <a name="msyuv-color-space-converter-codec"></a>Codec de conversor de espaço de cores MSYUV

MSYUV é um codec de conversor de espaço de cores YUV a RGB. Ele permite a reprodução de dados de origem de vídeo em formatos YUV em clientes cujo adaptador de vídeo não pode ser usado para conversões de YUV para RGB no hardware. O codec participa de gráficos de filtro por meio do filtro de wrapper do [descompactador AVI](avi-decompressor-filter.md) .

Câmeras de conferência digital com interfaces USB ou 1394 podem produzir dados de imagem em vários formatos YUV. Se o hardware de vídeo não oferecer suporte à conversão de YUV para RGB integrada ou se o recurso de conversão de hardware não puder ser usado por algum outro motivo, os dados de imagem YUV deverão ser convertidos para o formato RGB antes de serem enviados para o processador de vídeo.

Devido ao requisito do [processador de vídeo](video-renderer-filter.md)para um tipo de entrada RGB no momento da conexão, esse filtro pode ser inserido em um grafo upstream do processador de vídeo durante a criação automática de grafo. Especificamente, se o construtor de gráficos detectar um formato YUV no tipo de mídia do pino de saída do filtro upstream, o construtor de grafo irá inserir o descompactador AVI, que carregará o codec MSYUV e o configurará inicialmente para executar a conversão em RGB. Depois que o grafo passa pela primeira vez para um estado de execução ou pausado, o filtro de processamento de vídeo pode detectar se o adaptador de vídeo pode executar a conversão em hardware. Se puder, o descompactador AVI será notificado e reconfigurará o MSYUV para operar no "modo de passagem", o que faz com que o codec ignore a conversão e copie os dados de imagem YUV diretamente em uma superfície de sobreposição do DirectDraw na memória de vídeo.

Como os renderizadores de mixagem de vídeo (VMR-7 e VMR-9) nunca usam GDI, eles não exigem um tipo RGB no momento da conexão e o conversor de espaço de cor MSYUV nunca é inserido antes do VMR em um grafo.

MSYUV converte os formatos YUV empacotados em RGB, conforme mostrado na lista a seguir:

-   Formatos de entrada: UYVY, YUY2, YVYU
-   Formatos de saída: RGB 8, RGB 16, RGB 24, RGB 32

O codec do conversor de espaço de cores MSYUV é um codec de VCM (Gerenciador de compactação de vídeo). Ele é usado no DirectShow por meio do filtro de [descompactação AVI](avi-decompressor-filter.md) . Para um conversor de cores de uso mais geral, use o [**DSP do conversor de cores**](../medfound/colorconverter.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msyuv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 
