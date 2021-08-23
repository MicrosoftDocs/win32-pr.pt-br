---
description: Uma função do instalador pode exibir uma caixa de diálogo de mensagem de erro retornando qualquer um dos erros a seguir. Uma caixa de erro será exibida somente se o nível da interface do usuário estiver no nível completo, reduzido ou básico. Para obter mais informações, consulte Interface do Usuário níveis.
ms.assetid: 0153a21f-9b26-4088-b12b-96c9e6918cc3
title: Mensagens de erro exibidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4e339a67f054134b4e2462593682cbdeac8d6eb7be63fefd93fd32d504f5e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745376"
---
# <a name="displayed-error-messages"></a>Mensagens de erro exibidas

Uma [função do instalador](installer-function-reference.md) pode exibir uma caixa de diálogo de mensagem de erro retornando qualquer um dos erros a seguir. Uma caixa de erro será exibida somente se o nível da interface do usuário estiver no nível completo, reduzido ou básico. Para obter mais informações, consulte [Interface do Usuário níveis .](user-interface-levels.md)

As funções do instalador exibem apenas mensagens de erro que estão na tabela a seguir. Para erros que não estão nesta lista, o chamador da função é responsável por manipular a exibição de mensagens de erro.



| Código do erro               | Erro                        |
|--------------------------|------------------------------|
| ERRO AO \_ INSTALAR \_ SUSPEND  | A instalação foi suspensa.   |
| ERRO \_ AO \_ INSTALAR USEREXIT | O usuário saiu da instalação. |
| ERRO \_ AO INSTALAR \_ FALHA  | Falha na instalação.              |



 

 

 



