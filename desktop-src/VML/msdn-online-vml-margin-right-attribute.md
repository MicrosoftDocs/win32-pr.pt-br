---
title: Atributo Margin-Right de VML
description: Atributo Margin-Right de VML
ms.assetid: 7b635bea-df3f-4a24-aa22-cfca95575599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5529257a0e21c8a8f8c7a1a2f8381c10a6e3b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008340"
---
# <a name="vml-margin-right-attribute"></a>Atributo Margin-Right de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica a borda direita da forma que contém o retângulo em relação à âncora de forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* Style = "margin-right: *expression* " >

**Sintaxe do script**

*elemento* . Style. marginright = "*expressão*"

*expressão* = de *elemento*. Style. marginright

**Comentários**

O atributo **margin-right** é semelhante ao atributo de margem HTML padrão **-direito** usado com folhas de estilo.

Observe que **marginright** é usado em vez de **margin-right** para scripts. Observe também que, se a **posição** for **absoluta**, a margem não parecerá ser alterada.

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

A margem direita é definida como 25 pixels.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-right:25px">
   </v:rect>
```



[Exemplo do atributo margin-right](/previous-versions/bb229677(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 