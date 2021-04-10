---
title: Atributo eqn de VML
description: Atributo eqn de VML
ms.assetid: b2c41bad-2f83-4280-9441-33206d8dc1b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da00084a825147c6f8a05f503e5ee2679f40e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294486"
---
# <a name="vml-eqn-attribute"></a>Atributo eqn de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a equação usada por uma fórmula. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[F](msdn-online-vml-f-element.md) (subelemento de [fórmulas](msdn-online-vml-formulas-element.md))

**Sintaxe de marca**

<v: *Element* eqn = " *expressão* " >

**Sintaxe do script**

*Element* . eqn = "*expressão*"

*expressão* = de *elemento*. eqn

**Comentários**

As equações são definidas pela avaliação de uma expressão de texto que tem a forma geral de uma operação seguida por até três argumentos. Cada argumento pode ser dos seguintes tipos:

-   ajuste (por exemplo, \# 2)
-   outra fórmula (por exemplo, @2 )
-   números fixos (por exemplo, 2)
-   valores predefinidos

A tabela a seguir define as fórmulas que podem ser usadas com os argumentos opcionais de acordo com os nomes *v*, *P1* e *P2*. O padrão de fórmula é:

<f eqn=" *operation* \[*v* \] \[*p1* \] \[*p2* \]"/>



| Operação | Params | Exato  | Result                    | Descrição                                                                    |
|-----------|--------|--------|---------------------------|--------------------------------------------------------------------------------|
| Val       | 1      | sim    | v                         | Define um valor de guia de algum outro valor.                                   |
| Sum       | 3      | sim    | v + P1-P2               | Usado para adição e subtração.                                             |
| product   | 3      | Arredonda | v \* P1/P2              | Usado para multiplicação e divisão.                                          |
| mid       | 2      | &    | (v + P1)/2               | Média.                                                                       |
| abs       | 1      | sim    | ABS (v)                    | Valor absoluto.                                                                |
| min       | 2      | sim    | mín. (v, P1)                 | O menor valor de v e P1.                                                  |
| max       | 2      | sim    | Max (v, P1)                 | O maior valor de v e P1.                                                 |
| if        | 3      | sim    | v > 0? P1: P2        | Teste condicional.                                                           |
| mod       | 3      | não     | sqrt (v ^ 2 + P1 ^ 2 + P2 ^ 2)   | Valor do módulo.                                                                 |
| atan2     | 2      | não     | atan2 (P1, v)               | Valor do polar em graus \* 2 ^ 16 (unidades FD).                                     |
| sin       | 2      | não     | v \* sin (P1)              | Sin, argumento em graus \* 2 ^ 16 ( [unidades](msdn-online-vml-units.md) FD).     |
| cos       | 2      | não     | v \* cos (P1)              | Cos, argumento em graus \* 2 ^ 16 ( [unidades](msdn-online-vml-units.md) FD).     |
| cosatan2  | 3      | não     | v \* cos (ATAN2 (P2, P1))    | Preserva a precisão total no cálculo intermediário.                           |
| sinatan2  | 3      | não     | v \* sin (ATAN2 (P2, P1))    | Preserva a precisão total no cálculo intermediário.                           |
| sqrt      | 1      | não     | sqrt (v)                   | O resultado é positivo e arredonda para baixo.                                            |
| sumangle  | 3      | sim    | v + P1 \* 2 ^ 16 + P2 \* 2 ^ 16 | v dimensionado por 2 ^ 16; P1 e P2 são graus.<br/>                            |
| ellipse   | 3      | não     | P2 \* sqrt (1-(v/P1) ^ 2)    | Elipse.                                                                       |
| tan       | 2      | não     | v \* tan (P1)              | Tangente, argumento em graus \* 2 ^ 16 ( [unidades](msdn-online-vml-units.md) FD). |



 

Observe que a equação consiste apenas em operações e números; os símbolos matemáticos são omitidos. Por exemplo, a equação

eqn = "Sum 5 9 3"

produziria o equivalente de

5 + 9-3

para o valor retornado de 11. Se os operandos estiverem ausentes, o valor não será usado. Por exemplo,

eqn = "Sum 5 9"

produziria o equivalente de

5 + 9

e ignoraria o operando ausente.

*Atributo padrão da VML*

**Exemplo**

A fórmula a seguir produziria um resultado de 6 (a soma dos dois números dividido por 2), que, se esta fosse a primeira fórmula, poderia ser recuperada pelo símbolo " @0 ".


```HTML
    <v:f eqn="mid 5 7"/>
```



 

