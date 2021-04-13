---
title: Origem da imagem para o botão desabilitado
description: Origem da imagem para o botão desabilitado
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Aparências móveis do Windows Media Player, origem da imagem do botão
- aparência, origem da imagem do botão
- referência para capas, botões
- botões em capas, origem da imagem
- origem da imagem para capas, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ccd0362f3dd11acec71eaf0b92574f2c27c77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364025"
---
# <a name="image-source-for-disabled-button"></a>Origem da imagem para o botão desabilitado

Você deve definir a origem da imagem que deseja exibir quando um botão é desabilitado ou tem um estado que corresponde a desativado. A imagem é proveniente do arquivo definido como desabilitado na seção bitmaps. Você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço. Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do arquivo de bitmap. O local no qual a imagem será exibida vem das coordenadas definidas para o botão em relação à imagem de plano de fundo, mas o local de origem é definido pelos dois números após "Disabled @" e é relativo ao bitmap desabilitado do qual você está lendo a imagem.

Por exemplo, para usar uma imagem do bitmap desabilitado que está no arquivo desabilitado em um local superior e esquerdo de 50, 60 pixels, use o seguinte código:


```C++
Disabled @ 50,60

```



Você deve definir um bitmap desabilitado. Se você não quiser exibir uma imagem diferente, poderá definir o bitmap de plano de fundo como seu bitmap desabilitado com um deslocamento de 0, 0:


```C++
Disabled @ 50,60

```



No exemplo anterior, 50, 60 é o local do botão com o qual você está trabalhando no arquivo desabilitado (nesse caso, o mesmo local que o botão no bitmap em segundo plano). No entanto, é altamente recomendável que você exiba uma imagem desabilitada para todos os botões para dar a seus usuários uma indicação visual, pois muitos botões não serão utilizáveis em determinadas condições, como uma lista de reprodução vazia. Se os usuários souberem que um botão está desabilitado, eles não continuarão tentando clicar nele ou acreditar que sua capa não está funcionando como projetado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Botões**](buttons.md)
</dt> </dl>

 

 




