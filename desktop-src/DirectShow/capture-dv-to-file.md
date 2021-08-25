---
description: Capturar DV no arquivo
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: Capturar DV no arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d886b964502d705f5902c17de8e6e008a11a31699de40b3089033867873fa021
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814336"
---
# <a name="capture-dv-to-file"></a>Capturar DV no arquivo

Esta seção descreve como capturar um DV (vídeo digital) de uma câmera DV ou de uma fita VTR.

1.  Crie uma instância do filtro [driver MSDV.](msdv-driver.md) Para obter mais informações, consulte [Selecionando um dispositivo de captura](selecting-a-capture-device.md).
2.  Inicialize o Construtor Graph De captura, conforme descrito em [Sobre o Construtor Graph Capture.](about-the-capture-graph-builder.md)
3.  Crie o grafo de captura, dependendo do tipo de arquivo de destino:
    -   [Capturar um arquivo DV tipo 1](capture-a-type-1-dv-file.md)
    -   [Capturar um arquivo DV type-2](capture-a-type-2-dv-file.md)
    -   [Capturar DV para RGB descompactado](capture-dv-to-uncompressed-rgb.md)
4.  Execute o grafo.

A captura de uma fita VTR funciona da mesma forma que a captura de vídeo ao vivo da câmera, exceto pelo fato de que você deve reproduzir a fita, conforme descrito em Controlando [uma gravação dv.](controlling-a-dv-camcorder.md) Para evitar a perda de quadros, execute o grafo primeiro e, em seguida, reproduza a fita. Quando terminar de transmitir, pare a fita primeiro e, em seguida, pare o grafo.

> [!Note]  
> A câmera deve estar no modo VTR. Consulte [Modo de Dispositivo](device-mode.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Arquivos TYPE-1 vs. Type-2 DV AVI](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



