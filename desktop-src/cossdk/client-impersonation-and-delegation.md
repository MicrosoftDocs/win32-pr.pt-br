---
description: Em algumas circunstâncias, um aplicativo de servidor precisa apresentar uma identidade de clientes aos recursos que acessa em nome dos clientes, geralmente para fazer com que as verificações de acesso ou a autenticação sejam executadas na identidade dos clientes.
ms.assetid: fd75eb54-eefe-411f-a7aa-0bc8628f8778
title: Representação e delegação do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b0262f3d8dd6736d183fa76eb5d3f0946d50b2724e76bcea73843644aaefb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129368"
---
# <a name="client-impersonation-and-delegation"></a>Representação e delegação do cliente

Em algumas circunstâncias, um aplicativo de servidor precisa apresentar a identidade de um cliente aos recursos que ele acessa em nome do cliente, geralmente para fazer com que as verificações de acesso ou a autenticação sejam executadas na identidade do cliente. Até certo ponto, o servidor pode agir sob a identidade do cliente , uma ação conhecida como representação do cliente.

*Representação é* a capacidade de um thread executar em um contexto de segurança diferente do processo que possui o thread. O thread do servidor usa um token de acesso que representa as credenciais do cliente e, com isso, ele pode acessar recursos que o cliente pode acessar.

O uso da representação garante que o servidor possa fazer exatamente o que o cliente pode fazer. O acesso aos recursos pode ser restrito ou expandido, dependendo do que o cliente tem permissão para fazer.

Você pode optar por fazer com que um servidor represente um cliente ao se conectar a um banco de dados para que o banco de dados possa autenticar e autorizar o cliente por conta própria. Ou, se seu aplicativo acessar arquivos protegidos com um descritor de segurança e permitir que o cliente obtenha acesso autorizado às informações nesses arquivos, o aplicativo poderá representar o cliente antes de acessar os arquivos.

## <a name="how-to-implement-impersonation"></a>Como implementar a representação

A representação requer a participação do cliente e do servidor (e, em alguns casos, dos administradores do sistema). O cliente deve indicar sua disposição de permitir que o servidor use sua identidade, e o servidor deve assumir explicitamente a identidade do cliente programaticamente. Para obter detalhes, consulte os tópicos [Requisitos](client-side-requirements-for-impersonation.md) do lado do cliente para representação e requisitos [do lado do servidor para representação](server-side-requirements-for-impersonation.md).

## <a name="administrative-requirements-for-delegate-level-impersonation"></a>Requisitos administrativos para Delegate-Level representação

Para usar efetivamente a forma mais poderosa de *representação,* delegação , que é a representação de clientes pela rede, as contas de usuário cliente e servidor devem ser configuradas corretamente no Serviço do Active Directory para dar suporte a ele (além da autoridade de concessão do cliente para fazer a representação em nível delegado), da seguinte maneira:

-   A identidade do servidor deve ser marcada como "Confiável para delegação" no Serviço do Active Directory.
-   A identidade do cliente não deve ser marcada como "A conta é sensível e não pode ser delegada" no Serviço do Active Directory.

Esses recursos de configuração dão ao administrador de domínio um alto grau de controle sobre a delegação, o que é desejável, considerando a confiança (e, portanto, o risco de segurança) envolvido. Para obter mais detalhes sobre delegação, consulte [Delegação e representação.](/windows/desktop/com/delegation-and-impersonation)

## <a name="cloaking"></a>Camuflagem

Juntamente com a autoridade que um cliente concede a um servidor por meio do nível de representação, a capacidade de depuração do servidor determina em grande parte como a representação se comportará. A identificação afeta qual identidade é realmente apresentada pelo servidor quando ele faz chamadas em nome do cliente , sua própria identidade ou do cliente. Para obter detalhes, consulte [Detalhando](cloaking.md).

## <a name="performance-implications"></a>Implicações de desempenho

A representação pode afetar significativamente o desempenho e o dimensionamento. Geralmente, é mais caro representar um cliente em uma chamada do que fazer a chamada diretamente. A seguir estão alguns dos problemas a considerar:

-   A sobrecarga computacional de passar a identidade em padrões complicados, especialmente se a depuração dinâmica estiver habilitada.
-   A complexidade geral da imposição da verificação de segurança redundante em vários locais, em vez de apenas centralmente na camada intermediária.
-   Recursos como conexões de banco de dados, quando abertos representando um cliente, não podem ser reutilizados em vários clientes – um obstáculos muito grande para o dimensionamento bem.

Às vezes, a única solução eficaz para um problema é usar a representação, mas essa decisão deve ser cuidadosamente ponderada. Para ver mais uma discussão sobre esses problemas, consulte [Segurança de aplicativo de várias camadas.](multi-tier-application-security.md)

## <a name="queued-components"></a>Componentes na fila

[Os componentes na fila](com--queued-components.md) não são suportados para representação. Quando um cliente faz uma chamada para um objeto na fila, a chamada é realmente feita para o gravador, que o em pacotes como parte de uma mensagem para o servidor. Em seguida, o ouvinte lê a mensagem da fila e a passa para o player, que invoca o componente de servidor real e faz a mesma chamada de método. Assim, quando o servidor recebe a chamada, o token do cliente original fica indisponível por meio da representação. No entanto, a segurança baseada em função ainda se aplica e a segurança programática usando a interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) funcionará. Para obter detalhes, consulte [Segurança de componentes na fila.](queued-components-security.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação de cliente](client-authentication.md)
</dt> <dt>

[Segurança do aplicativo de biblioteca](library-application-security.md)
</dt> <dt>

[Segurança de aplicativos de várias camadas](multi-tier-application-security.md)
</dt> <dt>

[Segurança de componente programático](programmatic-component-security.md)
</dt> <dt>

[Administração de segurança baseada em função](role-based-security-administration.md)
</dt> <dt>

[Usando a política de restrição de software em COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
