---
description: Requisitos de codec BRUTOs para o Windows 7
ms.assetid: 3f8bd336-ba03-4ffb-9aa2-ea55a276e3bc
title: Requisitos de codec BRUTOs para o Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0c4d04175eab1b6e68ac87ed18a648fa4655b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759674"
---
# <a name="raw-codec-requirements-for-windows-7"></a>Requisitos de codec BRUTOs para o Windows 7

Os seguintes recursos de codec são necessários no mínimo:

Todas as funcionalidades necessárias para o Shell do Windows Vista e para o suporte da Galeria de fotos: miniatura, visualização e rotação (persistente). O processamento bruto deve padronizar para as configurações do as shot apropriadas.

O suporte para metadados principais (leitura e gravação), metadados não EXIF, bem como metadados de EXIF, deve persistir dentro de formatos de arquivo BRUTOs sem o uso de arquivos sidecar.

Suporte para a interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . Para o Windows 7, o WIC do Windows Imaging Component (WIC) requer que todas as interfaces de parâmetro expostas por [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) sejam implementadas.

Suporte ao estado de orientação:

-   90 as rotações de imagem de etapa de grau devem ser aplicadas usando o método [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) . Aplicativos e Windows Use esse método para girar as imagens (e as miniaturas e visualizações em cache).
-   A aplicação de rotação usando essa API também deve persistir pelo codec (veja anteriormente neste documento).
-   Os aplicativos podem usar os recursos de rotação da API [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , mas o codec não serializará nenhuma configuração de rotação nessa API, portanto, as rotações feitas usando o [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) não serão persistidas.

Suporte à extração de miniatura e visualização de alta velocidade. Se a dimensão de pixel de visualização máxima (largura ou altura) tiver menos de 1024 pixels de tamanho, o Windows Vista solicitará um processamento para visualização de tela:

-   O método [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**setprocessmode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) deve dar suporte a pelo menos os modos [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) e [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) para permitir renderização mais rápida de miniaturas e visualizações do que o modo de qualidade total.
-   O Windows chamará [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) com o tamanho de resolução de tela solicitado.
-   Os tamanhos de resolução de tela devem ter suporte na API acima.
-   É necessário um processamento de imagem consistente de miniatura, visualização e bits de imagem completa do [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) .

Formatos de pixel de intervalo dinâmico alto (HDR).

Impressão de XML Paper Specification (XPS).

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

 

 



