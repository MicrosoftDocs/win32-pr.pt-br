---
description: Em muitos cenários, a segurança baseada em funções é um mecanismo muito eficaz, mas há situações em que ela é menos eficaz.
ms.assetid: 6a1e6cf3-7a8c-4249-926d-675a54061adf
title: Criando funções com eficiência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a340cb2fc643a414ebf784a14e7b61a45bccd3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500849"
---
# <a name="designing-roles-effectively"></a>Criando funções com eficiência

Em muitos cenários, a segurança baseada em funções é um mecanismo muito eficaz, mas há situações em que ela é menos eficaz. Você deve levar alguns fatores em consideração ao decidir onde e como aplicar a segurança baseada em função a um determinado aplicativo.

## <a name="user-and-data-characteristics-and-the-suitability-of-roles"></a>Características de usuário e de dados e a adequação das funções

As funções funcionam muito bem para caracterizar os grupos de usuários e, nessa base, filtrar as ações que esses usuários podem executar. Geralmente, isso é realizado na prática criando funções que refletem o local de um usuário em uma organização — por exemplo, as funções "gerentes" e "Dizems", "administradores" e "leitores", "projeto um funcionário" e "projeto dois funcionários". Nesses casos, onde os dados que estão sendo acessados são razoavelmente genéricos em relação aos usuários, as funções podem ser usadas com eficiência para impor regras de negócio, como as seguintes:

-   "Os gerentes podem transferir qualquer quantidade de dinheiro. Os informadores podem transferir apenas até $10000. "

-   "Os administradores podem alterar qualquer coisa. Todos os outros podem ler apenas. "

-   "O projeto um funcionário pode acessar um determinado banco de dados. Ninguém mais pode ".

Os usuários podem se enquadrar naturalmente em várias funções, dependendo de como as funções modelam a estrutura organizacional de um negócio.

No entanto, as funções não funcionam muito bem quando uma decisão de acesso de segurança mantém as características de uma determinada parte dos dados. Por exemplo, seria difícil usar funções para refletir relacionamentos de dados de usuário complicados, como o seguinte:

-   "Um gerente específico pode acessar dados de pessoal apenas para seus relatórios."

-   "Joe Consumer pode pesquisar seu saldo de conta".

Nesses casos, a verificação de segurança deve ser feita com frequência no próprio banco de dados, em que é mais fácil levar em conta as características de inato dos dados que estão sendo acessados. Isso significa que você deve usar a *representação* para passar a identidade do cliente ao banco de dados e permitir que o banco de dados valide a solicitação. Isso pode afetar o desempenho e pode afetar o design do aplicativo — por exemplo, o pool de conexões pode não funcionar quando uma conexão é aberta sob uma identidade de usuário específica. Para obter uma discussão sobre os problemas envolvidos, consulte [segurança de aplicativos de várias camadas](multi-tier-application-security.md) e [representação e delegação de cliente](client-impersonation-and-delegation.md).

## <a name="complexity-and-scalability-of-a-role-based-authorization-policy"></a>Complexidade e escalabilidade de uma política de autorização de Role-Based

Qualquer política de segurança que você coloque no local será tão eficaz quanto sua implementação pelos administradores do sistema implantando seu aplicativo. Se os administradores cometem erros na atribuição de usuários às funções corretas de acordo com sua política de segurança, sua política não funcionará conforme o esperado. Os problemas têm maior probabilidade de ocorrer nas seguintes circunstâncias:

-   Você fez uma política baseada em função muito complexa, com muitas funções e mapeamentos de usuários para várias funções.
-   Você cria funções com critérios ambíguos para quem deve pertencer a elas.
-   Há muitos usuários no site em que o aplicativo está instalado e os usuários costumam se mover na organização, mudando em relação às funções que você criou.
-   Há muitos administradores no site em que o aplicativo está instalado, com a divisão de responsabilidades, para que um administrador familiarizado com os requisitos de segurança do seu aplicativo esteja potencialmente infamiliarizado com os grandes grupos de usuários que devem usá-lo. Isso é de preocupação específica à medida que os usuários se movem dentro da organização — essas informações precisam ser bem comunicadas.

Além disso, à medida que o número de funções atribuídas a um aplicativo aumenta, a quantidade de tempo que COM+ deve levar em busca da associação do chamador nessas funções, com uma degradação provável no desempenho.

Para gerenciar a complexidade e atenuar essas preocupações, você pode usar as seguintes diretrizes:

-   Escolha os nomes de função que são autodescritivos. Torne-o tão óbvio quanto possível quais usuários devem pertencer a quais funções.
-   Torne sua política baseada em função o mais simples possível (e não mais simples). Escolha o mínimo de funções que você pode, mantendo uma política efetiva.
-   Documente claramente a política baseada em função que você constrói para administradores, independentemente de a associação de função ser óbvia (para você). Em particular, use o campo Descrição disponível para cada função para descrever a intenção da função. Se você não puder descrever geralmente quem deve pertencer à função em algumas frases, provavelmente será muito complicado.
-   É altamente recomendável que os administradores do seu aplicativo preencham funções com grupos de usuários em vez de usuários individuais. Essa é uma solução muito mais escalonável. Ele facilita a reatribuição ou a remoção de usuários à medida que eles se movem dentro da organização e protegem os administradores de uma determinada quantidade de supervisão e problemas na comunicação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Limites de segurança](security-boundaries.md)
</dt> <dt>

[Informações de contexto de chamada de segurança](security-call-context-information.md)
</dt> <dt>

[Propriedade de contexto de segurança](security-context-property.md)
</dt> <dt>

[Usando funções para autorização de cliente](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



