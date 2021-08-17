---
title: Elemento de curva de VML
description: Elemento de curva de VML
ms.assetid: 37197ef0-7597-465a-bc37-7ffcde2e736b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fd06480b0d4bcf062f1f64eb9fa0b22862cf2b338b2c2f5ea0bf1c3cd2a1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655526"
---
# <a name="vml-curve-element"></a>Elemento de curva de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Forma de curva predefinida.

A **curva** usa os atributos [para](to-attribute--curve--vml.md), [de](from-attribute--curve--vml.md), [Control1](msdn-online-vml-control1-attribute.md)e [Control2](msdn-online-vml-control2-attribute.md) .

Veja a seguir o código mínimo necessário para produzir uma imagem.


```HTML
   <v:curve
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```





 

 