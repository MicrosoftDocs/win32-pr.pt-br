---
title: Atributo VML Eqn
description: Atributo VML Eqn
ms.assetid: b2c41bad-2f83-4280-9441-33206d8dc1b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae5872c29064f24a10b4a12c0d0e2a4ca4a200f79e295d60713fe56355f23aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655446"
---
# <a name="vml-eqn-attribute"></a>Atributo VML Eqn

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a equação usada por uma fórmula. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[F](msdn-online-vml-f-element.md) (subelemento de [fórmulas](msdn-online-vml-formulas-element.md))

**Sintaxe de marca**

<v: *elemento* eqn=" *expressão* ">

**Sintaxe do script**

*element* .eqn="*expression*"

*expressão* = *elemento*.eqn

**Comentários**

As equações são definidas pela avaliação de uma expressão de texto que tem a forma geral de uma operação seguida por até três argumentos. Cada argumento pode ser dos seguintes tipos:

-   ajuste (por exemplo, \# 2)
-   outra fórmula (por exemplo, @2 )
-   números fixos (por exemplo, 2)
-   valores predefinidos

A tabela a seguir define as fórmulas que podem ser usadas com os argumentos opcionais, considerando os nomes *v*, *p1* e *p2*. O padrão de fórmula é:

<f eqn=" *operation* \[*v* \] \[*p1* \] \[*p2* \]"/>



| Operação | Params | Exato  | Result                    | Descrição                                                                    |
|-----------|--------|--------|---------------------------|--------------------------------------------------------------------------------|
| Val       | 1      | sim    | v                         | Define um valor de guia de algum outro valor.                                   |
| Sum       | 3      | sim    | v + p1 – p2               | Usado para adição e subtração.                                             |
| product   | 3      | Rodadas | v \* p1 /p2              | Usado para multiplicação e divisão.                                          |
| mid       | 2      | (c)    | (v + p1)/ 2               | Média.                                                                       |
| abs       | 1      | sim    | abs(v)                    | Valor absoluto.                                                                |
| min       | 2      | sim    | min(v,p1)                 | O valor menor de v e p1.                                                  |
| max       | 2      | sim    | max(v,p1)                 | O valor maior de v e p1.                                                 |
| if        | 3      | sim    | v > 0 ? p1 : p2        | Teste condicional.                                                           |
| mod       | 3      | não     | sqrt(v^2 + p1^2 + p2^2)   | Valor de módulo.                                                                 |
| atan2     | 2      | não     | atan2(p1,v)               | Valor polar em graus \* 2^16 (unidades fd).                                     |
| sin       | 2      | não     | v \* sin(p1)              | Sin, argumento em graus \* 2^16 (unidades fd ). [](msdn-online-vml-units.md)     |
| cos       | 2      | não     | v \* cos(p1)              | Cos, argumento em graus \* 2^16 (unidades fd ). [](msdn-online-vml-units.md)     |
| cosatan2  | 3      | não     | v \* cos(atan2(p2,p1))    | Preserva a precisão total no cálculo intermediário.                           |
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



 

