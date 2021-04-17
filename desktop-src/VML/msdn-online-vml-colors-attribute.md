---
title: Atributo de cores da VML
description: Atributo de cores da VML
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c5df5b2dc97c19441d6abaf6cd6c03d949c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499103"
---
# <a name="vml-colors-attribute"></a>Atributo de cores da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define várias cores para um preenchimento gradual. Leitura/gravação. **IVgGradientColorArray**.

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *Element* Colors = " *expression* " >

**Sintaxe do script**

*Element* . Colors = "*expression*"

*expressão* = de *elemento*. Colors

**Comentários**

Usado para definir uma matriz que consiste em valores emparelhados de percentuais ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) e Color ([VgColor](msdn-online-vml-ivgcolor.md)). A matriz cria um preenchimento combinado usando cada ponto na matriz, começando em 0% (definido por **cor**) e terminando em 100% (definido por **Color2**). As cores intermediárias ao longo do caminho podem ser definidas atribuindo um valor de cor a uma porcentagem. O par de porcentagem e de cores não é separado por uma vírgula, mas os pares são separados uns dos outros por vírgulas.

Atributo padrão da VML

**Exemplo**

A forma tem um preenchimento gradual que consiste em quatro cores, começando com vermelho, mesclando para amarelo, em seguida, verde e finallyblue.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   colors="30% yellow,70% green"/>
   </v:shape>
```



 

 