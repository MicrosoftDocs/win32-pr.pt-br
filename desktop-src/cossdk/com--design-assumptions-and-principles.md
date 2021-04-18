---
description: O modelo de programação distribuída da Microsoft consiste em várias tecnologias, incluindo MSMQ, IIS, DCOM e COM+. Todos esses serviços foram projetados para uso por aplicativos distribuídos.
ms.assetid: c72bbd47-0219-40ba-a7d5-2a6b725972d0
title: Princípios e pressuposições de design de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7dea86c404896a3d6095d39ebd6031767f6ccdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807258"
---
# <a name="com-design-assumptions-and-principles"></a>Princípios e pressuposições de design de COM+

O modelo de programação distribuída da Microsoft consiste em várias tecnologias, incluindo MSMQ, IIS, DCOM e COM+. Todos esses serviços foram projetados para uso por aplicativos distribuídos.

O COM+ foi desenvolvido para facilitar a criação de aplicativos distribuídos. A arquitetura geral é baseada em um conjunto de pressuposições e princípios.

## <a name="assumptions"></a>Suposições

As suposições são as seguintes:

-   **O aplicativo COM+ dará suporte a vários usuários em vários servidores.** Em outras palavras, você está criando um aplicativo distribuído, e esses vários usuários estarão em computadores host diferentes de onde o código é executado. Os usuários acessarão o código pela Internet ou por meio de uma rede privada. A interface do usuário será apresentada por meio do navegador ou talvez um aplicativo personalizado, como um aplicativo baseado em formulário escrito com o Microsoft Visual Basic ou o MFC. Essa interface do usuário será localizada no computador cliente.
-   **O aplicativo COM+ pode se tornar escalonável e pode fornecer maior disponibilidade e confiabilidade ao implantar o aplicativo em vários computadores servidores.** Ao fazer isso, você pode balancear a carga de trabalho do aplicativo e fornecer tolerância a falhas usando o clustering do Windows.
-   **Se as coisas forem erradas, o estado dos dados persistentes, armazenados em um banco de dado, de um aplicativo COM+ será mantido se você estiver usando transações.** O estado do aplicativo deve sobreviver a acidentes que podem ocorrer, como erros de aplicativo, falhas do sistema ou falhas de rede.

## <a name="principles"></a>Princípios

Além dessas três suposições, os princípios a seguir pervade o modelo de programação COM+:

-   **A lógica do aplicativo residirá em computadores do servidor, não em computadores cliente.** Há três motivos principais para fazer isso:
    -   O computador cliente pode não ter a capacidade de processamento ou os recursos necessários para executar a lógica do aplicativo. Além disso, manter a lógica do aplicativo no servidor simplifica a implantação.
    -   Os computadores do servidor geralmente estão mais próximos dos dados, e esses dados geralmente estão em um banco de dado. Como seu aplicativo está acessando bancos de dados, você deseja ser muito sensível ao custo das conexões de banco de dados. Ao colocar a maior parte da lógica nos computadores servidor, você pode compartilhar conexões de banco de dados e obter uma melhoria significativa no desempenho. Há outros recursos nos computadores servidor que também podem ser compartilhados, novamente com um benefício de desempenho.
    -   Ter a lógica de aplicativo residir em computadores de servidor mantém o controle do contexto de segurança com o aplicativo. Você terá mais controle sobre a segurança se mantiver essa segurança em componentes de aplicativos em execução em computadores servidores em vez de em computadores cliente.
-   **As transações são o núcleo.** Por design, as transações, portanto, percarnem o modelo de programação COM+ de que é muito importante para você entender. Embora você possa fazer uso de muitos dos serviços do COM+ sem usar transações, se optar por não usá-los, não poderá aproveitar ao máximo os serviços COM+ disponíveis para você. Alguns benefícios importantes do uso de transações incluem o seguinte:
    -   As transações são uma solução razoável para o problema do gerenciamento de simultaneidade. Além disso, as transações ajudam a proteger contra falhas e têm um bom modelo de recuperação de erro. Além disso, as transações são uma ótima maneira de gerenciar tarefas em vários sistemas.
    -   Você pode criar um aplicativo COM+ baseado em transações para trabalhar com um Gerenciador de recursos e um banco de dados, o que ajuda a proteger a maioria das informações de estado. Mantendo o estado dentro de um banco de dados ou algum outro armazenamento gerenciado por um Gerenciador de recursos, você não precisa manter muito o estado dentro dos objetos reais que seu aplicativo cria. Embora essa seja uma partida de um modelo puro orientado a objeto, ela funciona bem para a criação de aplicativos distribuídos com recuperação de erros.
-   **A funcionalidade do aplicativo é criada como objetos COM, encapsulando os protocolos usados para se comunicar com outros sistemas ou tecnologias.** Como você provavelmente está criando componentes que vão unir várias tecnologias ou sistemas herdados, planeje o uso de uma variedade de protocolos de comunicação. Use HTTP para comunicação de cliente/servidor ou comunicação entre aplicativos pela Internet. Use o DCOM para comunicação entre aplicativos ou componente para componente no servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes básicas para criar aplicativos COM+](basic-guidelines-for-designing-com--applications.md)
</dt> <dt>

[Criando o aplicativo COM+ usando UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Dicas de design gerais para usar o COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Otimizando interações com a camada de lógica de negócios do COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Outras ferramentas da Microsoft para a criação de aplicativos distribuídos](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



