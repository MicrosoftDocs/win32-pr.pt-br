---
title: Atributo DashStyle de VML
description: Atributo DashStyle de VML
ms.assetid: 7d6c7cbf-9ccc-4117-af0a-ca8f36684f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4651af9ade605166121c7225925e3bf1ed8264ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294120"
---
# <a name="vml-dashstyle-attribute"></a>Atributo DashStyle de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica o padrão de ponto e tracejado para um traço. Leitura/gravação. **VgLineDashStyle**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *Element* DashStyle = " *expressão* " >

**Sintaxe do script**

*Element* . DashStyle = "*expressão*"

*expressão* = de *elemento*. DashStyle

**Comentários**

Os valores são:

-   Solid (padrão)
-   ShortDash
-   ShortDot
-   ShortDashDot
-   ShortDashDotDot
-   Ponto
-   Traço
-   LongDash
-   DashDot
-   LongDashDot
-   LongDashDotDot

O atributo **DashStyle** permite que o usuário especifique um padrão de traço definido por personalizado. Isso é feito usando uma série de números. Os estilos de traço são definidos em termos do comprimento do traço (a parte desenhada do traço) e o comprimento do espaço entre os traços. Os comprimentos são relativos à largura da linha: um comprimento de "1" é igual à largura da linha. O estilo **EndCap** é aplicado a cada Dash, o estilo de seta não é. A cadeia de caracteres define primeiro o comprimento do traço em seguida, o comprimento do espaço. Isso pode ser repetido para formar estilos de traço complexos. A cadeia de caracteres sempre deve conter um par de números; Se ele contiver um número ímpar de números, o último pode ser desconsiderado.

A tabela a seguir lista alguns valores típicos e uma descrição do efeito pretendido. "0" implica um ponto que deve ser consta simétrico (com Caps de extremidade arredondado deve ser um círculo). Se a ponta de extremidade de linha for "simples", um visualizador deverá escolher um sistema operacional interno, onde for possível (em outras palavras. algo que é rápido de desenhar.). A tabela a seguir mostra alguns exemplos.



| DashStyle     | Descrição                                                                                          |
|---------------|------------------------------------------------------------------------------------------------------|
| "2 2"         | Traços curtos. Cada traço e o espaço entre o é o dobro da largura da linha.                        |
| "0 2"         | Pontilha. O espaço entre é duas vezes a largura da linha.                                                  |
| "2 2 0 2"     | Traço curto ponto.                                                                                      |
| "2 2 0 2 0 2" | Traço ponto curto ponto.                                                                                  |
| "1 2"         | Final. Cada traço é a largura da linha, enquanto cada espaço é o dobro da largura da linha.            |
| "4 2"         | Dash. Cada traço é quatro vezes a largura da linha, enquanto cada espaço é o dobro da largura da linha. |
| "8 2"         | Tracejado longo.                                                                                           |
| "4 2 1 2"     | Traço ponto.                                                                                            |
| "8 2 1 2"     | Ponto de tracejado longo.                                                                                       |
| "8 2 1 2 1 2" | Ponto longo de ponto pontilhado.                                                                                   |



 

*Atributo padrão da VML*

**Exemplo**

A forma tem um estilo tracejado de traços e pontilhados alternados.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200,200, 200,1 x e">
   <v:stroke dashstyle="dashdot"/>
   </v:shape>
```



 

 