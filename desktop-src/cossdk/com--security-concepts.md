---
description: O COM+ fornece vários recursos de segurança que você pode usar para ajudar a proteger seus aplicativos COM+, variando de serviços que você configura de forma administrativa para APIs que você pode chamar dentro de código.
ms.assetid: 686fb391-d337-41b4-bb51-b70f27a0c300
title: Conceitos de segurança do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca5126f4b715f84c2b8801c8ec1adc29b3cbb83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010268"
---
# <a name="com-security-concepts"></a>Conceitos de segurança do COM+

O COM+ fornece vários recursos de segurança que você pode usar para ajudar a proteger seus aplicativos COM+, variando de serviços que você configura de forma administrativa para APIs que você pode chamar dentro de código.

Sempre que possível, para aplicativos COM+, é melhor usar a segurança automática, como segurança e autenticação baseadas em função declarativa, em vez de configurar a segurança em componentes. O uso da segurança automática facilita escrever e manter componentes, facilitar o design de segurança em um aplicativo inteiro e, por ser configurado administrativamente, mais fácil de modificar a política de segurança de um aplicativo. Esses serviços de segurança automática possibilitam que você deixe toda a funcionalidade relacionada à segurança de seus componentes. Quando você puder ativar os serviços e configurá-los adequadamente, o COM+ manipulará os detalhes de impor a política de segurança que você especificar.

No entanto, quando os serviços de segurança automáticas no COM+ não fazem exatamente o que você precisa fazer, você pode estendê-los, criando a plataforma de segurança automática fornecida pelo COM+. Nos casos em que você optar por não usar a segurança automática ou onde deseja usá-la, mas precisar criá-la para atender aos requisitos de segurança do seu aplicativo, você tem as seguintes opções para configurar a segurança programaticamente:

-   Segurança baseada em função programática — por exemplo, verificação de função, que está disponível quando a segurança baseada em função está habilitada para seu aplicativo.
-   Representação — para quando você quiser usar a identidade de um cliente para acessar um recurso protegido.
-   Recursos de auditoria com base em informações de contexto de chamada de segurança — também disponíveis quando a segurança baseada em funções está habilitada.

Os mecanismos usados para ajudar a proteger um determinado aplicativo dependerão dos requisitos específicos desse aplicativo. Algumas opções de segurança podem afetar a maneira como você escreve componentes e algumas podem afetar significativamente o design do aplicativo. Antes de tomar decisões sobre como implementar uma estratégia de segurança para um aplicativo, você deve considerar seus requisitos de segurança no contexto de seu design geral — requisitos de desempenho, acesso a dados, design físico, e escolher a combinação mais adequada de recursos de segurança. Para obter mais informações sobre como implementar a segurança programática, consulte [programaticamente a segurança de componentes](programmatic-component-security.md).

As breves descrições de categorias de segurança, recursos e problemas do COM+ são fornecidas aqui, com links para tópicos nesta seção que fornecem uma discussão detalhada de cada uma das áreas importantes.

> [!Note]  
> Embora não discutido nesta seção, os componentes enfileirados também têm problemas específicos relacionados aos recursos de segurança disponíveis para eles. Para obter detalhes, consulte [segurança de componentes na fila](queued-components-security.md) e [desenvolvendo componentes enfileirados](developing-queued-components.md).

 

## <a name="role-based-security"></a>Segurança baseada em função

A segurança baseada em função é o recurso central da segurança do aplicativo COM+. Usando funções, você pode construir administrativamente uma política de autorização para um aplicativo, escolhendo (até o nível do método, se necessário) que os usuários podem acessar quais recursos. Além disso, as funções fornecem uma estrutura para impor a verificação de segurança no código se seu aplicativo exigir um controle de acesso refinado.

A segurança baseada em funções é criada em um mecanismo geral que permite que você recupere informações de segurança sobre todos os chamadores upstream na cadeia de chamadas para seu componente. Esse recurso será útil principalmente se você quiser fazer auditoria e log detalhados. Para obter uma descrição dos recursos de auditoria fornecidos pelo COM+, consulte [Acessando informações de contexto de chamada de segurança](accessing-security-call-context-information.md).

