---
title: Atributo ArrowOK do VML
description: Atributo ArrowOK do VML
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95b8fa7068f55246263e6622527a8ecec17d3351c284a0810cd77b085784aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124965"
---
# <a name="vml-arrowok-attribute"></a>Atributo ArrowOK do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se as setas serão exibidas. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *elemento* arrowok=" *expressão* ">

**Sintaxe do script**

*elemento* .arrowok="*expression*"

*expressão* = *elemento*.arrowok

**Comentários**

Se **False**, o caminho não terá setas. O padrão é **False**. Esse atributo substitui todos os outros atributos de ponta de seta no elemento pai **ou Traço.**

*Atributo padrão VML*

**Exemplo**

O caminho não terá uma ponta de seta.


```HTML
   <v:line id="whatsmyline"
   style="position:relative"
   from="114pt,66pt" to="402pt,66pt"
   strokecolor="black">
   <v:stroke startarrow="block" endarrow="block"/>
   <v:path arrowok="False"/>
   </v:line>
```



 

 