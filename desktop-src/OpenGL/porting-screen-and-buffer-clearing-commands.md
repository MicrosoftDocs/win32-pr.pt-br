---
title: Comandos de limpeza de tela e buffer de portabilidade
description: O OpenGL substitui uma variedade de funções do íris GL Clear (como zclear, aclear, sClear e assim por diante) por uma única função, glClear. Especifique exatamente o que você deseja limpar passando máscaras para glClear.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- Portabilidade do íris GL, limpar funções
- portando do íris GL, limpar funções
- portando para OpenGL do íris GL, limpar funções
- Portabilidade do OpenGL do íris GL, limpar funções
- limpar funções
- Portabilidade do íris GL, comandos de limpeza de tela
- portando do íris GL, comandos de limpeza de tela
- portando para OpenGL do íris GL, comandos de limpeza de tela
- Portabilidade OpenGL do íris GL, comandos de limpeza de tela
- comandos de limpeza de tela
- Portabilidade do íris GL, comandos de limpeza de buffer
- portando do íris GL, comandos de limpeza de buffer
- portando para OpenGL do íris GL, comandos de limpeza de buffer
- Portabilidade OpenGL do íris GL, comandos de limpeza de buffer
- comandos de limpeza de buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53566c9fe14922f3965133cef9e30cbea4548b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753119"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a>Comandos de limpeza de tela e buffer de portabilidade

O OpenGL substitui uma variedade de funções do íris GL **Clear** (como **zclear**, **aclear**, **sClear** e assim por diante) por uma única função, [**glClear**](glclear.md). Especifique exatamente o que você deseja limpar passando máscaras para **glClear**.

Tenha os seguintes pontos em mente ao portar comandos de tela e buffer:

-   O OpenGL mantém a limpeza das cores separadamente das cores de desenho, com chamadas como [**glClearColor**](glclearcolor.md) e [**glClearIndex**](glclearindex.md). Certifique-se de definir a cor clara para cada buffer antes de apagar.
-   Em vez de usar uma das várias chamadas Clear nomeadas de forma diferente, agora você limpa vários buffers com uma chamada, [**glClear**](glclear.md), por **ou** encaixar máscaras de buffer. Por exemplo, **czclear** é substituído por:

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   A íris GL faz referência ao polígono Stipple e à cor writemask. O OpenGL ignora o polígono Stipple mas faz referência à cor writemask. (A função **czclear** ignora o Stipple de polígono e a cor writemask.)

A tabela a seguir lista as várias funções do íris GL Clear com suas funções OpenGL equivalentes.



| Chamada do íris GL         | Chamada OpenGL                                                               | Significado                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| **acbuf**(AC \_ limpa) | **glClear**(bit de buffer do GL \_ Accum \_ \_ )                                     | Limpe o buffer de acumulação.                    |
|                      | **glClearColor**                                                          | Defina a cor nítida de RGBA.                         |
|                      | **glClearIndex**                                                          | Defina o índice de cor de limpeza.                        |
| **clear**            | **glClear**( \_ bit de buffer de cores GL \_ \_ )                                     | Limpe o buffer de cores.                           |
|                      | **glClearDepth**                                                          | Especifique o valor de limpeza para o buffer de profundidade.     |
| **zclear**           | **glClear**(bit de buffer de profundidade do GL \_ \_ \_ )                                     | Limpe o buffer de profundidade.                           |
| **czclear**          | **glClear**(bit de buffer de cores GL GL \_ \_ nível de \_ \| \_ \_ memória \_<br/> | Limpe o buffer de cores e o buffer de profundidade.      |
|                      | **glClearAccum**                                                          | Especifique os valores claros para o buffer de acumulação. |
|                      | **glClearStencil**                                                        | Especifique o valor de limpeza para o buffer de estêncil.   |
| **sclear**           | **glClear**( \_ bit de buffer do estêncil GL \_ \_ )                                   | Limpe o buffer do estêncil.                         |



 

Quando o código do íris GL usa **gclear** e **sClear**, você pode combiná-los em uma única chamada de **glClear** ; pode melhorar o desempenho do seu programa.

 

 





