---
title: Portando listas de exibição
description: A implementação do OpenGL de listas de exibição é semelhante à implementação da íris GL, com duas exceções no OpenGL, você não pode editar listas de exibição depois de criá-las e não pode chamar funções de listas de exibição.
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- Portabilidade do íris GL, listas de exibição
- portando do íris GL, listas de exibição
- portando para OpenGL do íris GL, listas de exibição
- Portabilidade OpenGL do íris GL, listas de exibição
- Exibir listas, portando do íris GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461000e6d785f0d03bbbc8f738eba60768bc5d74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291894"
---
# <a name="porting-display-lists"></a>Portando listas de exibição

A implementação do OpenGL de listas de exibição é semelhante à implementação da íris GL, com duas exceções: no OpenGL, não é possível editar as listas de exibição depois de criá-las e não é possível chamar funções de dentro de listas de exibição.

Como não é possível editar ou chamar funções de listas de exibição, essas funções de íris GL não têm nenhum equivalente em OpenGL:

-   **editobj**
-   **objdelete**, **objinsert** e **objreplace**
-   **maketag**, **gentag**, **IsTag** e **deltag**
-   **callfunc**

No íris GL, você usa as funções **makeobj** e **closeobj** para criar listas de exibição. No OpenGL, você usa [**glNewList**](glnewlist.md) e [**glEndList**](glendlist.md).

A tabela a seguir lista as funções de lista de exibição do íris GL com suas funções OpenGL equivalentes.



| Função GL de íris | Função OpenGL                                                      | Significado                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| **makeobj**      | **glNewList**                                                        | Cria uma nova lista de exibição.                                   |
| **closeobj**     | **glEndList**                                                        | Indica o fim da lista de exibição.                                  |
| **callobj**      | [**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md) | Executa lista ou listas de exibição.                               |
| **isobj**        | [**glIsList**](glislist.md)                                         | Testes para a existência da lista de exibição.                             |
| **delobj**       | [**glDeleteLists**](gldeletelists.md)                               | Exclui o grupo contíguo de listas de exibição.                    |
| **genobj**       | [**glGenLists**](glgenlists.md)                                     | Gera o número determinado de listas de exibição vazias contíguas. |



 

Este tópico inclui informações sobre o seguinte.

-   [Portando a função bbox2](porting-the-bbox2-function.md)
-   [Portando listas de exibição editadas](porting-edited-display-lists.md)
-   [Uma porta de exemplo de uma lista de exibição](a-sample-port-of-a-display-list.md)

 

 




