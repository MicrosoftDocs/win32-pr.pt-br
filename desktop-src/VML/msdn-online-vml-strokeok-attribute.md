---
title: Atributo StrokeOK de VML
description: Atributo StrokeOK de VML
ms.assetid: f150f87b-1ed9-4c53-bf7f-ebe1e81642fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a2875e3e6e8374238340ff2a596852e5ebce7c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917514"
---
# <a name="vml-strokeok-attribute"></a>Atributo StrokeOK de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se um traço será exibido. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *Element* strokeok = " *expressão* " >

**Sintaxe do script**

*Element* . strokeok = "*expressão*"

*expressão* = de *elemento*. strokeok

**Comentários**

Se **for false**, o caminho não poderá ser traçado. O padrão é **True**. Esse atributo substitui todos os outros atributos de traço no elemento pai ou **Stroke** .

*Atributo padrão da VML*

**Exemplo**

O caminho não será traçado.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" strokeok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 