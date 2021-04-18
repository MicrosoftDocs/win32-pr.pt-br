---
title: Atributo userhidden da VML
description: Atributo userhidden da VML
ms.assetid: 0e4616c7-a456-4157-b77a-56cd289e913c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 519857d53cbec985afae31a5e7dea8811773dc43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105789619"
---
# <a name="vml-userhidden-attribute"></a>Atributo userhidden da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se uma âncora de script está oculta. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* o:userhidden = " *expressão* " >

**Comentários**

O padrão é **False**. Se **for true**, as âncoras de script permanecerão ocultas mesmo se a forma estiver visível.

*Atributo de extensões de Microsoft Office*

**Exemplo**

A âncora do script da forma está oculta.


```HTML
   <v:rect id=myrect fillcolor="red" userhidden="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 