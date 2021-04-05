---
title: Botões (SDK do Windows Media Player)
description: Botões
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Aparências móveis do Windows Media Player, visão geral do botão
- capas, visão geral do botão
- referência para capas, botões
- botões em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f06eb2fe21ee18a24f92e92d4fa760e9c76887
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085102"
---
# <a name="buttons-windows-media-player-sdk"></a>Botões (SDK do Windows Media Player)

Você desejará usar um ou mais botões em sua capa, e cada botão deve ser definido no arquivo de definição de capa. Se você não definir um botão nesta seção, sua capa não será capaz de usá-lo.

A seção de botões do arquivo de definição de capa começa com esta linha:


```C++
[ Buttons ]

```



Em seguida, você deve adicionar uma ou mais linhas que contêm informações sobre cada um dos botões em sua capa. Uma linha típica pode ser:


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



Observe que esse código deve ser digitado como uma linha que começa com "PlayPause" e termina com "Push @ 160, 98".

Você pode usar o modelo a seguir para a seção de botões do arquivo de definição de capa:


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



Novamente, observe que elas devem ser digitadas como linhas únicas, a primeira começando com "// <Function> " e terminando com " &lt; push 2 Image src &gt; ". A segunda linha começa com "//----------" e termina com "------------------."

As informações do botão para cada linha na seção de botão devem aparecer na seguinte ordem. Somente as seis primeiras partes da linha são obrigatórias. As imagens secundárias não são incluídas, a menos que sejam necessárias.

1.  [Função de botão](button-function.md)
2.  [Tipo de botão](button-type.md)
3.  [Local do botão](button-location.md)
4.  [Origem da imagem enviada por push](pushed-image-source.md)
5.  [Origem da imagem para o botão desabilitado](image-source-for-disabled-button.md)
6.  [Pressione a cor RGB](hit-rgb-color.md)
7.  [Fonte de imagem secundária normal](normal-secondary-image-source.md)
8.  [Fonte de imagem terciário normal](normal-tertiary-image-source.md)
9.  [Fonte de imagem secundária enviada por push](pushed-secondary-image-source.md)
10. [Fonte de imagem terciário enviada por push](pushed-tertiary-image-source.md)

Para obter um exemplo de código de botão, consulte a [seção de botão de exemplo](sample-button-section.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de capa**](skin-reference.md)
</dt> </dl>

 

 




