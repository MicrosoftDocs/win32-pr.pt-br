---
title: Comandos de limpeza de buffer e tela de portação
description: O OpenGL substitui uma variedade de funções claras iris GL (como zclear, aclear, esclear e assim por diante) por uma única função, glClear. Especifique exatamente o que você deseja limpar passando máscaras para glClear.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- Portação IRIS GL, funções clear
- portando de IRIS GL, funções clear
- portando para OpenGL de IRIS GL, funções clear
- Portação openGL de IRIS GL, funções clear
- funções clear
- Portação IRIS GL, comandos de limpeza de tela
- portando do IRIS GL, comandos de limpeza de tela
- portando para OpenGL do IRIS GL, comandos de limpeza de tela
- Portação openGL do IRIS GL, comandos de limpeza de tela
- comandos de limpeza de tela
- Portação IRIS GL, comandos de limpeza de buffer
- portando do IRIS GL, comandos de limpeza de buffer
- portando para OpenGL do IRIS GL, comandos de limpeza de buffer
- Portação openGL do IRIS GL, comandos de limpeza de buffer
- comandos de limpeza de buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbff0fed3472fd4374605cb96dbae845998c0ba2d8ce488420f9b4c6895a07c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794871"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a>Comandos de limpeza de buffer e tela de portação

O OpenGL substitui uma variedade de funções claras **iris** GL (como **zclear,** **aclear,** **esclear** e assim por diante) por uma única função, [**glClear**](glclear.md). Especifique exatamente o que você deseja limpar passando máscaras para **glClear.**

Lembre-se dos seguintes pontos ao portar comandos de tela e buffer:

-   O OpenGL mantém as cores de limpeza separadamente das cores de desenho, com chamadas como [**glClearColor**](glclearcolor.md) e [**glClearIndex.**](glclearindex.md) Certifique-se de definir a cor clara para cada buffer antes de limpar.
-   Em vez de usar uma das várias chamadas claras nomeadas de forma diferente, agora você limpa vários buffers com uma chamada, [**glClear**](glclear.md), por **OR** juntando máscaras de buffer. Por exemplo, **czclear** é substituído por:

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   IRIS GL faz referência à apple de polígono e à máscara de gravação de cor. O OpenGL ignora a apple de polígono, mas faz referência à máscara de gravação de cor. (A **função czclear** ignora a apple de polígono e a máscara de gravação de cor.)

A tabela a seguir lista as várias funções claras do IRIS GL com suas funções equivalentes do OpenGL.



| Chamada IRIS GL         | Chamada openGL                                                               | Significado                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| **acbuf**(AC \_ CLEAR) | **glClear**( GL \_ ACCUM \_ BUFFER BIT \_ )                                     | Limpe o buffer de acúmulo.                    |
|                      | **glClearColor**                                                          | De definir a cor clara do RGBA.                         |
|                      | **glClearIndex**                                                          | De definir o índice de cores claras.                        |
| **clear**            | **glClear**( GL \_ COLOR BUFFER BIT \_ \_ )                                     | Limpe o buffer de cores.                           |
|                      | **glClearDepth**                                                          | Especifique o valor claro para o buffer de profundidade.     |
| **zclear**           | **glClear**( GL \_ DEPTH BUFFER BIT \_ \_ )                                     | Limpe o buffer de profundidade.                           |
| **czclear**          | **glClear**( BIT \_ DE BUFFER DE COR GL GL DEPTH BUFFER BIT \_ \_ \| \_ \_ \_ )<br/> | Limpe o buffer de cores e o buffer de profundidade.      |
|                      | **glClearAccum**                                                          | Especifique valores claros para o buffer de acúmulo. |
|                      | **glClearStencil**                                                        | Especifique o valor de limpar para o buffer de estêncil.   |
| **esclear**           | **glClear**( GL \_ STENCIL \_ BUFFER BIT \_ )                                   | Limpe o buffer de estêncil.                         |



 

Quando o código IRIS GL usa **gclear** **e esclear**, você pode combiná-los em uma única **chamada glClear;** pode melhorar o desempenho do programa.

 

 





