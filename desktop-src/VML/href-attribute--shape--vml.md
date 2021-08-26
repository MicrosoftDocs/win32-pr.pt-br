---
title: Atributo HRef (Forma)(VML)
description: Atributo HRef (Forma)(VML)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe4b545aa27d311b0e1d0c73f0107aa6fdb357d524d3150ce6ab7dfb1e0f009
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072036"
---
# <a name="href-attribute-shapevml"></a>Atributo HRef (Forma)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define uma URL para uma forma. Quando a forma for clicada, o navegador carregará a URL. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* href=" *expressão* ">

**Sintaxe do script**

*element* .href="*expression*"

*expressão* = *elemento*.href

**Comentários**

O **atributo HRef** é semelhante ao atributo **HRef** HTML padrão de âncoras.

O **uso de HRef** facilita a criação de botões interessantes em uma página da Web.

*Atributo padrão VML*

**Exemplo**

Quando o retângulo for clicado, o navegador carregará o Microsoft Corporation home page.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



[Exemplo de atributo HRef](/previous-versions/bb229672(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 