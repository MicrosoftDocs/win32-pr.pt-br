---
description: Você pode usar a ferramenta administrativa serviços de componentes para preencher uma função com contas de usuário ou grupos.
ms.assetid: 1cf7dc38-185a-4cc4-8f4c-44b6af4c5f4a
title: Atribuindo uma conta de usuário ou grupo a uma função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53b37c9f0265e02c7abdf74eeaf81bd0b12e3d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798460"
---
# <a name="assigning-a-user-account-or-group-to-a-role"></a>Atribuindo uma conta de usuário ou grupo a uma função

Você pode usar a ferramenta administrativa serviços de componentes para preencher uma função com contas de usuário ou grupos. A maneira preferida de atribuir uma conta de usuário a uma função é atribuir a conta de usuário a um grupo e, em seguida, atribuir o grupo à função. Usar grupos para popular funções torna mais fácil gerenciar um grande número de usuários. Na ajuda online para a ferramenta administrativa Gerenciamento de computador, consulte o tópico "usuários e grupos locais" para obter mais informações sobre como criar grupos ou atribuir uma conta de usuário a um grupo.

> [!Note]  
> Para permitir que usuários de rede não autenticados executem um aplicativo COM+, as funções de aplicativo devem incluir o usuário anônimo. A partir do Windows Server 2003, por padrão, o usuário anônimo não está incluído no grupo Everyone.

 

Depois de atribuir a conta de usuário ao grupo do Windows apropriado, siga estas etapas para atribuir o grupo do Windows à função.

**Para atribuir um grupo do Windows a uma função de segurança**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ que contém a função à qual você deseja adicionar a conta de usuário ou grupo. Expanda a exibição na árvore de console até que as funções do aplicativo fiquem visíveis.

2.  Localize a função à qual você deseja adicionar a conta de usuário ou grupo.

    > [!Note]  
    > Se a função que você está procurando não estiver na pasta **funções** , a função não foi adicionada ao aplicativo. Ele deve ser adicionado ao aplicativo pelo desenvolvedor antes que você possa atribuir contas de usuário à função.

     

3.  Clique com o botão direito do mouse na pasta **usuários** na função, aponte para **novo** e clique em **usuário**.

4.  Na janela **Selecionar usuários ou grupos** , no painel inferior, digite o nome totalmente qualificado do usuário ou grupo que você deseja adicionar. Se você não souber o nome, clique no botão **avançado** e, em seguida, clique em **localizar agora** para exibir uma lista de usuários e grupos no domínio selecionado. Selecione um usuário ou grupo na lista **nome (RDN)** e clique em **OK**.

5.  Para adicionar mais contas de usuário ou grupos, repita a etapa 4.

6.  Quando terminar de adicionar contas de usuário e grupos à função, clique em **OK**.

Para cada conta de usuário ou grupo que você atribuiu à função, um ícone é exibido na pasta **usuários** . A nova associação de função entrará em vigor na próxima vez em que o aplicativo for iniciado.

 

 



