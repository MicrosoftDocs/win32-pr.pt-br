---
title: Atributos de escuta
description: Atributos de escuta
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Windows Media Player capas, atributos de escuta
- capas, atributos de escuta
- referência para capas, atributos de escuta
- atributos de escuta
- atributos, ouvindo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8cceb9a8721995c494b5e4366291353376a2569c045e41eb41c1418e2f4d5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996406"
---
# <a name="listening-attributes"></a>Atributos de escuta

Um atributo de escuta é usado para conectar um atributo a outro para que seu valor seja alterado toda vez que o valor do outro atributo for alterado.

O atributo de escuta **wmpprop:** é o mais útil. Se o valor de um atributo for especificado para ser o **wmpprop:** de um segundo atributo, o primeiro valor será atualizado automaticamente para refletir o segundo valor cada vez que o segundo valor for alterado.

**Exemplo:**


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



Dessa forma, o valor de mydeslizer, mostrado pela posição do controle deslizante, também pode ser mostrado como um número dentro de uma caixa de texto.

Os dois outros atributos de escuta, **wmpenabled:** e **wmpdisabled:**, podem ser usados para alterar o atributo **habilitado** de um controle dependendo se sua funcionalidade está disponível no Player no momento. Esses atributos podem escutar somente para métodos do objeto **Controls** .

**Exemplo:**


```C++
<BUTTON 
  id="play" 
  enabled="wmpenabled:player.controls.play"
/>

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Diversos**](miscellaneous.md)
</dt> </dl>

 

 




