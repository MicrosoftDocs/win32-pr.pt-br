---
title: Atributo alt da VML
description: Atributo alt da VML
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b420d556e69ed2f987a3a3b10a5709f926dc5c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162391"
---
# <a name="vml-alt-attribute"></a>Atributo alt da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o texto alternativo a ser exibido em vez de um elemento gráfico. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* Alt = " *expressão* " >

**Sintaxe do script**

*Element* . Alt = "*expressão*"

*expressão* = de *elemento*. Alt

**Comentários**

O atributo **ALT** é semelhante ao atributo HTML **ALT** padrão. Esse atributo fornece uma maneira para os navegadores que convertem texto em fala para descrever elementos gráficos em uma página.

*Atributo padrão da VML*

**Consulte também**

[Forma](shape-element--vml.md)

**Exemplo**

O elemento **ALT** abaixo exibirá a frase "retângulo vermelho" em navegadores que convertem páginas da Web em frases faladas.


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemplo do atributo ALT](/previous-versions/bb229663(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 