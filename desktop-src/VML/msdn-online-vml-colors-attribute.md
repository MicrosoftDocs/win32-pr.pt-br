---
title: Atributo Cores do VML
description: Atributo Cores do VML
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a699b0ab8da898dd82fa4e1bf4823c0f9fdd443eb8275e25dbfaac6d2f039a6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999276"
---
# <a name="vml-colors-attribute"></a>Atributo Cores do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define várias cores para um preenchimento de gradiente. Leitura/gravação. **IVgGradientColorArray.**

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *element* colors=" *expressão* ">

**Sintaxe do script**

*elemento* .colors="*expression*"

*expressão* = *elemento*.colors

**Comentários**

Usado para definir uma matriz que consiste em valores emparelhados de percentuais ([VgAção](msdn-online-vml-vgfraction-data-type.md)) e cor ([VgColor](msdn-online-vml-ivgcolor.md)). A matriz cria um preenchimento misto usando cada ponto na matriz, começando em 0% (definido por Cor **)** e terminando em 100% (definido por **Color2**). As cores intermediárias ao longo do caminho podem ser definidas atribuindo um valor de cor a um percentual. A porcentagem e o par de cores não são separados por uma vírgula, mas os pares são separados uns dos outros por vírgulas.

Atributo padrão VML

**Exemplo**

A forma tem um preenchimento de gradiente que consiste em quatro cores, começando com vermelho, combinando com amarelo, em seguida, verde e finalmenteblue.


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



 

 