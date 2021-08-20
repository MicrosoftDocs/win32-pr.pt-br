---
title: Atributo VML Z-index
description: Atributo VML Z-index
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07100b2ecdbda792ea3f7d5550759430539b95b86c5ef76ded2f9238785b1151
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123766"
---
# <a name="vml-z-index-attribute"></a>Atributo VML Z-index

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Determina a ordem de exibição de formas sobrepostas. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* Style = "z-index: *expression* " >

**Sintaxe do script**

*elemento* . Style. ZIndex = "*expressão*"

*expressão* = de *elemento*. Style. ZIndex

**Comentários**

O atributo **z-index** é semelhante ao atributo HTML **z-index** padrão para estilos.

Os valores são:



| Valor | Descrição                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto  | A ordem em que as formas aparecem na página HTML será usada, de baixo para cima.                                                                                                                         |
| ordem | Um número que representa a precedência de empilhamento. Uma forma com um número mais alto será exibida como se wereoverlapping (em "frente" de) uma forma com um número mais baixo. Números negativos podem ser usados. |



 

*Atributo padrão da VML*

**Exemplo**

A forma vermelha será exibida em "frente" da forma azul, pois ela tem um índice z superior.


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



[Exemplo de atributo Z-index](/previous-versions/ms530275(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 