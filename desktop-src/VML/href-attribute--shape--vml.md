---
title: Atributo HRef (forma) (VML)
description: Atributo HRef (forma) (VML)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ecbc0f97ca2fb9c1565b712d3677d007a62b035
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008074"
---
# <a name="href-attribute-shapevml"></a>Atributo HRef (forma) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma URL para uma forma. Quando a forma é clicada, o navegador carregará a URL. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* href = " *expressão* " >

**Sintaxe do script**

*Element* . href = "*expressão*"

*expressão* = de *Element*. href

**Comentários**

O atributo **href** é semelhante ao atributo HTML **href** padrão de âncoras.

Usar **href** torna mais fácil criar botões interessantes em uma página da Web.

*Atributo padrão da VML*

**Exemplo**

Quando o retângulo for clicado, o navegador carregará o home page da Microsoft Corporation.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



[Exemplo de atributo href](/previous-versions/bb229672(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 