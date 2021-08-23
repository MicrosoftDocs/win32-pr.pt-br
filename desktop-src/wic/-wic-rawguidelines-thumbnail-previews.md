---
description: Miniaturas e visualizações
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Miniaturas e visualizações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 110b0f4da08eaf2b17582dabec1ff7bd6d4f3ab4389c6bcf7654cdb5ca3198a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086879"
---
# <a name="thumbnails-and-previews"></a>Miniaturas e visualizações

Windows o Vista e a galeria de fotos Windows contam com o WIC (Windows Imaging Component) para renderizar miniaturas e visualizações rápidas de imagens. Para dar suporte à renderização rápida de miniatura e visualização, os codecs BRUTOs devem implementar as interfaces WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) e [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) . Para dar suporte a uma experiência de usuário responsiva, é altamente desejável que essas interfaces retornem um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) para o chamador em 200 milissegundos ou menos.

A Microsoft recomenda enfaticamente que os proprietários de formato de arquivo bruto gerem uma visualização renderizada e armazenem em cache o arquivo de imagem. Para um formato no dispositivo, isso geralmente é feito no momento da captura. No entanto, as visualizações também podem ser geradas novamente e armazenadas no arquivo de imagem sempre que as propriedades da interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) forem alteradas – se não for necessário muito trabalho para fazer isso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Windows Visão geral do componente de geração de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Diretrizes do WIC para formatos de imagem bruta de câmera](-wic-rawguidelines.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



