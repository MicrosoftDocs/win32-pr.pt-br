---
title: Atributo BWMode VML
description: Atributo BWMode VML
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5640680af40f4649f7ab34b2ec8cfd4e5cf94ee4c7c6ce3c3f2185e68bdac360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754961"
---
# <a name="vml-bwmode-attribute"></a>Atributo BWMode VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina como uma forma será renderizar para dispositivos de saída em preto e branco. Leitura/gravação. [VgBlackWhiteMode.](msdn-online-vml-vgblackwhitemode.md)

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* o:bwmode=" *expressão* ">

**Comentários**

Quando uma forma é impressa em uma impressora em preto e branco ou exibida em uma exibição em preto e branco em um aplicativo, várias opções são possíveis. Para obter mais informações sobre os valores desse atributo, consulte o [tópico VgBlackWhiteMode.](msdn-online-vml-vgblackwhitemode.md) O valor padrão é **auto.**

Se **auto** for especificado, [BWNormal](msdn-online-vml-bwnormal-attribute.md) será usado para determinar o comportamento da saída normal em preto e branco e [BWPure](msdn-online-vml-bwpure-attribute.md) será usado para determinar o comportamento da saída em preto e branco puro.

*Microsoft Office Atributo Extensions*

**Exemplo**

O modo preto e branco da forma é **automático.**


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 