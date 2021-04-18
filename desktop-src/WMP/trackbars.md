---
title: Trackbars
description: Trackbars
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Capas móveis do Windows Media Player, trackbars
- capas, trackbars
- referência para capas, trackbars
- trackbars em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb7b64f7bada6f927b25aeecb71d584aa1ec2a68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105807872"
---
# <a name="trackbars"></a>Trackbars

Um TrackBar exibe uma imagem que muda em pequenos incrementos. Trackbars são usados para controles de volume e controles de posição de reprodução. Você pode usar trackbars para exibir informações sobre o item de mídia atual ou para permitir que o usuário altere as configurações ou a posição de reprodução. Por exemplo, você pode usar um TrackBar para permitir que o usuário ajuste o volume e outro TrackBar que possa mostrar o usuário a posição de reprodução atual. Trackbars têm uma imagem em miniatura que define a configuração atual do valor de TrackBar.

A seção trackbars do arquivo de definição de capa deve começar com esta linha:


```C++
[ Trackbars ]

```



Em seguida, você deve adicionar uma ou mais linhas que contêm informações sobre cada uma das trackbars em sua capa.


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



Você pode usar o modelo a seguir para a seção trackbars do seu arquivo de definição de capa:


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



Você deve usar a seguinte ordem para informações de TrackBar para cada linha na seção trackbars (cada parte da linha é necessária):

1.  [Tipo de TrackBar](trackbar-type.md)
2.  [Local TrackBar](trackbar-location.md)
3.  [Origem da imagem para TrackBar desabilitada](image-source-for-disabled-trackbar.md)
4.  [Origem da imagem em miniatura](thumb-image-source.md)
5.  [Tamanho da miniatura](thumb-size.md)

Para obter um exemplo de código trackbars, consulte a [seção trackbars de exemplo](sample-trackbars-section.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de capa**](skin-reference.md)
</dt> </dl>

 

 




