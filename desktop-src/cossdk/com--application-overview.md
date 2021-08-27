---
description: Um aplicativo COM+ é a principal unidade de administração e segurança dos Serviços de Componentes e consiste em um grupo de componentes COM que geralmente executam funções relacionadas.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Visão geral do aplicativo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c964d760b5ba0ef260bc9dcb0658b564a4b211075692ce6301a0445eee0eb7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991867"
---
# <a name="com-application-overview"></a>Visão geral do aplicativo COM+

Um aplicativo COM+ é a principal unidade de administração e segurança dos Serviços de Componentes e consiste em um grupo de componentes COM que geralmente executam funções relacionadas. Esses componentes consistem ainda em interfaces e métodos, conforme mostrado na ilustração a seguir.

![Diagrama que mostra interfaces e métodos dentro de caixas, na ordem de Método dentro da Interface dentro do Componente dentro do Aplicativo COM+.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

Você pode usar a ferramenta administrativa serviços de componentes para criar novos aplicativos COM+, adicionar componentes a aplicativos e definir os atributos para um aplicativo e seus componentes.

Ao criar grupos lógicos de componentes COM como aplicativos COM+, você pode aproveitar os seguintes benefícios do COM+:

-   Um escopo de implantação para componentes COM.
-   Um escopo de configuração comum para componentes COM, incluindo limites de segurança e fila.
-   Armazenamento atributos de componente não fornecidos pelo desenvolvedor do componente (por exemplo, transações e sincronização).
-   DLLs (bibliotecas de vínculo dinâmico) do componente carregadas em processos (DLLHost.exe) sob demanda.
-   O servidor gerenciado processa para hospedar componentes.
-   Criação e gerenciamento de threads usados pelos componentes.
-   Acesso ao objeto de contexto para os distribuidores de recursos, permitindo que os recursos adquiridos sejam associados automaticamente ao contexto. (Para obter mais informações sobre contextos e componentes COM, consulte [Contextos COM+.)](com--contexts.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo aplicativos COM+](developing-com--applications.md)
</dt> <dt>

[Partes de um aplicativo COM+](parts-of-a-com--application.md)
</dt> <dt>

[Tipos de aplicativos COM+](types-of-com--applications.md)
</dt> </dl>

 

 



