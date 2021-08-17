---
title: Atributo de arco de VML
description: Atributo de arco de VML
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8715440f56625d16ed5b4386120dbf50588ce861c1ba59772e3ec8f35a077dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755120"
---
# <a name="vml-arcsize-attribute"></a>Atributo de arco de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define a quantidade de arredondamento para um retângulo arredondado. Leitura/gravação. [VgFraction](msdn-online-vml-vgfraction-data-type.md) .

**Aplica-se a**

[RoundRect](msdn-online-vml-roundrect-element.md)

**Sintaxe de marca**

<v: *Element* = " *expression* " >

**Sintaxe do script**

*Element* . anestable = "*expression*"

*expressão* = de *elemento*. arcoize

**Comentários**

Define os cantos arredondados de um retângulo arredondado como uma porcentagem da metade da dimensão menor do comprimento e da largura de um retângulo. 0% teria cantos quadrados e 100% formaria cantos circulares. Um quadrado com um valor de **arcos** de 1,0 seria um círculo. O valor padrão é 0,2 (20%).

*Atributo padrão da VML*

**Exemplo**

O retângulo arredondado é desenhado com cantos apertados e arredondados.


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 