---
title: UI_PKEY_FontProperties_Size
description: Identifica a propriedade de tamanho da interface do usuário \_ PKEY \_ fontproperties \_ .
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae991cfe5f91b4aca4fe0b49a7b7c547e71b0fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761914"
---
# <a name="ui_pkey_fontproperties_size"></a>\_Tamanho da \_ fonte de PKEY da interface do usuário \_

Identifica a propriedade de tamanho da interface do usuário \_ PKEY \_ fontproperties \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Size
   shellPKey = UI_PKEY_FontProperties_Size
   formatID = 00000302-7363-696e-8441798acf5aebb7
   propID = 302
   typeInfo
      type = VT_DECIMAL
```

## <a name="remarks"></a>Comentários

\_O tamanho da fonte de PKEY da interface do usuário \_ \_ é usado por um aplicativo para consultar o valor do controle de **tamanho da fonte** .

Os valores válidos para esse intervalo de propriedade são de 1 a 9999, inclusive. Se um usuário tentar inserir um valor inválido, a entrada será rejeitada e o controle de **tamanho da fonte** reverterá para o último valor válido.

Se um aplicativo tentar definir o tamanho da fonte programaticamente para um valor fora do intervalo válido, a estrutura da faixa de opções invalidará todas as propriedades de fonte e definirá os controles de fonte (**tamanho da fonte** e **face da fonte**) como em branco ou com seu estado padrão, quando apropriado.

O valor padrão é 0.

Um valor de 0 especifica que nenhum único tamanho de ponto é selecionado (nenhum texto ou uma execução de texto de tamanho heterogêneo, é selecionado).

Um usuário não pode definir o controle de **tamanho da fonte** como 0.

Diferente de 0, os valores válidos para a interface do usuário \_ PKEY \_ fontproperties \_ dimensionar intervalo entre *MinimumFontSize* e *MaximumFontSize* como declarado na marcação de [controle de fonte](windowsribbon-controls-fontcontrol.md) .

> [!Note]  
> O controle **tamanho da fonte** é definido como em branco quando o tamanho da fonte é definido por meio de programação como 0, como quando uma execução de texto de tamanho heterogêneo é realçada.

 

Quando uma execução de texto de tamanho heterogêneo é selecionada, o aplicativo deve consultar a [interface do usuário \_ PKEY \_ fontproperties \_ DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) para capturar **aumentar a fonte** e reduzir os comandos de **fonte** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




