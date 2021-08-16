---
title: Atributo de foco VML
description: Atributo de foco VML
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b60eeb9ff379c8006cbb9068b6b78c8f24490ecf2fd15573b5b224a9ee1208ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057864"
---
# <a name="vml-focus-attribute"></a>Atributo de foco VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o centro de um preenchimento de gradiente linear. Leitura/gravação. **VgAção .**

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *elemento* focus=" *expressão* ">

**Sintaxe do script**

*element* .focus="*expression*"

*expressão* = *elemento*.focus

**Comentários**

Define a posição inicial central da combinação. Os valores variam de 100% a -100%. O valor padrão é 0. Um valor de 100% (ou -100%) deslocará o foco para que a direção da combinação seja inversa (na verdade, revertendo **Cor** e **Cor2**). Um valor de 50% alterará a combinação para que **Color** seja em ambas as extremidades e **Color2** no meio. Um valor de -50% alterará a combinação para que **Color2** seja em ambas as extremidades e **Color** seja no meio.

*Atributo padrão VML*

**Exemplo**

O foco de gradiente do preenchimento é deslocado para que vermelho **(** Cor ) seja uma faixa no centro da forma e que a parte superior e inferior seja azul (**Color2**).


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 