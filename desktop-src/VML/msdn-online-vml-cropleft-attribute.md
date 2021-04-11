---
title: Atributo CropLeft de VML
description: Atributo CropLeft de VML
ms.assetid: 923482f2-e3eb-4508-81d4-f19db8fcf4eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff01af761e7177d866b46ed48e5d633506aa63fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162317"
---
# <a name="vml-cropleft-attribute"></a>Atributo CropLeft de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a porcentagem de remoção de imagem do lado esquerdo. Leitura/gravação. **VgNumber**.

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *Element* CropLeft = " *expressão* " >

**Sintaxe do script**

*Element* . CropLeft = "*expressão*"

*expressão* = de *elemento*. CropLeft

**Comentários**

A quantidade de corte pode variar de-1,0 a 1,0. O valor padrão é 0. Observe que um valor de 1 não exibirá nenhuma imagem. Valores negativos resultarão na imagem que está sendo descompactada da borda que está sendo cortada (o espaço vazio entre a imagem e a borda cortada será preenchido pela cor de preenchimento da forma). Valores positivos menores que 1 resultarão na imagem restante sendo ampliada para se ajustar à forma.

*Atributo padrão da VML*

**Exemplo**

20% da imagem serão removidas do lado esquerdo e a imagem restante será ampliada para se ajustar à forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropleft=".2" src="kids.jpg"/>
   </v:shape>
```



 

 