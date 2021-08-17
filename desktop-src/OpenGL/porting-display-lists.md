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
ms.openlocfilehash: 858f1f3be180b3ef09c81bb8d61b18705fc9485742d7384562eecff142f4bfb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980798"
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

 

 




