---
description: Você determina uma política de segurança para um aplicativo definindo os privilégios de segurança necessários.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Definindo funções para um aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc4b4fb6aaee557eea69dec405254925cd669d18ac73cdea229f548145d8701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637706"
---
# <a name="defining-roles-for-an-application"></a>Definindo funções para um aplicativo

Você determina uma política de segurança para um aplicativo definindo os privilégios de segurança necessários. Para fazer isso, declare um nível simbólico de privilégio como uma função , [](assigning-roles-to-components--interfaces--or-methods.md) ou seja, defina a função para o aplicativo e atribua a função a recursos específicos dentro do aplicativo. Esse design é atendido quando o aplicativo é implantado e os administradores do sistema preenchem a função com usuários reais e grupos de usuários. Para saber mais, confira [Administração de segurança baseada em função.](role-based-security-administration.md)

**Para adicionar uma função a um aplicativo**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ ao qual você deseja adicionar a função. Expanda a árvore para exibir as pastas do aplicativo.

2.  Clique com o botão direito **do** mouse na pasta Funções do aplicativo, aponte para **Novo** e clique em **Função**.

3.  Na caixa **de** diálogo Função, digite o nome da nova função na caixa fornecida.

4.  Clique em **OK**.

> [!Note]  
> Depois de adicionar funções ao aplicativo, você deve atribuir as funções aos componentes, interfaces e métodos apropriados. Caso contrário, se a segurança baseada em função tiver sido escolhida e habilitada e se as funções foram adicionadas, mas não atribuídas, todas as chamadas ao aplicativo falharão. Para obter mais informações, [consulte Atribuindo funções a componentes, interfaces ou métodos](assigning-roles-to-components--interfaces--or-methods.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atribuindo funções a componentes, interfaces ou métodos](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configurando a Role-Based segurança](configuring-role-based-security.md)
</dt> <dt>

[Habilitando verificações de acesso para um aplicativo](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Habilitando verificações de acesso no nível do componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Definindo um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



