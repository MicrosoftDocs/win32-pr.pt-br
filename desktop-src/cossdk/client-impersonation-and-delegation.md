---
description: Em algumas circunstâncias, um aplicativo de servidor precisa apresentar uma identidade de clientes aos recursos que ele acessa nos clientes, geralmente para fazer com que as verificações de acesso ou a autenticação sejam executadas em relação à identidade dos clientes.
ms.assetid: fd75eb54-eefe-411f-a7aa-0bc8628f8778
title: Representação e delegação de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7557dcde4cadf559dd8e116cf4e7bece4221aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780907"
---
# <a name="client-impersonation-and-delegation"></a>Representação e delegação de cliente

Em algumas circunstâncias, um aplicativo de servidor precisa apresentar a identidade de um cliente aos recursos que ele acessa em nome do cliente, geralmente para fazer com que as verificações de acesso ou a autenticação sejam executadas em relação à identidade do cliente. Até certo ponto, o servidor pode agir sob a identidade do cliente — uma ação conhecida como representando o cliente.

*Representação* é a capacidade de execução de um thread em um contexto de segurança diferente daquele do processo que possui o thread. O thread do servidor usa um token de acesso que representa as credenciais do cliente e, com isso, ele pode acessar recursos que o cliente pode acessar.

O uso da representação garante que o servidor possa fazer exatamente o que o cliente pode fazer. O acesso aos recursos pode ser restrito ou expandido, dependendo do que o cliente tem permissão para fazer.

Você pode optar por fazer com que um servidor represente um cliente ao se conectar a um banco de dados para que o banco de dados possa autenticar e autorizar o cliente para si mesmo. Ou, se seu aplicativo acessar arquivos que são protegidos com um descritor de segurança e para permitir que o cliente obtenha acesso autorizado a informações nesses arquivos, o aplicativo poderá representar o cliente antes de acessar os arquivos.

## <a name="how-to-implement-impersonation"></a>Como implementar a representação

A representação requer a participação tanto pelo cliente quanto pelo servidor (e, em alguns casos, por administradores do sistema). O cliente deve indicar sua disposição para permitir que o servidor use sua identidade, e o servidor deve assumir a identidade do cliente de forma programática. Para obter detalhes, confira os tópicos [requisitos do lado do cliente para representação](client-side-requirements-for-impersonation.md) e [requisitos do lado do servidor para representação](server-side-requirements-for-impersonation.md).

## <a name="administrative-requirements-for-delegate-level-impersonation"></a>Requisitos administrativos para representação de Delegate-Level

Para usar efetivamente a forma mais poderosa de representação, *delegação*, que é a representação de clientes na rede, as contas de usuário do cliente e do servidor devem ser configuradas corretamente no serviço de Active Directory para dar suporte a ela (além do cliente que concede a autoridade para fazer a representação em nível de delegado), da seguinte maneira:

-   A identidade do servidor deve ser marcada como "confiável para delegação" no serviço de Active Directory.
-   A identidade do cliente não deve ser marcada como "a conta é confidencial e não pode ser delegada" no serviço de Active Directory.

Esses recursos de configuração dão ao administrador de domínio um alto grau de controle sobre a delegação, o que é desejável, considerando a quantidade de confiança (e, portanto, o risco de segurança) envolvida. Para obter mais detalhes sobre a delegação, consulte [delegação e representação](/windows/desktop/com/delegation-and-impersonation).

## <a name="cloaking"></a>Encobrimento

Junto com a autoridade que um cliente concede um servidor por meio do nível de representação, a capacidade de encobrimento do servidor determina em grande parte como o comportamento da representação se comportará. O encobrimento afeta qual identidade é realmente apresentada pelo servidor quando faz chamadas em nome do cliente — seu próprio ou o do cliente. Para obter detalhes, consulte [encobrindo](cloaking.md).

## <a name="performance-implications"></a>Implicações de desempenho

A representação pode afetar significativamente o desempenho e o dimensionamento. Geralmente, é mais caro representar um cliente em uma chamada do que fazer a chamada diretamente. A seguir estão alguns dos problemas a serem considerados:

-   A sobrecarga computacional de passar a identidade em padrões complicados, especialmente se o encobrimento dinâmico estiver habilitado.
-   A complexidade geral de impor a verificação de segurança redundante em vários lugares, em vez de apenas de forma centralizada na camada intermediária.
-   Recursos como conexões de banco de dados, quando aberto representando um cliente, não podem ser reutilizados em vários clientes — um obstáculo muito grande para dimensionar bem.

Às vezes, a única solução eficaz para um problema é usar a representação, mas essa decisão deve ser cuidadosamente avaliada. Para obter uma discussão adicional sobre esses problemas, consulte [segurança de aplicativos de várias camadas](multi-tier-application-security.md).

## <a name="queued-components"></a>Componentes na fila

Os [componentes na fila](com--queued-components.md) não oferecem suporte à representação. Quando um cliente faz uma chamada para um objeto enfileirado, a chamada é realmente feita ao gravador, que o empacota como parte de uma mensagem para o servidor. Em seguida, o ouvinte lê a mensagem da fila e a passa para o Player, que invoca o componente de servidor real e faz a mesma chamada de método. Assim, quando o servidor recebe a chamada, o token do cliente original não está disponível por meio da representação. A segurança baseada em função ainda se aplica, no entanto, e a segurança programática usando a interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) funcionará. Para obter detalhes, consulte [segurança de componentes na fila](queued-components-security.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação de cliente](client-authentication.md)
</dt> <dt>

[Segurança de aplicativos de biblioteca](library-application-security.md)
</dt> <dt>

[Segurança de aplicativos de várias camadas](multi-tier-application-security.md)
</dt> <dt>

[Segurança de componente programática](programmatic-component-security.md)
</dt> <dt>

[Administração de segurança baseada em funções](role-based-security-administration.md)
</dt> <dt>

[Usando a política de restrição de software no COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
