---
title: Atributo onmouseover da VML
description: Atributo onmouseover da VML
ms.assetid: 68f0fa7a-0d22-4ede-8404-e007296960e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d2bb65864987988996cfad710360fd908a5248c11857e8df1eb5a941b1b895b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999126"
---
# <a name="vml-onmouseover-attribute"></a>Atributo onmouseover da VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Dispara um evento de mouse para uma forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* onmouseover = " *expressão* " >

**Comentários**

Um evento "mouseover" é gerado quando o ponteiro do mouse está sobre a forma. O valor é gerado usando a palavra-chave **this** (como uma referência ao objeto) seguida pela sintaxe do modelo de objeto. Por exemplo, para alterar a cor de preenchimento para vermelho, use o seguinte:

onmouseover = "this. FillColor = ' Red '"

Observe o uso de aspas simples e duplas para definir a expressão.

*Atributo padrão da VML*

**Exemplo**

Quando o ponteiro do mouse estiver na forma, a cor de preenchimento mudará de vermelho para verde.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20"
   onmouseover='this.fillcolor="green"'>
   </v:rect>
```



[Exemplo de atributo onmouseover](/previous-versions/bb264088(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 