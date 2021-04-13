---
description: Atribuindo funções a componentes, interfaces ou métodos
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: Atribuindo funções a componentes, interfaces ou métodos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5efb66c9de865cbfcdc6e9cb047af92c95f6bc0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370462"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a>Atribuindo funções a componentes, interfaces ou métodos

Você pode atribuir explicitamente uma função a qualquer item em um aplicativo COM+ que seja visível por meio da ferramenta administrativa serviços de componentes. Isso garante que todos os usuários que são membros da função tenham acesso permitido a esse item e a quaisquer outros itens que ele contenha. Por exemplo, se você atribuir a função "leitores" a um componente, qualquer membro de "leitores" tem permissão para acessar esse componente e quaisquer interfaces e métodos que ele expõe. Os "leitores" aparecerão como uma função herdada para qualquer uma dessas interfaces e métodos.

Um método só poderá ser acessado pelos chamadores se você atribuir uma função a ele, seja atribuindo explicitamente a função diretamente ao método ou atribuindo uma função à interface do método ou ao componente do método; nesse caso, a função será herdada pelo método. Se nenhuma função for atribuída e se as verificações de acesso estiverem habilitadas, todas as chamadas para o método falharão.

Para poder atribuir uma função, você deve [defini](defining-roles-for-an-application.md) -la para o aplicativo. Todas as funções definidas para o aplicativo aparecerão na janela **funções explicitamente definidas para os itens selecionados** na guia **segurança** para quaisquer componentes, métodos e interfaces dentro do aplicativo.

**Para atribuir funções a um componente, método ou interface**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ para o qual a função foi definida. Expanda a árvore para exibir os componentes, as interfaces ou os métodos do aplicativo, dependendo do que você está atribuindo a função.

2.  Clique com o botão direito do mouse no item ao qual você deseja atribuir a função e clique em **Propriedades**.

3.  Na caixa de diálogo Propriedades, clique na guia **segurança** .

4.  Na caixa **funções explicitamente definidas para Item (ns) selecionado (s)** , selecione as funções que você deseja atribuir ao item.

5.  Clique em **OK**.

Todas as funções que você definir explicitamente para um item serão herdadas por itens de nível inferior que ele contém e aparecerão na janela **funções herdadas por item (ns) selecionado (s)** para esses itens.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando a segurança do Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Definindo funções para um aplicativo](defining-roles-for-an-application.md)
</dt> <dt>

[Habilitando verificações de acesso para um aplicativo](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Habilitando verificações de acesso no nível do componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Configurando um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



