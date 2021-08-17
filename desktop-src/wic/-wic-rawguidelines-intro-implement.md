---
description: Diretrizes gerais para implementar codecs RAW
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Diretrizes gerais para implementar codecs RAW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5081edfc6f49dc1d145fc3e2ce7e5f993fb2e7e250aeb0f1091579dd3f45461
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204624"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a>Diretrizes gerais para implementar codecs RAW

Em comparação com tipos de imagem não RAW, como JPEG ou TIFF, há duas diferenças importantes em como os formatos de imagem RAW devem se comportar Windows:

-   Presume-se que a maioria dos formatos de imagem RAW seja "somente leitura" e provavelmente não dará suporte à codificação de pixel para o formato RAW. No entanto, como Windows WIC (Componente de Imagem) requer um codificador para dar suporte ao write-back de metadados, os autores de codec RAW devem planejar implementar pelo menos uma classe de codificador de esqueleto.
-   A decodificação de uma imagem RAW de tamanho completo pode levar muito tempo em comparação com outros formatos. Por esse motivo, a Microsoft recomenda que determinadas abordagens sejam tomadas para minimizar a latência de decodificação e garantir o suporte para cenários como renderização rápida de miniaturas e visualizações.

    Por exemplo, todos os autores de codec RAW devem implementar a interface [**IWICBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) que fornece um mecanismo para notificar o decodificador antes do tamanho do bitmap de destino, permitindo assim a decodificação otimizada para um tamanho de imagem de saída menor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Diretrizes do WIC para formatos de imagem RAW da câmera](-wic-rawguidelines.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



