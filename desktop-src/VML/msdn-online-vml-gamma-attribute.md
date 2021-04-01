---
title: Atributo gama da VML
description: Atributo gama da VML
ms.assetid: 47a4d10e-f5ef-457b-92dd-bce5dae59b1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b74c80739d694038601588eee4c8ad7ed90923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084711"
---
# <a name="vml-gamma-attribute"></a>Atributo gama da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a quantidade de contraste para uma imagem. Leitura/gravação. **VgNumber**.

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *Element* gama = " *expression* " >

**Sintaxe do script**

*Element* . gama = "*expressão*"

*expressão* = de *elemento*. gama

**Comentários**

Diminuir o gama abaixo 1 modifica uma imagem para torná-la mais contrastantivo, enquanto valores maiores que 1 diminuem o contraste. Os valores úteis são de 0,3 a aproximadamente 3. O valor padrão é 0.

*Atributo padrão da VML*

**Exemplo**


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gamma=".7" src="gamera.jpg"/>
   </v:shape>
```



 

 