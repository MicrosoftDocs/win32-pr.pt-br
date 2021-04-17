---
description: Miniaturas e visualizações
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Miniaturas e visualizações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e279da9771a43eb75bb94faff23d2e6aa29c4ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751017"
---
# <a name="thumbnails-and-previews"></a>Miniaturas e visualizações

O Windows Vista e a Galeria de fotos do Windows contam com o Windows Imaging Component (WIC) para renderizar miniaturas rápidas e visualizações de imagens. Para dar suporte à renderização rápida de miniatura e visualização, os codecs BRUTOs devem implementar as interfaces WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) e [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) . Para dar suporte a uma experiência de usuário responsiva, é altamente desejável que essas interfaces retornem um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) para o chamador em 200 milissegundos ou menos.

A Microsoft recomenda enfaticamente que os proprietários de formato de arquivo bruto gerem uma visualização renderizada e armazenem em cache o arquivo de imagem. Para um formato no dispositivo, isso geralmente é feito no momento da captura. No entanto, as visualizações também podem ser geradas novamente e armazenadas no arquivo de imagem sempre que as propriedades da interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) forem alteradas – se não for necessário muito trabalho para fazer isso.

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

 

 



