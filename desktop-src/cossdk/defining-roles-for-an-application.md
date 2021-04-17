---
description: Você determina uma política de segurança para um aplicativo definindo os privilégios de segurança que ele requer.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Definindo funções para um aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e46eb2cb857a2b2dee2aabe41cb571e12ed98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813704"
---
# <a name="defining-roles-for-an-application"></a>Definindo funções para um aplicativo

Você determina uma política de segurança para um aplicativo definindo os privilégios de segurança que ele requer. Para fazer isso, você declara um nível simbólico de privilégio como uma função, ou seja, define a função para o aplicativo — e, em seguida, [atribui a função](assigning-roles-to-components--interfaces--or-methods.md) a recursos específicos dentro do aplicativo. Esse design é atendido quando o aplicativo é implantado e os administradores do sistema preenchem a função com usuários reais e grupos de usuários. Para obter mais detalhes, consulte [Administração de segurança baseada em funções](role-based-security-administration.md).

**Para adicionar uma função a um aplicativo**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ ao qual você deseja adicionar a função. Expanda a árvore para exibir as pastas do aplicativo.

2.  Clique com o botão direito do mouse na pasta **funções** do aplicativo, aponte para **novo** e clique em **função**.

3.  Na caixa de diálogo **função**, digite o nome da nova função na caixa fornecida.

4.  Clique em **OK**.

> [!Note]  
> Depois de adicionar funções ao aplicativo, você deve ter certeza de atribuir as funções aos componentes, às interfaces e aos métodos apropriados. Caso contrário, se a segurança baseada em funções tiver sido escolhida e habilitada e se as funções tiverem sido adicionadas, mas não atribuídas, todas as chamadas para o aplicativo falharão. Para obter mais informações, consulte [atribuindo funções a componentes, interfaces ou métodos](assigning-roles-to-components--interfaces--or-methods.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atribuindo funções a componentes, interfaces ou métodos](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configurando a segurança do Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Habilitando verificações de acesso para um aplicativo](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Habilitando verificações de acesso no nível do componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Configurando um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



