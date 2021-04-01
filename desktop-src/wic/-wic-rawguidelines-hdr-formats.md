---
description: Formatos de pixel de intervalo dinâmico alto
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Formatos de pixel de intervalo dinâmico alto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8405a01fa5397dd5681077ac1ac9acc28e7d1003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829491"
---
# <a name="high-dynamic-range-pixel-formats"></a>Formatos de pixel de intervalo dinâmico alto

Os codecs devem usar formatos de pixel do Windows Imaging Component (WIC) que preservam todo o intervalo dinâmico dos dados de sensor subjacentes. \_O GUID WICPixelFormat48bppRGB é um formato típico de 16 bits por canal de ponto fixo que pode ser usado. Outros formatos de precisão mais altos também podem ser usados. Para habilitar o suporte completo para o pipeline de renderização acelerado da GPU (unidade de processamento gráfico) do Windows Presentation Foundation, a Microsoft incentiva fortemente o suporte a um formato de pixel flutuante de 32 bits.

Formatos de pixel de alta cor: com o Windows 7, dois novos formatos de pixel WIC foram adicionados para dar suporte aos novos formatos de exibição de alta cor. São eles: GUID \_ WICPixelFormat32bppRGBA1010102 e GUID \_ WICPixelFormat32bppRGBA1010102XR.

O formato de alta cor flutuante de 16 bits por canal (BPC) é suportado pelo \_ formato de pixel WICPIXELFORMAT64BPPRGBAHALF GUID existente.

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

 

 



