---
description: Diretrizes gerais para implementação de codecs BRUTOs
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Diretrizes gerais para implementação de codecs BRUTOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f774e5d254330e3274daccb6062f35baa443144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170862"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a>Diretrizes gerais para implementação de codecs BRUTOs

Em comparação com tipos de imagem não-BRUTOs, como JPEG ou TIFF, há duas diferenças notáveis em como espera-se que formatos de imagem BRUTOs se comportem no Windows:

-   É presumido que os formatos de imagem mais BRUTOs sejam "somente leitura" e, provavelmente, não oferecerão suporte à codificação de pixel para o formato bruto. No entanto, como o Windows Imaging Component (WIC) requer um codificador para dar suporte a Write-back de metadados, os autores de codec BRUTOs devem planejar a implementação de pelo menos uma classe de codificador estrutural.
-   A decodificação de uma imagem bruta de tamanho total pode levar muito tempo em comparação com outros formatos. Por esse motivo, a Microsoft recomenda que determinadas abordagens minimizem a latência de decodificação e garantam suporte para cenários como renderização rápida de miniaturas e visualizações.

    Por exemplo, todos os autores de codecs BRUTOs devem implementar a interface [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , que fornece um mecanismo para notificar o decodificador antes do tamanho do bitmap de destino, permitindo, assim, a decodificação otimizada para um tamanho de imagem de saída menor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Diretrizes do WIC para formatos de imagem bruta de câmera](-wic-rawguidelines.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



