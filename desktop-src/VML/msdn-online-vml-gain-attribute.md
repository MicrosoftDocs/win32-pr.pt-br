---
title: Atributo de ganho de VML
description: Atributo de ganho de VML
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7b72f1588608f4988731111583e758b0207080eb3e02768a45b58c39071b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057824"
---
# <a name="vml-gain-attribute"></a>Atributo de ganho de VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a intensidade de todas as cores em uma imagem. Leitura/gravação. **VgNumber.**

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *elemento* gain=" *expressão* ">

**Sintaxe do script**

*element* .gain="*expression*"

*expressão* = *elemento*.gain

**Comentários**

Esse atributo define o brilho da cor branca, afetando todas as outras cores. Os valores variam de 0 a infinito. O valor padrão é 1.0. Um valor de 0 não exibe nenhuma imagem. Valores maiores que 1 aliviam a imagem e valores menores que 1 fazem com que a imagem pareça mais cinza.

Esse atributo pode ser usado para criar efeitos interessantes.

*Atributo padrão VML*

**Exemplo**

A imagem será exibida com todas as cores tendendo para cinza.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 