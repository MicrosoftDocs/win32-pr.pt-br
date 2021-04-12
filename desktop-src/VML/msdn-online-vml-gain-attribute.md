---
title: Atributo de obter VML
description: Atributo de obter VML
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5675503def2f48d4c5fbf7154f0d0d05b2fe417d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366368"
---
# <a name="vml-gain-attribute"></a>Atributo de obter VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a intensidade de todas as cores em uma imagem. Leitura/gravação. **VgNumber**.

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *Element* saiba = " *expression* " >

**Sintaxe do script**

*Element* . obter = "*expressão*"

*expressão* = de *elemento*. obter

**Comentários**

Esse atributo define a claridade da cor branca, afetando todas as outras cores. Os valores variam de 0 a infinito. O valor padrão é 1.0. Um valor de 0 não exibe nenhuma imagem. Valores maiores que 1 claream a imagem e os valores menores que 1 fazem com que a imagem pareça Grayer.

Esse atributo pode ser usado para criar efeitos interessantes.

*Atributo padrão da VML*

**Exemplo**

A imagem será exibida com todas as cores que tendem a ficar cinza.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 