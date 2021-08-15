---
title: Atributo de Margin-Bottom VML
description: Atributo de Margin-Bottom VML
ms.assetid: c1101430-f4fc-4fa5-8e02-7cee126c2c1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 551cf9cba00901e07998f2de38465cba1cb45bb8f563c04d1adf25f75d1852bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057814"
---
# <a name="vml-margin-bottom-attribute"></a>Atributo de Margin-Bottom VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Especifica a borda inferior do retângulo que contém a forma em relação à âncora de forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* margin-bottom=" *expressão* ">

**Sintaxe do script**

*expressão element* .marginbottom=""

*expressão* = *elemento*.marginbottom

**Comentários**

O **atributo Margin-Bottom** é semelhante ao atributo padrão **HTML Margin-Bottom** usado com folhas de estilos.

Observe que **marginbottom** é usado em vez da **margem inferior** para script. Observe também que, se **a posição** for **absoluta,** a margem não será exibida para alteração.

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

A margem inferior é definida como 25 pixels.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-bottom:25px">
   </v:rect>
```



[Exemplo de atributo Margin-Bottom](/previous-versions/bb229675(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 