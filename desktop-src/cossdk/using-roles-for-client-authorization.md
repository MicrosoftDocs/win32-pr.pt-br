---
description: Você usa a segurança baseada em função para estabelecer uma política de autorização, determinando qual cliente ou cliente deve entrar e com qual autoridade. Você está decidindo quem deve ser capaz de executar quais ações e acessar quais recursos.
ms.assetid: 8fc27fe1-e50a-44ba-a595-70b1fe463e24
title: Usando funções para autorização de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a808abc08d5360ba0b7fae0a7c31af80a4cab28c43e6014076c549204e6f28e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499636"
---
# <a name="using-roles-for-client-authorization"></a>Usando funções para autorização de cliente

Você usa a segurança baseada em função para estabelecer uma política de autorização, determinando qual cliente ou cliente deve entrar e com qual autoridade. Você está decidindo quem deve ser capaz de executar quais ações e acessar quais recursos.

As funções facilitam isso atuando como um mecanismo de controle de acesso invocado sempre que um usuário tenta acessar qualquer recurso de aplicativo. Uma função é basicamente uma lista de usuários, mais precisamente, uma categoria simbólica de usuários que compartilham o mesmo privilégio de segurança. Ao atribuir uma função a um recurso de aplicativo, você está concedendo permissão de acesso para esse recurso a quem é membro dessa função.

Portanto, você pode definir um privilégio de segurança muito específico declarando-o como uma função e atribuindo a função a recursos específicos. Quando o aplicativo é implantado, o administrador do sistema pode preencher a função com usuários e grupos de usuários reais. Quando o aplicativo for executado, o COM+ imporá a política executando verificações de função.

Fundamentalmente, as funções ajudam a proteger seu código, ou seja, os métodos que podem ser chamados por clientes de um aplicativo COM+. A associação de função é verificada sempre que um cliente tenta chamar um método exposto por um componente em um aplicativo. Se o chamador estiver em uma função atribuída ao método chamado ou recurso, a chamada terá êxito; caso contrário, ele falhará.

## <a name="declarative-role-based-security"></a>Segurança Role-Based declarativa

Com a segurança declarativa baseada em função, você declara funções administrativamente ( usando a ferramenta administrativa serviços de componentes ou as funções administrativas ) e as atribui administrativamente aos recursos do aplicativo. Onde e como você define a segurança declarativa determinarão onde os limites de segurança são desenhados para seu aplicativo. Para obter mais detalhes, consulte [Limites de segurança.](security-boundaries.md)

Você pode atribuir uma determinada função a todo o aplicativo, a um componente específico, a uma interface específica em um componente ou a um método específico em uma interface. As atribuições de função são herdadas na cadeia natural de inclusão, ou seja, se você atribuir uma função a um componente, ela será atribuída implicitamente a cada interface e método exposto por esse componente.

Com a disponibilidade de atribuições de função de nível de método, você pode ajudar a proteger efetivamente componentes e interfaces que não foram projetados com a segurança em mente. No entanto, se os próprios métodos não sãocuráveis com atribuições de função declarativas, talvez seja necessário fazer a verificação programática de função. Geralmente, é uma boa ideia ter em mente a segurança ao decidir como fatorar a funcionalidade de negócios por meio de métodos; caso contrário, você poderá adicionar o código relacionado à segurança no último minuto.

Para ver os procedimentos detalhados para definir a segurança baseada em função, consulte [Configurando Role-Based segurança.](configuring-role-based-security.md)

## <a name="programmatic-security"></a>Segurança programática

Em algumas circunstâncias, talvez você queira colocar a lógica de segurança em componentes enquanto ainda usa a segurança baseada em função. Pode ser que você não seja capaz de, ou optar por não fazer isso, fatorar todas as decisões de acesso por meio de métodos. Por exemplo, você pode ter um recurso de aplicativo privado, talvez um banco de dados específico, que você deseja permitir que apenas alguns chamadores de um método acessem, excluindo outros. Ou você pode ter um único método TransferMoney e querer restringir alguns chamadores limitando a quantidade que eles podem transferir.

Nessas circunstâncias, você pode fazer a verificação de função no código. Uma API simples é fornecida, permitindo que você verifique se a segurança está ativa e se um chamador ou um usuário específico está em uma determinada função. Essa funcionalidade só estará disponível quando a segurança baseada em função estiver habilitada. Isso significa que você ainda pode aproveitar a segurança declarativa baseada em função onde ela é suficiente e, em seguida, pode estendá-la programaticamente para um nível mais fino de granularidade quando necessário.

Além disso, ao usar a segurança baseada em função, você tem acesso programático a informações sobre todos os chamadores upstream na cadeia de chamadas para seu componente. Isso é especialmente útil quando você deseja manter uma trilha de auditoria detalhada.

Para obter descrições de como fazer a verificação de função no código e como acessar informações de contexto de chamada de segurança, consulte [Segurança de componente programático](programmatic-component-security.md).

## <a name="authorization-and-authentication"></a>Autorização e autenticação

A autorização significativa pressupõe que você tem certeza de que os clientes são, na verdade, quem eles dizem ser. A verificação da identidade do cliente é tratada separadamente por um serviço de autenticação. Sem autenticação, basicamente, você está deixando os chamadores entrarem no sistema de excelência. Para ver descrições da autenticação, pois ela afeta aplicativos COM+, consulte [Autenticação de cliente](client-authentication.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Projetando funções com eficiência](designing-roles-effectively.md)
</dt> <dt>

[Limites de segurança](security-boundaries.md)
</dt> <dt>

[Informações de contexto de chamada de segurança](security-call-context-information.md)
</dt> <dt>

[Propriedade de contexto de segurança](security-context-property.md)
</dt> </dl>

 

 



