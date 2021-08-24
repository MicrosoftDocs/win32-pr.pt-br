---
title: Funções de portabilidade que obtêm matrizes e transformações
description: A tabela a seguir lista as funções da íris GL que obtêm o estado de matrizes e transformações e seus equivalentes em OpenGL.
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- Portabilidade do íris GL, matrizes
- portando do íris GL, matrizes
- portando para OpenGL do íris GL, matrizes
- Portabilidade OpenGL do íris GL, matrizes
- matrizes
- Portabilidade do íris GL, transformações
- portando do íris GL, transformações
- portando para OpenGL do íris GL, transformações
- Portabilidade do OpenGL do íris GL, transformações
- transformações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68eed8722d982d8d93f47f4d2dc02b8f0f97d9c58512400353ab068015455e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776966"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a>Funções de portabilidade que obtêm matrizes e transformações

A tabela a seguir lista as funções da íris GL que obtêm o estado de matrizes e transformações e seus equivalentes em OpenGL.



| Consulta de matriz do íris GL                  | Consulta de matriz de glGet OpenGL         | Significado                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| **getmmode**                          | \_modo de matriz GL \_                  | Retorna o modo de matriz atual.                                |
| **getmatrix** no modo de **MVIEWING**    | \_MODELVIEW \_ matriz GL             | Retorna uma cópia da matriz de exibição de modelo atual.                |
| **getmatrix** no modo de **MPROJECTION** | \_matriz de projeção GL \_            | Retorna uma cópia da matriz de projeção atual.                |
| **getmatrix** no modo de **MTEXTURE**    | \_matriz de textura GL \_               | Retorna uma cópia da matriz de textura atual.                   |
| Não aplicável.                       | \_profundidade máxima \_ de \_ pilha de MODELVIEW \_ GL  | Retorna a profundidade máxima com suporte da pilha de matriz de exibição de modelo. |
| Não aplicável.                       | \_profundidade máxima \_ da \_ pilha de projeção GL \_ | Retorna a profundidade máxima com suporte da pilha da matriz de projeção. |
| Não aplicável.                       | \_profundidade máxima \_ da \_ pilha de textura \_ GL    | Retorna a profundidade máxima com suporte da pilha de matriz de textura.    |
| Não aplicável.                       | \_profundidade de \_ pilha \_ MODELVIEW GL       | Retorna o número de matrizes na pilha de exibição do modelo.             |
| Não aplicável.                       | \_profundidade da pilha de projeção GL \_ \_      | Retorna o número de matrizes na pilha de projeção.             |
| Não aplicável.                       | \_profundidade da \_ pilha de textura GL \_         | Retorna o número de matrizes na pilha de textura.                |



 

??

 

 




