---
title: Atributo StrokeOK do VML
description: Atributo StrokeOK do VML
ms.assetid: f150f87b-1ed9-4c53-bf7f-ebe1e81642fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5051f3a2d5e7ac8e4d509d8b8f65182f86799db41bbd8a4d71741961c3a1e406
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475216"
---
# <a name="vml-strokeok-attribute"></a>Atributo StrokeOK do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se um traço será exibido. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *elemento* strokeok=" *expressão* ">

**Sintaxe do script**

*expressão element* .strokeok=""

*expressão* = *elemento*.strokeok

**Comentários**

Se **False**, o caminho não poderá ser traço. O padrão é **True**. Esse atributo substitui todos os outros atributos de traço no elemento pai **ou Traço.**

*Atributo padrão VML*

**Exemplo**

O caminho não será traço.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" strokeok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 