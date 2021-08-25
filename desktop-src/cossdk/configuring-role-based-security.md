---
description: Se o aplicativo COM+ usar a segurança baseada em função, haverá várias tarefas que precisam ser concluídas.
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: Configurando a Role-Based segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aba7df6b11bf44b53adaa9776435e43eabe3188fccb789a01d996f45331298dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859056"
---
# <a name="configuring-role-based-security"></a>Configurando a Role-Based segurança

Se o aplicativo COM+ usar a segurança baseada em função, haverá várias tarefas que precisam ser concluídas. Ao projetar os componentes em seu aplicativo, você define as funções necessárias para ajudar a proteger o acesso a esses componentes. Você também decide quais funções atribuir aos componentes, interfaces e métodos do aplicativo. Durante a integração de aplicativos, você usa a ferramenta administrativa serviços de componentes para adicionar as funções definidas ao aplicativo e atribuir cada função aos componentes, interfaces e métodos apropriados.

Ao configurar a segurança baseada em função, execute as seguintes etapas:

1.  Habilitar verificações de acesso no nível do aplicativo. Para ativar a verificação de segurança de um aplicativo. Consulte [Habilitando verificações de acesso para um aplicativo](enabling-access-checks-for-an-application.md) para obter detalhes sobre como executar esta etapa.
2.  Definir o nível de segurança para verificações de acesso. Para definir a segurança no processo ou no nível do processo e do componente. Consulte [Definindo um nível de segurança para verificações de](setting-a-security-level-for-access-checks.md) acesso para obter detalhes sobre como executar esta etapa.
3.  Habilitar verificações de acesso no nível do componente. Para ativar a verificação de segurança nos níveis de componente, interface e método. Consulte [Habilitando verificações de acesso no nível do componente](enabling-access-checks-at-the-component-level.md) para obter detalhes sobre como executar esta etapa.
4.  Definir funções para um aplicativo. Para criar funções para um aplicativo. Consulte [Definindo funções para um aplicativo para](defining-roles-for-an-application.md) obter detalhes sobre como executar esta etapa.
5.  Atribua funções a componentes, interfaces ou métodos. Para atribuir funções a recursos específicos dentro de um aplicativo. Consulte [Atribuindo funções a componentes, interfaces](assigning-roles-to-components--interfaces--or-methods.md) ou métodos para obter detalhes sobre como executar esta etapa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando a política de restrição de software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Definindo um nível de representação](setting-an-impersonation-level.md)
</dt> </dl>

 

 



