---
title: bitmaps (Windows Media Player SDK)
description: Bitmaps
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Windows Media Player Capas móveis, bitmaps
- capas, bitmaps
- referência para capas, bitmaps
- bitmaps em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ff4689c052162d8addfb9a66aeb6b227916f0e22e21de3e3572ea265380664
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123856"
---
# <a name="bitmaps-windows-media-player-sdk"></a>bitmaps (Windows Media Player SDK)

Você deve usar uma ou mais imagens em sua capa e cada imagem deve ser definida no arquivo de definição de capa. Se você não definir uma imagem nesta seção, sua capa não será capaz de usá-la.

O termo "bitmap" é usado em toda a referência em um sentido genérico e refere-se a imagens de bitmap com uma extensão .bmp, imagens GIF com uma extensão .gif, imagens JPEG com uma extensão .jpg e imagens PNG com uma extensão .png.

A seção bitmaps do arquivo de definição de capa começa com esta linha:


```C++
[ Bitmaps ]

```



Em seguida, você deve adicionar uma ou mais linhas que contêm informações sobre cada uma das imagens em sua capa.

Uma linha típica pode ser:


```C++
    Background  Background.bmp  0,0

```



Você pode usar o modelo a seguir para a seção bitmaps do seu arquivo de definição de capa:


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



Você deve usar a seguinte ordem para informações de bitmap para cada linha na seção de bitmap. Cada parte da linha é necessária.

1.  [Tipo de bitmap](bitmap-type.md)
2.  [Nome do Arquivo](file-name.md)
3.  [Coordenadas](coordinates.md)

Para obter um exemplo de código de bitmap, consulte a [seção bitmap de exemplo](sample-bitmap-section.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de capa**](skin-reference.md)
</dt> </dl>

 

 




