---
description: Você pode remover contas de usuário ou grupos de uma função quando os usuários ou membros dos grupos não devem mais receber acesso aos recursos do aplicativo aos quais a função está atribuída.
ms.assetid: d2cfa5cb-a143-41de-9aa2-7af7fce10ed7
title: Movendo uma conta de usuário ou grupo para uma função diferente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea402b6012fa4f6e7769e4bbb29a2a11da6e750636b0c139d5f5d6701a397116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047334"
---
# <a name="moving-a-user-account-or-group-to-a-different-role"></a>Movendo uma conta de usuário ou grupo para uma função diferente

Você pode remover contas de usuário ou grupos de uma função quando os usuários ou membros dos grupos não devem mais receber acesso aos recursos do aplicativo aos quais a função está atribuída.

**Para remover uma conta de usuário ou grupo de uma função**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ que contém a função em que você está interessado. Expanda a exibição na árvore de console até que os usuários da função fiquem visíveis.

2.  Clique com o botão direito do mouse na conta de usuário ou grupo que você deseja remover e clique em **excluir**.

3.  Quando solicitado pela caixa de diálogo **Confirmar exclusão de item** , clique em **Sim** para excluir a conta de usuário ou grupo.

A conta de usuário ou o grupo que você removeu da função não aparece mais na pasta **usuários** . A nova associação de função entrará em vigor na próxima vez em que o aplicativo for iniciado. Se você tiver feito alterações no **aplicativo do sistema**, deverá reiniciar o computador para que as alterações entrem em vigor.

 

 



