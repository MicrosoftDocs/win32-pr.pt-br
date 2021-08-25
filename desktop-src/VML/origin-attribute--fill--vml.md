---
title: Atributo De origem (Preenchimento)(VML)
description: Atributo De origem (Preenchimento)(VML)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc33ae1f4cf7c588ae9b3f40ff8c445be88192bae1dfc86a3593eea931befb25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959216"
---
# <a name="origin-attribute-fillvml"></a>Atributo De origem (Preenchimento)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o centro de uma imagem de preenchimento. Leitura/gravação. [VgVector2D.](msdn-online-vml-ivgvector2d-data-type.md)

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *element* origin=" *expressão* ">

**Sintaxe do script**

*element* .origin="*expression*"

*expressão* = *elemento*.origin

**Comentários**

Especifica um ponto relativo ao canto superior esquerdo da imagem; esse ponto é tratado como a origem da imagem. O padrão é o centro da imagem. O vetor é uma fração da largura e altura da imagem.

*Atributo padrão VML*

**Exemplo**

A imagem do preenchimento é deslocada para a esquerda para um ponto de 50% da largura da forma .


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 