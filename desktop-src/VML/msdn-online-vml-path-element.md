---
title: Elemento Path VML
description: Elemento Path VML
ms.assetid: c5b9f9e3-edee-45fa-9387-8f15e09983ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb46ce43d2dc9ad80aeb21340dceacde80feba99d9debdf66920b662eeaf3a9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308176"
---
# <a name="vml-path-element"></a>Elemento Path VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define um caminho para uma forma.

Os atributos a seguir modificam uma sombra.



| Atributo                                                        | Descrição                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Setaok](msdn-online-vml-arrowok-attribute.md)                 | Determina se as setas serão exibidas.                                |
| [ConnectAngles](msdn-online-vml-connectangles-attribute.md)     | Especifica como uma curva se conectará a um ponto de conexão.                       |
| [ConnectLocs](msdn-online-vml-connectlocs-attribute.md)         | Define o local dos pontos de conexão em um caminho.                            |
| [ConnectType](msdn-online-vml-connecttype-attribute.md)         | Define o tipo de ponto de conexão usado para anexar formas a outras formas. |
| [LtdionOK](msdn-online-vml-extrusionok-attribute.md)         | Determina se umaion será exibida.                              |
| [FillOK](msdn-online-vml-fillok-attribute.md)                   | Determina se um preenchimento será exibido.                                    |
| [GradientShapeOK](msdn-online-vml-gradientshapeok-attribute.md) | Determina se uma forma de gradiente será exibida.                          |
| [ID](id-attribute--path--vml.md)                                | Define um identificador exclusivo para um caminho.                                         |
| [Limusine](msdn-online-vml-limo-attribute.md)                       | Define um ponto de alongamento no caminho.                                            |
| [ShadowOK](msdn-online-vml-shadowok-attribute.md)               | Determina se uma sombra será exibida.                                  |
| [StrokeOK](msdn-online-vml-strokeok-attribute.md)               | Determina se um traço será exibido.                                  |
| [TextBoxRect](msdn-online-vml-textboxrect-attribute.md)         | Define uma ou mais caixas de texto dentro de uma forma.                                   |
| [TextPathOK](msdn-online-vml-textpathok-attribute.md)           | Determina se um caminho de texto será exibido.                                |
| [V](msdn-online-vml-v-attribute.md)                             | Define os comandos que comem um caminho.                                       |



 

**Comentários**

Esse elemento deve ser definido dentro de um [elemento Shape.](shape-element--vml.md)

O código a seguir mostra como definir uma forma com um caminho.


```HTML
   <v:shape strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="top:1;left:1;width:50;height:50">
   <v:path v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



Observe que o [atributo V](msdn-online-vml-v-attribute.md) de **Path** substitui o [atributo Path](msdn-online-vml-path-attribute.md) da [Forma](shape-element--vml.md).

**Exemplos**

-   [Exemplo de elemento filho de caminho simples](/previous-versions/bb229545(v=vs.85))
-   [Exemplo de elemento filho de caminho dinâmico](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/path/x_path.md)

 

 