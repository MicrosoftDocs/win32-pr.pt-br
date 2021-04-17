---
description: Criando um novo aplicativo COM+
ms.assetid: eec4e871-36c2-4e60-9808-1400efcfc60c
title: Criando um novo aplicativo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09eb296ad0a5f2326b5d931f59a5075d001d89f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762356"
---
# <a name="creating-a-new-com-application"></a>Criando um novo aplicativo COM+

A criação de um novo aplicativo COM+ requer duas etapas básicas, da seguinte maneira:

-   Criando um aplicativo COM+ vazio (descrito abaixo).
-   Adicionando componentes ao aplicativo. (Consulte [instalando novos componentes](installing-new-components.md) e [importando componentes](importing-components.md).)

**Para criar um aplicativo COM+ vazio**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, selecione o computador no qual você deseja criar um aplicativo.

2.  Selecione a pasta **aplicativos com+** para esse computador.

3.  No menu **ação** , aponte para **novo** e clique em **aplicativo**. Você também pode clicar com o botão direito do mouse na pasta **aplicativos com+** , apontar para **novo** e clicar em **aplicativo**.

4.  Na página de **boas-vindas** do assistente de instalação do aplicativo com+, clique em **Avançar** e, na caixa de diálogo **instalar ou criar um novo aplicativo** , clique em **criar um aplicativo vazio**.

5.  Na caixa fornecida, digite um nome para o novo aplicativo. (Observe que os seguintes caracteres especiais não podem ser usados em um nome de aplicativo: \\ ,/, ~,!, @, \# ,%, ^, &, \* , (,), \| ,}, {, \] , \[ , ', ", >, <,.,?,: e;.) Em **tipo de ativação**, clique em **aplicativo de biblioteca** ou **aplicativo de servidor**. Clique em **Próximo**.

    > [!Note]  
    > Um aplicativo de servidor é executado em seu próprio processo. Os aplicativos de servidor podem dar suporte a todos os serviços COM+. Um aplicativo de biblioteca é executado no processo do cliente que o cria. Os aplicativos de biblioteca podem usar a segurança baseada em função, mas não dão suporte a acesso remoto ou a componentes na fila.

     

6.  Na caixa de diálogo **definir identidade do aplicativo** , escolha uma identidade sob a qual o aplicativo será executado. Se você selecionar **este usuário**, digite o nome de usuário e a senha. Você também deve digitar a senha novamente na caixa **Confirmar senha** . Clique em **Próximo**. (A seleção padrão de identidade do aplicativo é **usuário interativo**. O usuário interativo é o usuário conectado ao computador do servidor em um determinado momento. Você pode selecionar um usuário diferente selecionando **esse usuário** e inserindo um usuário ou grupo específico.)

    > [!Note]  
    > A caixa de diálogo **definir identidade do aplicativo** será exibida somente se você tiver selecionado **aplicativo de servidor** para o tipo de ativação do novo aplicativo na caixa de diálogo anterior do assistente de instalação de aplicativo com. A propriedade Identity não é usada para aplicativos de biblioteca.

     

7.  Na caixa de diálogo **adicionar funções de aplicativo** , adicione as funções que você deseja associar ao aplicativo. Por padrão, somente a função **CreatorOwner** é definida. Para obter informações sobre funções, consulte [Administração de segurança baseada em funções](role-based-security-administration.md).

8.  Na caixa de diálogo **Adicionar usuários às funções** , preencha cada função que você criou na última etapa com os usuários, grupos ou entidades de segurança internas às quais você deseja conceder os privilégios associados a essa função. Por padrão, o usuário interativo é colocado na função **CreatorOwner** .

9.  Clique em **Concluir**.

O novo aplicativo agora será exibido na pasta **aplicativos com+** na árvore de console da ferramenta administrativa serviços de componentes.

> [!Note]  
> A partir do Windows Server 2003, as verificações de acesso são habilitadas por padrão ao criar um aplicativo COM+. Em versões anteriores, as verificações de acesso foram desabilitadas por padrão no nível do aplicativo. O resultado é que, por padrão, o acesso a um aplicativo COM+ é permitido somente para usuários que estão nas funções associadas ao aplicativo. (Consulte [Administração de segurança baseada em funções](role-based-security-administration.md).) Como alternativa, você pode permitir o acesso a todos os usuários desabilitando as verificações de acesso em um aplicativo COM+. (Consulte [habilitando verificações de acesso para um aplicativo](enabling-access-checks-for-an-application.md).)

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Copiando componentes](copying-components.md)
</dt> <dt>

[Excluindo um aplicativo COM+](deleting-a-com--application.md)
</dt> <dt>

[Importando componentes](importing-components.md)
</dt> <dt>

[Instalando novos componentes](installing-new-components.md)
</dt> <dt>

[Movendo componentes](moving-components.md)
</dt> <dt>

[Removendo um componente de um aplicativo COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



