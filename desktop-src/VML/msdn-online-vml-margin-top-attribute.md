---
title: Atributo Margin-Top de VML
description: Atributo Margin-Top de VML
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14b6f4743f04740fe3fdbac4cc1d03f7bbe0282
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294483"
---
# <a name="vml-margin-top-attribute"></a>Atributo Margin-Top de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica a borda superior da forma que contém o retângulo em relação à âncora de forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* margin-top = " *expressão* " >

**Sintaxe do script**

*elemento* . margin-top = "*expressão*"

*expressão* = de *elemento*. margin-top

**Comentários**

O atributo **margin-top** é semelhante ao atributo padrão **de margem HTML-superior** usado com folhas de estilo.

Observe que **MarginTop** é usado em vez de **margin-top** para scripts. Observe também que, se a **posição** for **absoluta**, a margem não parecerá ser alterada.

Essa propriedade é usada em vez de **Top** para formas no Microsoft Word e no Microsoft Excel que estão flutuantes em uma posição relativa a um ponto de ancoragem.

Os valores são:



| Valor      | Descrição                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automático       | Posição padrão de um elemento no fluxo da página.                                                                                                                                           |
| units      | Padrão. Um número com um designador de unidades absolutas (cm, mm, em, pt, PC ou px) ou um designador de unidades relativas (em ou ex). Se nenhuma unidade for fornecida, serão assumidos pixels (px). O valor padrão é 0. |
| percentage | Valor expresso como uma porcentagem da altura do objeto pai.                                                                                                                                    |



 

*Atributo padrão da VML*

**Consulte também**

[Unidades](msdn-online-vml-units.md)

**Exemplo**

A margem superior é definida como 25 pixels.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-top:25px">
   </v:rect>
```



[Exemplo do atributo margin-top](/previous-versions/bb264087(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 