---
title: Atributo de Margin-Top VML
description: Atributo de Margin-Top VML
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e42d86ba6e0fe05c2b0dff1f6d8bdabba0100fffee97d489fd59360cb8e13bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346392"
---
# <a name="vml-margin-top-attribute"></a>Atributo de Margin-Top VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Especifica a borda superior do retângulo que contém a forma em relação à âncora de forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* margin-top=" *expressão* ">

**Sintaxe do script**

*expressão element* .margin-top=""

*expressão* = *elemento*.margin-top

**Comentários**

O **atributo Margin-Top** é semelhante ao atributo padrão HTML **Margin-Top** usado com folhas de estilos.

Observe que **margintop** é usado em vez de **margin-top** para scripts. Observe também que, se **a posição** for **absoluta,** a margem não será exibida para alteração.

Essa propriedade é usada em vez de **Top** para formas em Microsoft Word e Microsoft Excel que estão flutuantes em uma posição em relação a um ponto de âncora.

Os valores são:



| Valor      | Descrição                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posição padrão de um elemento no fluxo da página.                                                                                                                                           |
| units      | Padrão. Um número com um designador de unidades absolutas (cm, mm, in, pt, pc ou px) ou um designador de unidades relativas (em ou ex). Se nenhuma unidade for dada, será assumido pixels (px). O valor padrão é 0. |
| percentage | Valor expresso como uma porcentagem da altura do objeto pai.                                                                                                                                    |



 

*Atributo padrão VML*

**Consulte também**

[Unidades](msdn-online-vml-units.md)

**Exemplo**

A margem superior é definida como 25 pixels.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-top:25px">
   </v:rect>
```



[Exemplo de atributo Margin-Top](/previous-versions/bb264087(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 