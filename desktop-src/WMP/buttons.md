---
title: Botões (Windows Media Player SDK)
description: Botões
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Windows Media Player Capas móveis, visão geral do botão
- capas, visão geral do botão
- referência para capas, botões
- botões em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96128c723c5b8bbac31c82a32060704bc892dfb7
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885532"
---
# <a name="buttons-windows-media-player-sdk"></a>Botões (Windows Media Player SDK)

Você deverá usar um ou mais botões em sua capa e cada botão deve ser definido no arquivo de definição de capa. Se você não definir um botão nesta seção, sua capa não poderá usá-lo.

A seção botões do arquivo de definição de capa começa com esta linha:


```C++
[ Buttons ]

```



Em seguida, você deve adicionar uma ou mais linhas que contenham informações sobre cada um dos botões em sua capa. Uma linha típica pode ser:


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



Observe que esse código deve ser digitado como uma linha começando com "PlayPause" e terminando com "Esvasado @ 160,98".

Você pode usar o seguinte modelo para a seção Botão do arquivo de definição de capa:


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



Novamente, observe que eles devem ser digitados como linhas simples, a primeira começando com "// Function" e terminando com &lt; &gt; " Push &lt; 2 Image Src &gt; ". A segunda linha começa com "// ----------" e termina com "------------------."

As informações de botão para cada linha na seção Botão devem aparecer na ordem a seguir. Somente as seis primeiras partes da linha são necessárias. As imagens secundárias não são incluídas, a menos que sejam necessárias.

1.  [Função Button](button-function.md)
2.  [Tipo de botão](button-type.md)
3.  [Localização do botão](button-location.md)
4.  [Origem da imagem por pushed](pushed-image-source.md)
5.  [Origem da imagem para o botão Desabilitado](image-source-for-disabled-button.md)
6.  [Cor RGB de hit](hit-rgb-color.md)
7.  [Origem de imagem secundária normal](normal-secondary-image-source.md)
8.  [Origem de imagem terciária normal](normal-tertiary-image-source.md)
9.  [Origem da imagem secundária por pushed](pushed-secondary-image-source.md)
10. [Origem da imagem terciária por esão](pushed-tertiary-image-source.md)

Para ver um exemplo de código de botão, consulte [a seção Botão de exemplo](sample-button-section.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de capa**](skin-reference.md)
</dt> </dl>

 

 




