---
title: Atributo Color2 (sombra) (VML)
description: Atributo Color2 (sombra) (VML)
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e735d7672457153881d384c7b625199cf4a202e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641573"
---
# <a name="color2-attribute-shadowvml"></a>Atributo Color2 (sombra) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a segunda cor de uma sombra. Leitura/gravação. **VgColor**.

**Aplica-se a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxe de marca**

<v: *Element* color2 = " *expressão* " >

**Sintaxe do script**

*Element* . color2 = "*expressão*"

*expressão* = de *elemento*. color2

**Comentários**

Use uma segunda cor para criar efeitos de sombra especiais. Consulte o atributo [Type](type-attribute--shadow--vml.md) para obter mais informações sobre as segundas cores.

*Atributo padrão da VML*

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



 

 