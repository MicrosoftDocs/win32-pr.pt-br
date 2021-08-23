---
title: Origem da imagem para o botão Desabilitado
description: Origem da imagem para o botão Desabilitado
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Windows Media Player Capas móveis, origem da imagem do botão
- capas, origem da imagem do botão
- referência para capas, botões
- botões em capas, origem da imagem
- fonte da imagem para capas, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a3b31a25eb40d82d33f241a6eaebf690fe11aa2128528739a7e7bbb4dc217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509256"
---
# <a name="image-source-for-disabled-button"></a>Origem da imagem para o botão Desabilitado

Você deve definir a origem da imagem que deseja exibir quando um botão estiver desabilitado ou tiver um estado que corresponda a desativado. A imagem vem do arquivo que você definiu como Desabilitado na seção Bitmaps. Você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço. Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do arquivo bitmap. O local no qual a imagem será exibida vem das coordenadas definidas para o botão em relação à imagem De plano de fundo, mas o local de origem é definido pelos dois números após "Disabled @" e é relativo ao bitmap desabilitado do qual você está lendo a imagem.

Por exemplo, para usar uma imagem do bitmap Desabilitado que está no arquivo Desabilitado em um local superior e esquerdo de 50,60 pixels, use o seguinte código:


```C++
Disabled @ 50,60

```



Você deve definir um bitmap desabilitado. Se você não quiser exibir uma imagem diferente, poderá definir o bitmap background como seu bitmap Desabilitado com um deslocamento de 0,0:


```C++
Disabled @ 50,60

```



No exemplo anterior, 50,60 é o local do botão com o que você está trabalhando no arquivo Desabilitado (nesse caso, o mesmo local que o botão no bitmap De plano de fundo). No entanto, é altamente recomendável exibir uma imagem Desabilitada para todos os botões para dar aos usuários uma indicação visual, pois muitos botões não serão viáveis em determinadas condições, como uma playlist vazia. Se os usuários sabem que um botão está desabilitado, eles não continuarão tentando clicar nele ou acharão que sua capa não está funcionando como projetado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Botões**](buttons.md)
</dt> </dl>

 

 




