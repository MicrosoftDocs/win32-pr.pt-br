---
description: O modelo de arquitetura de três camadas, que é a estrutura fundamental para o modelo de design lógico, segmenta os componentes de aplicativos em três camadas de serviços.
ms.assetid: a03327c1-e427-4c07-b3d4-808ce81c2c96
title: Usando um modelo de arquitetura de Three-Tier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20b765a6d103f3c349ffd9a44853f495c64a070
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370485"
---
# <a name="using-a-three-tier-architecture-model"></a>Usando um modelo de arquitetura de Three-Tier

O modelo de arquitetura de três camadas, que é a estrutura fundamental para o [modelo de design lógico](the-logical-model--application-definition-and-planning.md), segmenta os componentes de um aplicativo em três camadas de serviços. Essas camadas não correspondem necessariamente a locais físicos em vários computadores em uma rede, mas sim a camadas lógicas do aplicativo. A forma como as partes de um aplicativo são distribuídas em uma topologia física pode mudar, dependendo dos requisitos do sistema.

Veja a seguir descrições breves dos serviços alocados para cada camada:

-   **A camada de apresentação, ou de serviços de usuário, fornece a um usuário acesso ao aplicativo.** Essa camada apresenta dados para o usuário e, opcionalmente, permite a manipulação de dados e a entrada de dados. Os dois tipos principais de interface do usuário para essa camada são o aplicativo tradicional e o aplicativo baseado na Web. Agora, os aplicativos baseados na Web contêm a maioria dos recursos de manipulação de dados usados pelos aplicativos tradicionais. Isso é feito por meio do uso de fontes de dados HTML e do cliente dinâmicos e de cursores de dados.

    > [!Note]  
    > Em um aplicativo de três camadas, o aplicativo do lado do cliente será skinnier do que um aplicativo cliente-servidor, pois ele não conterá os componentes de serviço agora localizados na camada intermediária. Isso resulta em menos sobrecarga para o usuário, mas mais tráfego de rede para o sistema porque os componentes são distribuídos entre diferentes máquinas.

     

-   **A camada intermediária, ou de serviços comerciais, consiste em regras de negócios e dados.** Também conhecida como a *camada de lógica de negócios*, a camada intermediária é onde os desenvolvedores de com+ podem resolver problemas de negócios críticos e atingir grandes vantagens de produtividade. Os componentes que compõem essa camada podem existir em um computador servidor, para auxiliar no compartilhamento de recursos. Esses componentes podem ser usados para impor regras de negócio, como algoritmos de negócios e regulamentos legais ou governamentais, além de regras de dados, que são projetadas para manter as estruturas de dados consistentes em um ou vários bancos de dado. Como esses componentes de camada intermediária não estão vinculados a um cliente específico, eles podem ser usados por todos os aplicativos e podem ser movidos para locais diferentes, pois o tempo de resposta e outras regras exigem. Por exemplo, edições simples podem ser colocadas no lado do cliente para minimizar viagens de ida e volta da rede, ou as regras de dados podem ser colocadas em procedimentos armazenados.

-   **A camada de dados, ou de serviços de dados, interage com os dados persistentes geralmente armazenados em um banco de dado ou em um armazenamento permanente.** Essa é a camada de acesso do DBMS real. Ele pode ser acessado por meio da camada de serviços corporativos e ocasionalmente pela camada de serviços do usuário. Essa camada consiste em componentes de acesso a dados (em vez de conexões brutas de DBMS) para auxiliar no compartilhamento de recursos e permitir que os clientes sejam configurados sem instalar as bibliotecas DBMS e os drivers ODBC em cada cliente.

Durante o ciclo de vida de um aplicativo, a abordagem de três camadas fornece benefícios como reutilização, flexibilidade, capacidade de gerenciamento, facilidade de manutenção e escalabilidade. Você pode compartilhar e reutilizar os componentes e serviços criados por você e pode distribuí-los em uma rede de computadores, conforme necessário. Você pode dividir projetos grandes e complexos em projetos mais simples e atribuí-los a programadores ou equipes de programação diferentes. Você também pode implantar componentes e serviços em um servidor para ajudar a acompanhar as alterações e pode reimplantá-las como crescimento da base de usuários, dos dados e do volume de transações do aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O modelo lógico: definição e planejamento de aplicativos](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



