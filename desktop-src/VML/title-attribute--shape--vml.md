---
title: Atributo Title (forma) (VML)
description: Atributo Title (forma) (VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075b1cf078617abd3486ba55008794e1342efa63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454324"
---
# <a name="title-attribute-shapevml"></a>Atributo Title (forma) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o texto exibido quando o ponteiro do mouse se move sobre a forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* título = " *expression* " >

**Sintaxe do script**

*elemento* . title = "*expressão*"

*expressão* = de *elemento*. title

**Comentários**

O atributo **título** é semelhante ao atributo padrão de **título** HTML. O comportamento de um título é semelhante a uma dica de ferramenta do Microsoft Windows.

**Atributo padrão da VML**

**Exemplo**

O título da forma é "exibição da dica de ferramenta" e aparecerá quando o ponteiro do mouse se mover sobre a forma.


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemplo de atributo de título](/previous-versions/bb264097(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 