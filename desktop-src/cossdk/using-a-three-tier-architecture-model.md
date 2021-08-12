---
description: O modelo de arquitetura de três camadas, que é a estrutura fundamental para o modelo de design lógico, segmenta componentes de aplicativos em três camadas de serviços.
ms.assetid: a03327c1-e427-4c07-b3d4-808ce81c2c96
title: Usando um modelo Three-Tier arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd08ee1363504c610ed650d59b3837d292fb3a1d447c882dbd39ddba6229503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546053"
---
# <a name="using-a-three-tier-architecture-model"></a>Usando um modelo Three-Tier arquitetura

O modelo de arquitetura de três camadas, que é a estrutura fundamental para o modelo de [design](the-logical-model--application-definition-and-planning.md)lógico, segmenta os componentes de um aplicativo em três camadas de serviços. Essas camadas não correspondem necessariamente a locais físicos em vários computadores em uma rede, mas sim a camadas lógicas do aplicativo. Como as partes de um aplicativo são distribuídas em uma topologia física podem mudar, dependendo dos requisitos do sistema.

A seguir estão breves descrições dos serviços alocados para cada camada:

-   **A camada de apresentação ou a camada de serviços do usuário fornece a um usuário acesso ao aplicativo.** Essa camada apresenta dados para o usuário e, opcionalmente, permite a manipulação de dados e a entrada de dados. Os dois principais tipos de interface do usuário para essa camada são o aplicativo tradicional e o aplicativo baseado na Web. Aplicativos baseados na Web agora geralmente contêm a maioria dos recursos de manipulação de dados que os aplicativos tradicionais usam. Isso é feito por meio do uso de cursores de dados e fontes de dados dinâmicas do lado do cliente e HTML.

    > [!Note]  
    > Em um aplicativo de três camadas, o aplicativo do lado do cliente será mais rápido do que um aplicativo cliente-servidor porque ele não conterá os componentes de serviço agora localizados na camada intermediária. Isso resulta em menos sobrecarga para o usuário, mas mais tráfego de rede para o sistema porque os componentes são distribuídos entre diferentes máquinas.

     

-   **A camada intermediária, ou camada de serviços de negócios, consiste em regras de negócios e dados.** Também conhecida como camada de *lógica* de negócios, a camada intermediária é onde os desenvolvedores COM+ podem resolver problemas de negócios críticos e obter grandes vantagens de produtividade. Os componentes que comem essa camada podem existir em um computador servidor, para auxiliar no compartilhamento de recursos. Esses componentes podem ser usados para impor regras de negócios, como algoritmos de negócios e regulamentos legais ou governamentais e regras de dados, que são projetadas para manter as estruturas de dados consistentes em bancos de dados específicos ou múltiplos. Como esses componentes de camada intermediária não estão vinculados a um cliente específico, eles podem ser usados por todos os aplicativos e podem ser movidos para locais diferentes, como o tempo de resposta e outras regras exigem. Por exemplo, edições simples podem ser colocadas no lado do cliente para minimizar as viagens de ida e volta da rede ou as regras de dados podem ser colocadas em procedimentos armazenados.

-   **A camada de dados, ou camada de serviços de dados, interage com dados persistentes geralmente armazenados em um banco de dados ou em armazenamento permanente.** Essa é a camada de acesso real do DBMS. Ele pode ser acessado por meio da camada de serviços de negócios e, às vezes, pela camada de serviços do usuário. Essa camada consiste em componentes de acesso a dados (em vez de conexões DBMS brutas) para auxiliar no compartilhamento de recursos e permitir que os clientes sejam configurados sem instalar as bibliotecas dbMS e os drivers ODBC em cada cliente.

Durante o ciclo de vida de um aplicativo, a abordagem de três camadas oferece benefícios como reutilização, flexibilidade, capacidade de gerenciamento, capacidade de manutenção e escalabilidade. Você pode compartilhar e reutilizar os componentes e serviços que cria e distribuí-los em uma rede de computadores, conforme necessário. Você pode dividir projetos grandes e complexos em projetos mais simples e atribuí-los a diferentes programadores ou equipes de programação. Você também pode implantar componentes e serviços em um servidor para ajudar a acompanhar as alterações e reimplantá-las à medida que o crescimento da base de usuários, dos dados e do volume de transações do aplicativo aumenta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O modelo lógico: definição e planejamento de aplicativos](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



