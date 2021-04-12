---
title: Portando chamadas de plano de estêncil
description: No OpenGL, você aloca planos de estêncil solicitando o formato de pixel apropriado com o OpenGL auxInitDisplayMode ou ChoosePixelFormat.
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- Portabilidade do íris GL, planos de estêncil
- portando do íris GL, planos de estêncil
- portando para OpenGL do íris GL, planos de estêncil
- Portabilidade OpenGL do íris GL, planos de estêncil
- planos de estêncil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829ea033a75cb1153a475496c3f33398640dbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292439"
---
# <a name="porting-stencil-plane-calls"></a>Portando chamadas de plano de estêncil

No OpenGL, você aloca planos de estêncil solicitando o formato de pixel apropriado com o OpenGL **auxInitDisplayMode** ou [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat). funções. A tabela a seguir lista as funções do íris GL que afetam os planos de estêncil e suas funções OpenGL equivalentes.



| Função GL de íris             | Função OpenGL                                         | Significado                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| **stensize**                 | **ChoosePixelFormat**                                   |                                                        |
| **estêncil**( **verdadeiro**,...) | [**glEnable**](glenable.md) ( \_ teste de estêncil GL \_ )      | Habilita testes de estêncil.                                 |
| **estêncil**                  | [**glStencilOp**](glstencilop.md)                      | Define ações de teste de estêncil.                             |
| **estêncil**(... Func,...)  | [**glStencilFunc**](glstencilfunc.md)                  | Define o valor de função e referência para teste de estêncil. |
| **swritemask**               | [**glStencilMask**](glstencilmask.md)                  | Especifica quais bits de estêncil podem ser gravados.           |
|                              | [**glClearStencil**](glclearstencil.md)                | Especifica o valor de limpeza para o buffer de estêncil.      |
| **sclear**                   | [**glClear**](glclear.md) ( \_ bit de buffer do estêncil GL \_ \_ ) |                                                        |



 

As funções de comparação de estêncil e de passagem/falha de estêncil são quase equivalentes em OpenGL e íris GL. Os sinalizadores de função de estêncil íris GL são precedidos de it; os sinalizadores OpenGL com GL. Os sinalizadores de operação de passagem/reprovação do íris GL são precedidos de ST; os sinalizadores OpenGL com GL.

 

 




