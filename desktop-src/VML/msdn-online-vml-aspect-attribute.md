---
title: Atributo de aspecto da VML
description: Atributo de aspecto da VML
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669b0f93e740e6bc4d4fb94155f6ca0ab60d5e00cebfb1604d5272d45d4dd8ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602893"
---
# <a name="vml-aspect-attribute"></a>Atributo de aspecto da VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

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



 

 