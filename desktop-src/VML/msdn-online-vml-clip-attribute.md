---
title: Atributo de clipe da VML
description: Atributo de clipe da VML
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2702355ea93d8e87d173ee4c23406b12557dce4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105763436"
---
# <a name="vml-clip-attribute"></a>Atributo de clipe da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se o recorte está ativado. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxe de marca**

<v: *elemento* clip = " *expression* " >

**Sintaxe do script**

*Element* . Clip = "*expressão*"

*expressão* = de *elemento*. clip

**Comentários**

Se **clip** for **false**, a forma será dimensionada para caber no quadro. Se **for true**, qualquer parte da forma que estiver fora do quadro não será exibida.

Observe que a [origem](origin-attribute--vmlframe--vml.md) e o [tamanho](size-attribute--vmlframe.md) não serão usados, a menos que o **clipe** seja **verdadeiro**.

*Atributo padrão da VML*

**Exemplo**

A imagem definida no arquivo externo será recortada.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 