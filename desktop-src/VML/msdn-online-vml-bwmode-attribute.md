---
title: Atributo BWMode de VML
description: Atributo BWMode de VML
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f595159398e32fdb1c80ad5d949ef48758aea95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641348"
---
# <a name="vml-bwmode-attribute"></a>Atributo BWMode de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina como uma forma será renderizada para dispositivos de saída em preto e branco. Leitura/gravação. [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* o:bwmode = " *expressão* " >

**Comentários**

Quando uma forma é impressa em uma impressora preto e branco ou exibida em uma exibição em preto e branco em um aplicativo, várias opções são possíveis. Para obter mais informações sobre os valores desse atributo, consulte o tópico [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) . O valor padrão é **auto**.

Se **auto** for especificado, [BWNormal](msdn-online-vml-bwnormal-attribute.md) será usado para determinar o comportamento para saída normal de preto e branco, e [BWPure](msdn-online-vml-bwpure-attribute.md) será usado para determinar o comportamento de saída puro de preto e branco.

*Atributo de extensões de Microsoft Office*

**Exemplo**

O modo preto e branco da forma é **automático**.


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 