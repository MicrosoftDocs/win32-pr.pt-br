---
title: Atributo TextBoxRect do VML
description: Atributo TextBoxRect do VML
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644d4a89effa54a991d04de4c97c4f9d86876a78d86149d9b99c3a8161585b44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597478"
---
# <a name="vml-textboxrect-attribute"></a>Atributo TextBoxRect do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define uma ou mais caixas de texto dentro de uma forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *elemento* textboxrect=" *expressão* ">

**Sintaxe do script**

*element* .textboxrect="*expression*"

*expressão* = *elemento*.textboxrect

**Comentários**

Uma caixa de texto é definida por um ou mais conjuntos de números que especificam (em ordem) os pontos esquerdo, superior, direito e inferior do retângulo. Vários conjuntos são delimitados por um ponto e vírgula. O valor padrão é o mesmo valor de dimensão que o retângulo que o contém. Se mais de uma caixa de texto for definida, os conjuntos quádruplo delimitados por vírgula que definem cada caixa de texto serão separados por ponto e vírgula. Normalmente, as caixas de texto vêm em conjuntos de 1, 2, 3 ou 6 retângulos em uma forma.

*Atributo padrão VML*

**Exemplo**

Uma caixa de texto de 95 unidades por 95 unidades é definida e colocada 5 unidades dentro do canto superior esquerdo da forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 