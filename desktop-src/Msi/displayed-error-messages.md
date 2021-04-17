---
description: Uma função do instalador pode exibir uma caixa de diálogo de mensagem de erro retornando qualquer um dos erros a seguir. Uma caixa de erro será exibida somente se o nível da interface do usuário estiver no nível completo, reduzido ou básico. Para obter mais informações, consulte níveis de interface do usuário.
ms.assetid: 0153a21f-9b26-4088-b12b-96c9e6918cc3
title: Mensagens de erro exibidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d85417da7e2f8a01be5492560e83cd97bbc0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748163"
---
# <a name="displayed-error-messages"></a>Mensagens de erro exibidas

Uma [função do instalador](installer-function-reference.md) pode exibir uma caixa de diálogo de mensagem de erro retornando qualquer um dos erros a seguir. Uma caixa de erro será exibida somente se o nível da interface do usuário estiver no nível completo, reduzido ou básico. Para obter mais informações, consulte [níveis de interface do usuário](user-interface-levels.md).

As funções do instalador exibem apenas mensagens de erro que estão na tabela a seguir. Para erros que não estão nessa lista, o chamador da função é responsável por manipular a exibição de mensagens de erro.



| Código do erro               | Erro                        |
|--------------------------|------------------------------|
| ERRO ao \_ instalar \_ suspensão  | A instalação foi suspensa.   |
| ERRO ao \_ instalar o \_ UserExit | O usuário saiu da instalação. |
| \_falha na instalação do erro \_  | Falha na instalação.              |



 

 

 



