---
title: Vídeo (SDK do Windows Media Player)
description: Vídeo
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Aparências móveis do Windows Media Player, vídeo
- capas, vídeo
- referência para capas, vídeo
- vídeo em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d505acec3f6917c7ed3d182c656ff5e9f29f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105764505"
---
# <a name="video-windows-media-player-sdk"></a>Vídeo (SDK do Windows Media Player)

Uma exibição de vídeo permite que o usuário exiba arquivos de vídeo digital. A área de exibição de vídeo só fica visível quando o vídeo é reproduzido ou pausado. Ao projetar sua capa, você desejará reservar espaço na imagem de plano de fundo para conter a exibição do vídeo. Se você não fizer isso, a exibição de vídeo poderá se sobrepor a qualquer arte visível, como o arquivo de plano de fundo, os botões e o trackbars, que impedirá o usuário de operar os controles em sua capa.

A seção de vídeo do arquivo de definição de capa deve começar com esta linha:


```C++
[ Video ]

```



Em seguida, você deve adicionar uma linha que especifica o local e o tamanho da área de exibição do vídeo em sua capa.


```C++
0,38,240,172

```



Você pode usar o modelo a seguir para a seção de vídeo de seu arquivo de definição de capa:


```C++
//  <Location>
//  ----------

```



As seções a seguir fornecem mais detalhes.

-   [Local do vídeo](video-location.md)
-   [Origem da imagem de vídeo](video-image-source.md)
-   [Tamanho do vídeo](video-size.md)
-   [Exemplo de seção de vídeo](sample-video-section.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de capa**](skin-reference.md)
</dt> </dl>

 

 




