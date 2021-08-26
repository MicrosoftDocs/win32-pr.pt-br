---
title: Atributo UserHidden do VML
description: Atributo UserHidden do VML
ms.assetid: 0e4616c7-a456-4157-b77a-56cd289e913c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb49b54c2463769286d11877e992bb30d4e431f351e39bf30b0ed6ab748a58e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959226"
---
# <a name="vml-userhidden-attribute"></a>Atributo UserHidden do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se uma âncora de script está oculta. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* o:userhidden=" *expressão* ">

**Comentários**

O padrão é **False**. Se **True**, as âncoras de script permanecerão ocultas mesmo se a forma estiver visível de outra forma.

*Microsoft Office Atributo Extensions*

**Exemplo**

A âncora de script da forma está oculta.


```HTML
   <v:rect id=myrect fillcolor="red" userhidden="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 