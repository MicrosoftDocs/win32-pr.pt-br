---
description: Se os privilégios de usuários forem alterados ou se as funções forem adicionadas a um aplicativo, você poderá mover uma conta de uma função para outra função.
ms.assetid: 2d81a45a-9762-48b9-8395-3c3a4dcd5e8c
title: Removendo uma conta de usuário ou grupo de uma função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176272aef16af0d0a65d90f6a1d7628a5af232fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771659"
---
# <a name="removing-a-user-account-or-group-from-a-role"></a>Removendo uma conta de usuário ou grupo de uma função

Se os privilégios de um usuário forem alterados ou se as funções forem adicionadas a um aplicativo, você poderá mover uma conta de uma função para outra função. Para mover uma conta de usuário ou grupo de usuários de uma função para outra, você deve remover a conta de usuário ou grupo de sua função atual e, em seguida, atribuí-la à nova função.

**Para mover uma conta de usuário ou grupo de uma função para outra**

1.  Remova a conta de usuário ou grupo da função à qual ela não deve mais pertencer, da seguinte maneira:

    1.  Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ que contém a função em que você está interessado. Expanda a exibição na árvore de console até que os usuários da função fiquem visíveis.

    2.  Clique com o botão direito do mouse na conta de usuário ou grupo que você deseja remover e clique em **excluir**.

    3.  Quando solicitado pela caixa de diálogo **Confirmar exclusão de item** , clique em **Sim** para excluir a conta de usuário ou grupo.

    A conta de usuário ou o grupo que você removeu da função não aparece mais na pasta **usuários** .

2.  Atribua a conta de usuário ou grupo que você removeu para as funções às quais o usuário ou grupo deve ser atribuído, da seguinte maneira:

    1.  Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ que contém a função à qual você deseja adicionar a conta de usuário ou grupo. Expanda a exibição na árvore de console até que as funções do aplicativo fiquem visíveis.

    2.  Localize a função à qual você deseja adicionar a conta de usuário ou grupo.

        > [!Note]  
        > Se a função que você está procurando não estiver na pasta **funções** , a função não foi adicionada ao aplicativo. Ele deve ser adicionado ao aplicativo pelo desenvolvedor antes que você possa atribuir contas de usuário à função.

         

    3.  Clique com o botão direito do mouse na pasta **usuários** na função, aponte para **novo** e clique em **usuário**.

    4.  Na janela **Selecionar usuários ou grupos** , no painel inferior, digite o nome totalmente qualificado do usuário ou grupo que você deseja adicionar. Se você não souber o nome, clique no botão **avançado** e, em seguida, clique em **localizar agora** para exibir uma lista de usuários e grupos no domínio selecionado. Selecione um usuário ou grupo na lista **nome (RDN)** e clique em **OK**.

    5.  Quando terminar de adicionar a conta de usuário ou grupo à função, clique em **OK**.

    Para cada conta de usuário ou grupo que você atribuiu à função, um ícone é exibido na pasta **usuários** .

A associação de função alterada para a conta de usuário ou grupo entrará em vigor na próxima vez em que o aplicativo for iniciado.

 

 



