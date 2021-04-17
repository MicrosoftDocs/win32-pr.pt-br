---
title: Pressione a cor RGB
description: Pressione a cor RGB
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Aparências móveis do Windows Media Player, cores de botão
- aparências, cores de botão
- referência para capas, botões
- botões em capas, cores
- referência de cores para capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c69863c4197702383f729c8d7e8d30d3cb52bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105779997"
---
# <a name="hit-rgb-color"></a>Pressione a cor RGB

Se você estiver usando botões de região (PushHit, ToggleHit e 2PushHit), será necessário definir a cor que o Windows Media Player usará para determinar a área de pressionamento do botão. Esse valor deve ser especificado usando três inteiros positivos separados por vírgulas. Esses inteiros representam a quantidade de vermelho, verde e azul para uma cor de bitmap e variam de 0 a 255.

> [!Note]  
> Os tipos de botões são preteridos em capas para Windows Media Player 10 Mobile ou posterior.

 

Você pode usar quaisquer cores para os valores, mas certifique-se de que cada botão de região definido tem uma cor exclusiva no arquivo de imagem de região e que o valor de cor definido aqui como um número corresponde à cor real usada na imagem da região.

A tabela a seguir mostra algumas cores típicas que talvez você queira usar.



| Valor       | Descrição |
|-------------|-------------|
| 0, 0, 0       | Preto       |
| 255.255.255 | Branca       |
| 255, 0, 0     | Vermelho         |
| 0255, 0     | Verde       |
| 0, 0255     | Azul        |



 

Se você não usar botões de região, deverá inserir o seguinte:


```C++
0,0,0

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Botões**](buttons.md)
</dt> </dl>

 

 




