---
title: Origem da imagem de miniatura
description: Origem da imagem de miniatura
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Windows Media Player Capas móveis, barras de faixa
- skins,trackbars
- referência para capas, barras de faixa
- trackbars in skins,image source
- trackbars in skins,thumb image source
- fonte de imagem para capas, barras de faixa
- thumb,image source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550569a2858ba283824f28f6793097caa140c6112bccc41b3423413e17b6d89a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122766"
---
# <a name="thumb-image-source"></a>Origem da imagem de miniatura

Você deve definir o nome do arquivo que contém a imagem digital. Esse deve ser um nome de arquivo válido com a extensão .bmp, .gif, .jpg ou .png. O arquivo deve conter três imagens lado a lado de tamanho idêntico. Eles devem ser adjacentes uns aos outros sem espaço entre eles. A posição superior esquerda da imagem esquerda deve estar no canto superior esquerdo do arquivo. A imagem no lado esquerdo é a imagem normal para a imagem de miniatura e a imagem no meio representa o estado pressionado e a imagem à direita representa o estado desabilitado.


```C++
SeekThumb.bmp

```



Talvez você queira tornar determinadas áreas da imagem de miniatura transparentes. Isso permitirá que você crie imagens em miniatura em formas diferentes das retangulares. Qualquer região da imagem de miniatura que você preencher com a cor especificada pelo valor RGB 255, 0, 255 aparecerá transparente na sua capa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trackbars**](trackbars.md)
</dt> </dl>

 

 




