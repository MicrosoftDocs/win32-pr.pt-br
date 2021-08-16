---
description: Alto Alcance Dinâmico formatos de pixel
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Alto Alcance Dinâmico formatos de pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a544d2331cc32943e3bc74400e1751111aac69e0a1448103e7651cb51da9353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086909"
---
# <a name="high-dynamic-range-pixel-formats"></a>Alto Alcance Dinâmico formatos de pixel

Os codecs devem usar Windows formatos de pixel WIC (Componente de Geração de Imagem) que preservam todo o intervalo dinâmico dos dados do sensor subjacente. GUID \_ WICPixelFormat48bppRGB é um formato típico de ponto fixo de 16 bits por canal que pode ser usado. Outros formatos de precisão mais alta também podem ser usados. Para habilitar o suporte completo para o pipeline de renderização acelerada por GPU (unidade de processamento gráfico) do Windows Presentation Foundation, a Microsoft incentiva fortemente o suporte para um formato de pixel de ponto flutuante de 32 bits.

Formatos de pixel de cor alta: com Windows 7, dois novos formatos de pixel WIC foram adicionados para dar suporte aos novos formatos de exibição de Cor Alta. Estes são: GUID \_ WICPixelFormat32bppRGBA1010102 e GUID \_ WICPixelFormat32bppRGBA1010102XR.

O formato de cor alta float de 16 bits por canal (bpc) é suportado pelo formato de \_ pixel WICPixelFormat64bppRGBAHalf existente.

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

 

 



