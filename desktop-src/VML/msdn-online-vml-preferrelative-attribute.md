---
title: Atributo PreferRelative de VML
description: Atributo PreferRelative de VML
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154297a528f18a3ac53f788ebbfe80ff59196f2872dd3dcb3789db16d5c91cb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654976"
---
# <a name="vml-preferrelative-attribute"></a>Atributo PreferRelative de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Determina se o tamanho original de um objeto é salvo após a reformatação. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* o:preferrelative = " *expressão* " >

**Comentários**

O padrão é **False**. Se **for true**, o tamanho original do objeto será armazenado e todo o redimensionamento será baseado em uma porcentagem desse tamanho original. Caso contrário, cada redimensionamento redefinirá a escala para 100%.

*Microsoft Office Atributo de extensões*

**Exemplo**

Se a forma for redimensionada, o tamanho original não será armazenado.


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 