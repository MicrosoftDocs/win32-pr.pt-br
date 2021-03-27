---
title: Formatos de estêncil sem suporte com recursos de lado
description: Os formatos que contêm o estêncil não têm suporte com recursos de lado.
ms.assetid: 1B675245-F21F-47B5-B3B4-C8307DAC575B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce07b64e54808a2b4b730f6ed9c5321956f6bf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004797"
---
# <a name="stencil-formats-not-supported-with-tiled-resources"></a>Formatos de estêncil sem suporte com recursos de lado

Os formatos que contêm o estêncil não têm suporte com recursos de lado.

Os formatos que contêm o estêncil incluem o \_ formato dxgi \_ D24 \_ UNORM \_ S8 \_ uint (e os formatos relacionados na família R24G8) e o \_ formato dxgi \_ D32 \_ float \_ S8X24 \_ uint (e os formatos relacionados na família R32G8X24).

Algumas implementações armazenam profundidade e estêncil em alocações separadas enquanto outras os armazenam juntos. O gerenciamento de blocos para os dois esquemas precisaria ser diferente, e nenhuma API única pode abstrair ou racionalizar as diferenças. É recomendável que o hardware futuro tenha suporte a superfícies de profundidade e estêncil independentes, cada uma colocada lado a lado de forma independente. a intensidade de 32 bits teria blocos de 128x128 e o estêncil de 8 bits teria blocos de 256x256. Portanto, os aplicativos precisam conviver com o desalinhamento do formato de bloco entre a profundidade e o estêncil. Mas o mesmo problema já existe com formatos de superfície de destino de renderização diferentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processo cruzado de recursos cruzados e compartilhamento de dispositivos](tiled-resource-cross-process-and-device-sharing.md)
</dt> </dl>

 

 




