---
title: Atributo Color2 (Sombra)(VML)
description: Atributo Color2 (Sombra)(VML)
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241c7e0a620b6b5f2f54a8849779dcc905d027781fe38a5121ca74b6acbeac4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655696"
---
# <a name="color2-attribute-shadowvml"></a>Atributo Color2 (Sombra)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a segunda cor de uma sombra. Leitura/gravação. **VgColor**.

**Aplica-se a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxe de marca**

<v: *elemento* color2=" *expressão* ">

**Sintaxe do script**

*elemento* .color2="*expression*"

*expressão* = *elemento*.color2

**Comentários**

Use uma segunda cor para criar efeitos de sombra especiais. Consulte o [atributo Type](type-attribute--shadow--vml.md) para obter mais informações sobre as segundas cores.

*Atributo padrão VML*

**Exemplo**

A sombra tem azul para uma segunda cor.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green" color2="blue"/>
   </v:shape>
```



 

 