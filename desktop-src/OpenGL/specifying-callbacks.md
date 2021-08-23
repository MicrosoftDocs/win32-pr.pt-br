---
title: Especificando retornos de chamada
description: Você pode especificar até cinco funções de retorno de chamada para um mosaico.
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- Utilitário OpenGL (GLU), especificando funções de retorno de chamada
- GLU (Utilitário OpenGL), especificando funções de retorno de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e57a5f961a980f20451f594fa59885eda99d1e2de94a55fbfd2abd4b8301b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553776"
---
# <a name="specifying-callbacks"></a>Especificando retornos de chamada

Você pode especificar até cinco funções de retorno de chamada para um mosaico. As funções que você não especificar não serão chamadas durante o mosaico e você não obterá nenhuma informação que possa ter retornado. Especifique as funções de retorno de chamada [*com gluTessCallback*](glutess.md).

A **função gluTessCallback** associa a função de retorno de chamada *fn* ao objeto de mosaico *tessobj*. O tipo do retorno de chamada é determinado pelo tipo de parâmetro *,* que pode ser **GLU \_ BEGIN,** **GLU EDGE \_ \_ FLAG**, **GLU \_ VERTEX**, **GLU \_ END** ou **GLU \_ ERROR**. As cinco funções de retorno de chamada possíveis têm os seguintes protótipos.



| Função de retorno de chamada   | Protótipo                                    |
|---------------------|----------------------------------------------|
| **GLU \_ BEGIN**      | **void** **begin**(**tipo GLenum**_);_       |
| **SINALIZADOR GLU \_ EDGE \_** | **void** **edgeFlag**(**sinalizador GLboolean**_);_ |
| **GLU \_ VÉRTICE**     |  **vértice** void (**void \* ***data* );     |
| **GLU \_ END**        | **void** **end**( *void* );                  |
| **ERRO DE GLU \_**      | **erro** **void**(**GLenum**_errno_ );      |



 

Para alterar uma função de retorno de chamada, chame [*gluTessCallback*](glutess.md) com a nova função. Para eliminar uma função de retorno de chamada sem substituí-la por uma nova, passe **gluTessCallback** um ponteiro nulo para a função apropriada.

À medida que o mosaico prossegue, as funções de retorno de chamada são chamadas de maneira semelhante à maneira como você usaria as funções OpenGL [**glBegin,**](glbegin.md) [glEdgeFlag,](gledgeflag-functions.md) [glVertex](glvertex-functions.md)e [**glEnd.**](glend.md)

A função de retorno de chamada **GLU \_ BEGIN** é invocada com um dos três parâmetros possíveis:

-   VENTILADOR \_ DE TRIÂNGULO \_ GL
-   FAIXA \_ DE TRIÂNGULO \_ GL
-   TRIÂNGULOS \_ GL

Depois de chamar a função de retorno de chamada **GLU \_ BEGIN** e antes de chamar a função de retorno de chamada associada a **GLU \_ END,** alguma combinação dos retornos de chamada **GLU EDGE \_ \_ FLAG** e **GLU \_ VERTEX** é invocada. Os vértices e sinalizadores de borda associados são interpretados exatamente como estão no OpenGL entre **glBegin**(GL \_ TRIANGLE \_ FAN), **glBegin**(GL TRIANGLE STRIP) ou \_ \_ **glBegin**(GL TRIANGLES ) e o \_ **glEnd correspondente.**

Como os sinalizadores de borda não fazem sentido em um ventilador de triângulo ou uma faixa de triângulo, se houver uma função de retorno de chamada associada ao SINALIZADOR DE BORDA GLU , o retorno de chamada **GLU \_ BEGIN** será chamado somente com **GL \_ TRIANGLES**. **\_ \_** A função de retorno de chamada **\_ GLU EDGE \_ FLAG** funciona de forma análoga à função [GlEdgeFlag](gledgeflag-functions.md) do OpenGL.

Se houver um erro durante o mosaico, a função de retorno de chamada de erro será invocada. A função de retorno de chamada de erro é passada com um número de erro GLU. Você pode obter uma cadeia de caracteres que descreve o erro com a [**função gluErrorString.**](gluerrorstring.md)

 

 




