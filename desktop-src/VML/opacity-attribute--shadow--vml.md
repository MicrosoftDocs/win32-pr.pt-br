---
title: Atributo Opacity (Sombra)(VML)
description: Atributo Opacity (Sombra)(VML)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43287a4bb6de9f2dd0d9d2b0af97d971314ab7e93ab2c4fae58b666ee1a94124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680616"
---
# <a name="opacity-attribute-shadowvml"></a>Atributo Opacity (Sombra)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina a transparência de uma sombra. Leitura/gravação. [VgAção .](msdn-online-vml-vgfraction-data-type.md)

**Aplica-se a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxe de marca**

<v: *elemento* opacity=" *expressão* ">

**Sintaxe do script**

*expressão* element .opacity=""

*expressão* = *elemento*.opacity

**Comentários**

O valor padrão é 1. Um valor de 0 fará uma sombra completamente transparente.

*Atributo padrão VML*

**Exemplo**

A forma tem uma sombra que é 50% transparente.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 