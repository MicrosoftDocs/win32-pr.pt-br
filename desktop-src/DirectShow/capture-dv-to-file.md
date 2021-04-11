---
description: Capturar DV para o arquivo
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: Capturar DV para o arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296032"
---
# <a name="capture-dv-to-file"></a>Capturar DV para o arquivo

Esta seção descreve como capturar vídeo digital (DV) de uma câmera DV ou de uma fita VTR.

1.  Crie uma instância do filtro de [Driver MSDV](msdv-driver.md) . Para obter mais informações, consulte [selecionando um dispositivo de captura](selecting-a-capture-device.md).
2.  Inicialize o construtor de gráficos de captura, conforme descrito em [sobre o construtor de grafo de captura](about-the-capture-graph-builder.md).
3.  Compile o grafo de captura, dependendo do tipo de arquivo de destino:
    -   [Capturar um arquivo DV tipo-1](capture-a-type-1-dv-file.md)
    -   [Capturar um arquivo DV tipo-2](capture-a-type-2-dv-file.md)
    -   [Capturar DV para RGB descompactado](capture-dv-to-uncompressed-rgb.md)
4.  Execute o grafo.

A captura de uma fita VTR funciona exatamente como a captura de vídeo ao vivo da câmera, exceto que você deve reproduzir a fita, conforme descrito em [controlando uma camcorder DV](controlling-a-dv-camcorder.md). Para evitar a perda de quadros, execute o grafo primeiro e, em seguida, reproduza a fita. Quando terminar de transmitir, pare a fita primeiro e, em seguida, pare o grafo.

> [!Note]  
> A camcorder deve estar no modo VTR. Consulte [modo de dispositivo](device-mode.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Tipos-1 vs. tipo-2 arquivos AVI de DV](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



