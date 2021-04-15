---
title: Especificando retornos de chamada
description: Você pode especificar até cinco funções de retorno de chamada para um mosaico.
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- Utilitário OpenGL (GLU), especificando funções de retorno de chamada
- GLU (utilitário OpenGL), especificando funções de retorno de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6086448cf6f4a71ea6a49359d5656f12f613d760
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498791"
---
# <a name="specifying-callbacks"></a>Especificando retornos de chamada

Você pode especificar até cinco funções de retorno de chamada para um mosaico. Qualquer função que você não especificar não será chamada durante o mosaico e você não obterá nenhuma informação que possa ter retornado. Você especifica as funções de retorno de chamada com [*gluTessCallback*](glutess.md).

A função **gluTessCallback** associa a função de retorno de chamada *FN* com o objeto de mosaico *tessobj*. O tipo de retorno de chamada é determinado pelo *tipo* de parâmetro, que pode **ser \_ Glu Begin**, **Glu \_ \_ flag de borda**, **Glu \_ Vertex**, **Glu \_ end** ou **Glu \_ Error**. As cinco funções de retorno de chamada possíveis têm os seguintes protótipos.



| Função de retorno de chamada   | Protótipo                                    |
|---------------------|----------------------------------------------|
| **início do GLU \_**      | **void** **begin**(**GLenum * * * Type* );       |
| **\_sinalizador de borda Glu \_** | **void** **EdgeFlag**(**GLboolean * * * sinalizador* ); |
| **\_vértice Glu**     |  **vértice** nulo (**void \* * * * dados* );     |
| **GLU \_ fim**        | **anular** **término**( *void* );                  |
| **erro de GLU \_**      |  **erro** de void (**GLenum * * * errno* );      |



 

Para alterar uma função de retorno de chamada, chame [*gluTessCallback*](glutess.md) com a nova função. Para eliminar uma função de retorno de chamada sem substituí-la por uma nova, passe **gluTessCallback** um ponteiro nulo para a função apropriada.

Como o mosaico prossegue, as funções de retorno de chamada são chamadas de forma semelhante à forma como você usaria as funções OpenGL [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md)e [**glEnd**](glend.md).

A função de retorno de chamada **Glu \_ begin** é invocada com um dos três parâmetros possíveis:

-   \_ \_ ventilador do triângulo GL
-   \_faixa de triângulo GL \_
-   \_TRIângulos GL

Depois de chamar a função de retorno de chamada **Glu \_ begin** e antes de chamar a função de retorno de chamada associada ao **\_ término de Glu**, uma combinação do **\_ \_ sinalizador de borda Glu** e retornos de chamada de **\_ vértice Glu** é invocada. Os vértices associados e os sinalizadores de borda são interpretados exatamente como estão no OpenGL entre **glBegin**( \_ \_ ventilador do triângulo GL), **glBegin**(faixa de \_ triângulo GL \_ ) ou **glBegin**( \_ triângulos GL **)** e **glEnd** correspondentes.

Como os sinalizadores de borda não fazem sentido em um ventilador de triângulo ou em uma faixa de triângulo, se houver uma função de retorno de chamada associada ao **\_ \_ sinalizador de borda Glu**, o retorno de chamada de **Glu \_ começar** será chamado apenas com **\_ triângulos GL**. A função de retorno de chamada do **\_ \_ sinalizador de borda Glu** funciona de forma análoga com a função [glEdgeFlag](gledgeflag-functions.md) do OpenGL.

Se houver um erro durante o mosaico, a função de retorno de chamada de erro será invocada. A função de retorno de chamada de erro recebe um número de erro GLU. Você pode obter uma cadeia de caracteres que descreve o erro com a função [**gluErrorString**](gluerrorstring.md) .

 

 




