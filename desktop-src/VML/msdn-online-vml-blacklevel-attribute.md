---
title: Atributo BlackLevel de VML
description: Atributo BlackLevel de VML
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe31c9507468efd27aac9d9729a4f2ee3ddce449398b4a68bd7d79b2d029b8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057904"
---
# <a name="vml-blacklevel-attribute"></a>Atributo BlackLevel de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define a intensidade de preto em uma imagem. Leitura/gravação. **VgNumber**.

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *Element* blacklevel = " *expressão* " >

**Sintaxe do script**

*Element* . blacklevel = "*expressão*"

*expressão* = de *elemento*. blacklevel

**Comentários**

Permite que o nível de cor seja modificado para que os pretos apareçam como verdadeiros pretos e todas as outras cores fiquem visíveis como sombras acima do preto. O valor padrão é 0. Embora qualquer número entre o infinito positivo e negativo seja permitido, valores menores que-0,5 serão exibidos como todos os pretos e valores maiores que 0,5 serão exibidos como todos os brancos.

*Atributo padrão da VML*

**Exemplo**

A imagem será exibida com tons muito escuros.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 