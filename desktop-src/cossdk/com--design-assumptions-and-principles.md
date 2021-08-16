---
description: O modelo de programação distribuída da Microsoft consiste em várias tecnologias, incluindo MSMQ, IIS, DCOM e COM+. Todos esses serviços foram projetados para uso por aplicativos distribuídos.
ms.assetid: c72bbd47-0219-40ba-a7d5-2a6b725972d0
title: Suposições e princípios de design COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b87c5ae631cd5517b215efae3a09968649cd49ea94fe33b33d9b826082e911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549391"
---
# <a name="com-design-assumptions-and-principles"></a>Suposições e princípios de design COM+

O modelo de programação distribuída da Microsoft consiste em várias tecnologias, incluindo MSMQ, IIS, DCOM e COM+. Todos esses serviços foram projetados para uso por aplicativos distribuídos.

O COM+ foi desenvolvido para facilitar a criação de aplicativos distribuídos. A arquitetura geral baseia-se em um conjunto de suposições e princípios.

## <a name="assumptions"></a>Suposições

As suposições são as seguinte:

-   **O aplicativo COM+ dará suporte a vários usuários em vários servidores.** Em outras palavras, você está criando um aplicativo distribuído e esses vários usuários estarão em computadores host diferentes dos quais o código é executado. Os usuários acessarão o código pela Internet ou por meio de uma rede privada. A interface do usuário será apresentada por meio do navegador ou talvez de um aplicativo personalizado, como um aplicativo baseado em formulário escrito com Microsoft Visual Basic ou MFC. Essa interface do usuário estará localizada no computador cliente.
-   **O aplicativo COM+ pode ser escalonável e pode fornecer maior disponibilidade e confiabilidade implantando o aplicativo em vários computadores de servidor.** Ao fazer isso, você pode equilibrar a carga de trabalho do aplicativo e fornecer tolerância a falhas usando Windows Clustering.
-   **Se as coisas derem errado, o estado dos dados persistentes, armazenados em um banco de dados, de um aplicativo COM+ será mantido se você estiver usando transações.** O estado do aplicativo deve sobreviver a acidentes que podem ocorrer, como erros de aplicativo, falhas do sistema ou falhas de rede.

## <a name="principles"></a>Princípios

Além dessas três suposições, os seguintes princípios permeiam o modelo de programação COM+:

-   **A lógica do aplicativo residirá em computadores servidores, não em computadores cliente.** Há três motivos principais para fazer isso:
    -   O computador cliente pode não ter o poder de processamento ou os recursos necessários para executar a lógica do aplicativo. Além disso, manter a lógica do aplicativo no servidor simplifica a implantação.
    -   Os computadores de servidor geralmente estão mais próximos dos dados e esses dados geralmente estão em um banco de dados. Como seu aplicativo está acessando bancos de dados, você deseja ser muito sensível ao custo das conexões de banco de dados. Ao colocar a maior parte da lógica nos computadores servidores, você pode compartilhar conexões de banco de dados e obter uma melhoria significativa no desempenho. Há outros recursos nos computadores servidores que também podem ser compartilhados, novamente com um benefício de desempenho.
    -   Fazer com que a lógica do aplicativo resida em computadores servidores mantém o controle do contexto de segurança com o aplicativo. Você terá mais controle sobre a segurança se mantiver essa segurança em componentes de aplicativo em execução em computadores servidores em vez de em computadores cliente.
-   **As transações são o núcleo.** Por design, as transações tão desafoque o modelo de programação COM+ que é muito importante que você as entenda. Embora você possa usar muitos dos serviços do COM+ sem usar transações, se optar por não usá-los, não poderá aproveitar ao máximo os serviços COM+ disponíveis para você. Alguns benefícios importantes do uso de transações incluem o seguinte:
    -   As transações são uma solução razoável para o problema de gerenciamento de competência. Além disso, as transações ajudam a proteger contra falhas e têm um bom modelo de recuperação de erros. Além disso, as transações se transformam em uma ótima maneira de gerenciar tarefas em vários sistemas.
    -   Você pode criar um aplicativo COM+ baseado em transação para trabalhar com um gerenciador de recursos e um banco de dados, o que ajuda a proteger a maioria das informações de estado. Ao manter o estado dentro de um banco de dados ou algum outro armazenamento gerenciado por um gerenciador de recursos, você não precisa manter muito estado dentro dos objetos reais que seu aplicativo cria. Embora essa seja uma partida de um modelo orientado a objeto puro, ele funciona bem para criar aplicativos distribuídos com recuperação de erro.
-   **A funcionalidade do aplicativo é criada como objetos COM, envolvendo os protocolos usados para se comunicar com outros sistemas ou tecnologias.** Como você provavelmente está criando componentes que unirão várias tecnologias ou sistemas herdados, planeje usar uma variedade de protocolos de comunicação. Use HTTP para comunicação de cliente/servidor ou comunicação de aplicativo para aplicativo pela Internet. Use o DCOM para comunicação de aplicativo para aplicativo ou componente para componente no servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes básicas para a criação de aplicativos COM+](basic-guidelines-for-designing-com--applications.md)
</dt> <dt>

[Projetando o aplicativo COM+ usando UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Design geral Dicas para usar COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Otimizando interações com a camada lógica de negócios COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Outras ferramentas da Microsoft para a criação de aplicativos distribuídos](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



