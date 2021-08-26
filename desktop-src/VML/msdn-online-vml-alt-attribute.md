---
title: Atributo Alt do VML
description: Atributo Alt do VML
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08714efca9a390cbbec2f3dcf14782053d34db3506462214b9e62ebf1da206a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905336"
---
# <a name="vml-alt-attribute"></a>Atributo Alt do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o texto alternativo a ser exibido em vez de um gráfico. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* alt=" *expressão* ">

**Sintaxe do script**

*elemento* .alt="*expressão*"

*expressão* = *elemento*.alt

**Comentários**

O **atributo Alt** é semelhante ao atributo HTML **Alt** padrão. Esse atributo fornece uma maneira para navegadores que convertem texto em fala para descrever elementos gráficos em uma página.

*Atributo padrão VML*

**Consulte também**

[Forma](shape-element--vml.md)

**Exemplo**

O **elemento Alt** abaixo exibirá a frase "Retângulo vermelho" em navegadores que convertem páginas da Web em frases faladas.


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemplo de atributo Alt](/previous-versions/bb229663(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 