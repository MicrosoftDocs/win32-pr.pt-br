---
title: Atributo adj
description: Atributo adj
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85869500cc3e9f86e0f48e67f63cfd9e6ed2cff5580caa04994169a9e4b50df8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137139"
---
# <a name="adj-attribute"></a>Atributo adj

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Especifica um valor de ajuste usado para definir valores para uma fórmula. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* adj = " *expressão* " >

**Sintaxe do script**

*Element* . adj = "*expressão*"

*expressão* = de *elemento*. adj

**Comentários**

O **adj** é usado para fornecer pontos ajustáveis para uma fórmula. Se usado em marcas, **adj** é uma cadeia de caracteres delimitada por vírgula de até 8 valores. Alguns valores podem ser omitidos. Por exemplo, "0, 1, 2,, 4, 5,, 7" seria uma cadeia de caracteres válida, mas o quarto e o sétimo itens não teriam valores (itens são contados a partir de 0).

Para scripts, **adj** usa o tipo de dados [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) .

*Atributo padrão da VML*

**Consulte também**

[Fórmula](msdn-online-vml-formulas-element.md)

**Exemplo**

Um quadrado simples é criado com ajustes. Primeiro, a cadeia de caracteres de **adj** é criada para definir oito valores de ajuste. Em seguida, cada valor de ajuste é referenciado por uma das oito fórmulas, com cada valor de ajuste precedido por um símbolo de sinal de número ( \# ). Por fim, um caminho é definido por uma cadeia de caracteres que faz referência às fórmulas, com cada fórmula precedida pelo símbolo de arroba (@).


```HTML
   <v:shape id="rect01" type="#myshape"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:30;left:30;width:20;height:20"
   adj="1, 1, 1, 200, 200, 200, 200, 1">
   <v:path v="m @0,@1 l @2,@3, @4,@5, @6,@7 x e"/>
   <v:formulas>
   <v:f eqn="val #0"/>
   <v:f eqn="val #1"/>
   <v:f eqn="val #2"/>
   <v:f eqn="val #3"/>
   <v:f eqn="val #4"/>
   <v:f eqn="val #5"/>
   <v:f eqn="val #6"/>
   <v:f eqn="val #7"/>
   </v:formulas>
   </v:shape>
```



[Exemplo de atributo adj](/previous-versions/bb229662(v=vs.85)) (requer o Microsoft Internet Explorer 5 ou superior).

 

 