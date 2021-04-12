---
title: Atributo ArrowOK de VML
description: Atributo ArrowOK de VML
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8807b802370f81ddd084df8a171f95e8496c7ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366242"
---
# <a name="vml-arrowok-attribute"></a>Atributo ArrowOK de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se as pontas de seta serão exibidas. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *Element* arrowok = " *expressão* " >

**Sintaxe do script**

*Element* . arrowok = "*expressão*"

*expressão* = de *elemento*. arrowok

**Comentários**

Se **for false**, o caminho não terá pontas de seta. O padrão é **False**. Esse atributo substitui todos os outros atributos de ponta de seta no elemento pai ou **Stroke** .

*Atributo padrão da VML*

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



 

 