Para obter uma descrição de problemas de administração e segurança com base em função que você deve considerar ao usá-lo, consulte [Administração de segurança baseada em funções](role-based-security-administration.md).

## <a name="client-authentication"></a>Autenticação de cliente

Antes de autorizar os clientes a serem capazes de acessar os recursos, você deve ter certeza de que eles são quem dizem que estão. Para habilitar essa verificação de identidade, o COM+ fornece serviços de autenticação. Embora esses serviços sejam realmente fornecidos em um nível mais fundamental pelo COM e pelo Microsoft Windows, um aplicativo COM+ permite que você simplesmente ative o serviço de autenticação administrativamente para que ele funcione nos bastidores, transparente para o aplicativo. Para obter uma descrição dos serviços de autenticação, consulte [autenticação de cliente](client-authentication.md).

## <a name="client-impersonation-and-delegation"></a>Representação e delegação de cliente

Em alguns casos, seu aplicativo precisa fazer o trabalho em nome de um cliente usando a identidade do cliente, por exemplo, ao acessar um banco de dados que irá autenticar o cliente original. Isso exige que seu aplicativo represente o cliente. O COM+ fornece recursos para habilitar vários níveis de representação. A representação é configurada administrativamente, mas você também deve fornecer suporte para representação com o código dos componentes do seu aplicativo. Para obter uma descrição da representação e dos problemas relacionados a seu uso, consulte [representação e delegação do cliente](client-impersonation-and-delegation.md).

## <a name="using-the-software-restriction-policy-in-com"></a>Usando a política de restrição de software no COM+

Uma diretiva de restrição de software fornece uma maneira de executar código não confiável e, portanto, potencialmente prejudicial, em um ambiente restrito para que não seja possível fazer uso incorreto dos privilégios do usuário. Ele faz isso atribuindo níveis de confiança a arquivos que o usuário pode executar. Por exemplo, determinados arquivos do sistema podem ser totalmente confiáveis e receber acesso irrestrito aos privilégios do usuário, enquanto um arquivo que foi baixado da Internet pode ser completamente não confiável e, portanto, pode ser executado somente em um ambiente restrito no qual não é permitido usar nenhum privilégio de usuário sensível à segurança.

A diretiva de restrição de software de todo o grupo é controlada por meio da ferramenta administrativa diretiva de segurança local, que permite aos administradores configurar níveis de confiança para arquivos individuais. No entanto, todos os aplicativos do servidor COM+ são executados no arquivo dllhost.exe. Portanto, o COM+ fornece uma maneira de especificar a diretiva de restrição de software para cada aplicativo de servidor para que eles não precisem depender da diretiva de restrição do arquivo de dllhost.exe. Para obter uma discussão sobre como usar a política de restrição de software no COM+, consulte [usando a política de restrição de software no com+](using-the-software-restriction-policy-in-com-.md).

## <a name="library-application-security"></a>Segurança de aplicativos de biblioteca

Os aplicativos de biblioteca têm considerações de segurança especiais. Como esses aplicativos são executados no processo do cliente, eles são afetados pela segurança imposta pelo processo de hospedagem, enquanto não é possível controlar a segurança em nível de processo. Para obter uma descrição dos fatores a serem considerados para aplicativos de biblioteca, consulte [segurança de aplicativo de biblioteca](library-application-security.md).

## <a name="multi-tier-application-security"></a>Segurança de aplicativos de várias camadas

Aplicativos COM+ normalmente são aplicativos de camada intermediária; ou seja, eles movem informações entre clientes e recursos de back-end, como bancos de dados. Opções difíceis podem ser envolvidas na determinação de onde a segurança deve ser imposta e em que grau. Segurança inerentemente envolve compensações de desempenho. Algumas das mais graves ocorrem quando você deve impor a verificação de segurança na camada de dados e na camada intermediária. Para obter uma discussão sobre problemas a serem considerados, consulte [segurança de aplicativos de várias camadas](multi-tier-application-security.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação de cliente](client-authentication.md)
</dt> <dt>

[Representação e delegação de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Tarefas de segurança do COM+](com--security-tasks.md)
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

 

 



