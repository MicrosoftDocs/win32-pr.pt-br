---
title: Origem da imagem em miniatura
description: Origem da imagem em miniatura
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Capas móveis do Windows Media Player, trackbars
- capas, trackbars
- referência para capas, trackbars
- trackbars em capas, origem da imagem
- trackbars em capas, origem do Thumb Image
- origem da imagem para capas, trackbars
- Thumb, origem da imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac19053b58c7d12543d38c639abe5a43c01ff64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005180"
---
# <a name="thumb-image-source"></a>Origem da imagem em miniatura

Você deve definir o nome do arquivo que contém a imagem do Thumb. Ele deve ser um nome de arquivo válido com a extensão. bmp,. gif,. jpg ou. png. O arquivo deve conter três imagens lado a lado de tamanho idêntico. Eles devem ser adjacentes entre si sem nenhum espaço entre eles. A posição superior esquerda da imagem esquerda deve estar no canto superior esquerdo do arquivo. A imagem no lado esquerdo é a imagem normal da imagem em miniatura, e a imagem no meio mostra o estado enviado e a imagem à direita representa o estado desabilitado.


```C++
SeekThumb.bmp

```



Talvez você queira tornar as áreas do Thumb Image transparentes. Isso permitirá que você crie imagens thumbs em formas diferentes de retangulares. Qualquer região da imagem do Thumb que você preencher com a cor especificada pelo valor RGB 255, 0, 255 aparecerá transparente em sua capa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trackbars**](trackbars.md)
</dt> </dl>

 

 




