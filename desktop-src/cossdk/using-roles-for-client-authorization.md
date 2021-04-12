---
description: Você usa a segurança baseada em função para estabelecer uma diretiva de autorização, determinando qual cliente ou clientes deve permitir e com que autoridade. Você está decidindo quem deve ser capaz de executar quais ações e acessar quais recursos.
ms.assetid: 8fc27fe1-e50a-44ba-a595-70b1fe463e24
title: Usando funções para autorização de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ae748ddfec438a79e3d0440a00ed7c2f672aed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089299"
---
# <a name="using-roles-for-client-authorization"></a>Usando funções para autorização de cliente

Você usa a segurança baseada em função para estabelecer uma diretiva de autorização, determinando qual cliente ou clientes deve permitir e com que autoridade. Você está decidindo quem deve ser capaz de executar quais ações e acessar quais recursos.

As funções facilitam isso agindo como um mecanismo de controle de acesso invocado sempre que um usuário tenta acessar qualquer recurso de aplicativo. Uma função é basicamente uma lista de usuários – mais precisamente, uma categoria simbólica de usuários que compartilham o mesmo privilégio de segurança. Ao atribuir uma função a um recurso de aplicativo, você está concedendo permissão de acesso para esse recurso a qualquer pessoa que seja membro dessa função.

Portanto, você pode definir um privilégio de segurança muito específico declarando-o como uma função e, em seguida, atribuindo a função a recursos específicos. Quando o aplicativo é implantado, o administrador do sistema pode popular a função com usuários reais e grupos de usuários. Quando o aplicativo for executado, o COM+ imporá a política ao realizar verificações de função.

Fundamentalmente, as funções ajudam a proteger seu código — ou seja, os métodos que podem ser chamados por clientes de um aplicativo COM+. A associação de função é verificada sempre que um cliente tenta chamar um método exposto por um componente em um aplicativo. Se o chamador estiver em uma função atribuída ao método chamado ou ao recurso, a chamada terá sucesso; caso contrário, ele falhará.

## <a name="declarative-role-based-security"></a>Segurança de Role-Based declarativa

Com a segurança declarativa baseada em função, você declara funções administrativamente, usando a ferramenta administrativa serviços de componentes ou as funções administrativas, e as atribui administrativamente aos recursos do aplicativo. Onde e como você define a segurança declarativa determinará onde os limites de segurança são desenhados para seu aplicativo. Para obter mais detalhes, consulte [limites de segurança](security-boundaries.md).

Você pode atribuir uma determinada função a todo o aplicativo, a um componente específico, a uma interface específica em um componente ou a um método específico em uma interface. As atribuições de função são herdadas da cadeia natural de inclusão — ou seja, se você atribuir uma função a um componente, ela será atribuída implicitamente a cada interface e método expostos por esse componente.

Com a disponibilidade das atribuições de função de nível de método, você pode ajudar a proteger componentes e interfaces que não foram projetados tendo em mente a segurança. No entanto, se os próprios métodos não forem protegíveis com atribuições de função declarativas, talvez seja necessário realizar a verificação de função programática. Geralmente, é uma boa ideia manter a segurança em mente ao decidir como fatorar a funcionalidade de negócios por meio de métodos; caso contrário, você pode se deparar adicionando no código relacionado à segurança no último minuto.

Para obter procedimentos detalhados para definir a segurança baseada em função, consulte [configuring Role-Based Security](configuring-role-based-security.md).

## <a name="programmatic-security"></a>Segurança programática

Em algumas circunstâncias, talvez você queira colocar a lógica de segurança em componentes enquanto ainda usa a segurança baseada em funções. Pode ser que você não seja capaz de, ou optar por não, fatorar todas as decisões de acesso por meio de métodos. Por exemplo, você pode ter um recurso de aplicativo privado, talvez um determinado banco de dados, que você deseja permitir que apenas alguns chamadores de um método acessem enquanto exclui outros. Ou você pode ter um único método TransferMoney e deseja restringir alguns chamadores limitando o valor que ele pode transferir.

Em tais circunstâncias, você pode fazer a verificação de função no código. Uma API simples é fornecida, permitindo que você verifique se a segurança está ativada e se um chamador ou um usuário específico está em uma determinada função. Essa funcionalidade está disponível somente quando a segurança baseada em funções está habilitada. Isso significa que você ainda pode aproveitar a segurança declarativa baseada em função onde ela é suficiente e, em seguida, você pode estendê-la programaticamente para um nível mais preciso de granularidade quando necessário.

Além disso, ao usar a segurança baseada em função, você tem acesso programático a informações sobre todos os chamadores upstream na cadeia de chamadas para seu componente. Isso é especialmente útil quando você deseja manter uma trilha de auditoria detalhada.

Para obter descrições de como fazer a verificação de função no código e como acessar informações de contexto de chamada de segurança, consulte [segurança de componente programático](programmatic-component-security.md).

## <a name="authorization-and-authentication"></a>Autorização e autenticação

A autorização significativa pressupõe que você tenha certeza de que os clientes são realmente quem dizem que estão. A verificação da identidade do cliente é tratada separadamente por um serviço de autenticação. Sem a autenticação, você está basicamente deixando os chamadores no sistema honrar. Para obter descrições de autenticação, pois ela afeta aplicativos COM+, consulte [autenticação de cliente](client-authentication.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando funções com eficiência](designing-roles-effectively.md)
</dt> <dt>

[Limites de segurança](security-boundaries.md)
</dt> <dt>

[Informações de contexto de chamada de segurança](security-call-context-information.md)
</dt> <dt>

[Propriedade de contexto de segurança](security-context-property.md)
</dt> </dl>

 

 



