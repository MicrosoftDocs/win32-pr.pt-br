---
title: UI_PKEY_FontProperties_Size
description: Identifica a propriedade Tamanho de \_ \_ FontProperties PKEY da interface do \_ usuário.
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9c013c41290f6e062b03572a9e3cb848752efcb12f1c779348a0253f94d40e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028624"
---
# <a name="ui_pkey_fontproperties_size"></a>Tamanho de \_ \_ FontProperties de PKEY da interface do \_ usuário

Identifica a propriedade Tamanho de \_ \_ FontProperties PKEY da interface do \_ usuário.

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

O tamanho \_ de FontProperties de PKEY da interface do usuário é usado por um aplicativo para consultar \_ o valor do controle Tamanho \_ **da** fonte.

Valores válidos para esse intervalo de propriedades de 1 a 9999, inclusive. Se um usuário tentar inserir um valor inválido,  a entrada será rejeitada e o controle Tamanho da fonte será revertedo para o último valor válido.

Se um aplicativo tentar definir o tamanho da fonte programaticamente como um valor fora do intervalo válido, a estrutura da Faixa de Opções invalida todas as propriedades de fonte e define os controles de fonte (**Tamanho** da fonte e Face da **fonte**) como em branco ou para seu estado padrão, quando apropriado.

O valor padrão é 0.

Um valor de 0 especifica que nenhum tamanho de ponto único está selecionado (nenhum texto ou uma série de texto de tamanho heterogêneo é selecionada).

Um usuário não pode definir o **controle Tamanho da** fonte como 0.

Além de 0, valores válidos para FontProperties PKEY da interface do usuário Intervalo de tamanho entre \_ \_ \_ *MinimumFontSize* e *MaximumFontSize* [](windowsribbon-controls-fontcontrol.md) conforme declarado na marcação Controle de Fonte.

> [!Note]  
> O **controle Tamanho** da fonte é definido como em branco quando o tamanho da fonte é definido programaticamente como 0, como quando uma série de texto de tamanho heterogêneo é realçada.

 

Quando uma operação de texto de tamanho heterogêneo é selecionada, o aplicativo deve  consultar  a interface do usuário [ \_ \_ FontProperties \_ DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) para capturar os comandos Aumentar fonte e Reduzir fonte.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




