---
title: Atributo CropRight de VML
description: Atributo CropRight de VML
ms.assetid: 1e2bd8e8-3d56-435d-bfaf-fb07f6b6fba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d695bb3fd9e88c3357343860dcbbff820e5a49a22100d59fe46c502b642e31d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796296"
---
# <a name="vml-cropright-attribute"></a>Atributo CropRight de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define a porcentagem de remoção de imagem do lado direito. Leitura/gravação. **VgNumber**.

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *Element* CropRight = " *expressão* " >

**Sintaxe do script**

*Element* . CropRight = "*expressão*"

*expressão* = de *elemento*. CropRight

**Comentários**

A quantidade de corte pode variar de-1,0 a 1,0. O valor padrão é 0. Observe que um valor de 1 não exibirá nenhuma imagem. Valores negativos resultarão na imagem que está sendo descompactada da borda que está sendo cortada (o espaço vazio entre a imagem e a borda cortada será preenchido pela cor de preenchimento da forma). Valores positivos menores que 1 resultarão na imagem restante sendo ampliada para se ajustar à forma.

*Atributo padrão da VML*

**Exemplo**

A imagem será descompactada do lado direito em 20% da largura. O espaço vazio entre a imagem e a borda direita será preenchido pela cor de preenchimento da forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="blue"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropright="-.2" src="kids.jpg"/>
   </v:shape>
```





 

 