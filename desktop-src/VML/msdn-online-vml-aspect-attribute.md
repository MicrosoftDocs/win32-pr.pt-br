---
title: Atributo de aspecto da VML
description: Atributo de aspecto da VML
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f7cf666e9bb8d4bf3cfe0e47190a8127415ac1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641358"
---
# <a name="vml-aspect-attribute"></a>Atributo de aspecto da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica como a taxa de proporção da imagem de preenchimento será preservada. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *Element* aspecto = " *expression* " >

**Sintaxe do script**

*elemento* . Aspect = "*expressão*"

*expressão* = de *elemento*. Aspect

**Comentários**

Os valores são:



| Valor   | Descrição                           |
|---------|---------------------------------------|
| ignore  | Ignorar problemas de aspecto. Padrão.        |
| mínimo | A imagem é pelo menos tão grande quanto o **tamanho**. |
| atmost  | A imagem não é maior que o **tamanho**.     |



 

*Atributo padrão da VML*

**Exemplo**

A imagem que compõe o preenchimento é maior ou igual a um tamanho de 10 pontos em 10 pontos.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 