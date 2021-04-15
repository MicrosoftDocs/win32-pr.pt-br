---
description: Um aplicativo COM+ é a principal unidade de administração e segurança para serviços de componentes e consiste em um grupo de componentes COM que geralmente executam funções relacionadas.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Visão geral do aplicativo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3365e0c0e7598d8f1eb2f466e8a2cea2d93edf4
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "105768420"
---
# <a name="com-application-overview"></a>Visão geral do aplicativo COM+

Um aplicativo COM+ é a principal unidade de administração e segurança para serviços de componentes e consiste em um grupo de componentes COM que geralmente executam funções relacionadas. Esses componentes consistem mais em interfaces e métodos, conforme mostrado na ilustração a seguir.

![Diagrama que mostra interfaces e métodos dentro de caixas, em ordem de método dentro da interface dentro do componente dentro do aplicativo COM+.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

Você pode usar a ferramenta administrativa serviços de componentes para criar novos aplicativos COM+, adicionar componentes a aplicativos e definir os atributos para um aplicativo e seus componentes.

Criando grupos lógicos de componentes COM como aplicativos COM+, você pode aproveitar os seguintes benefícios do COM+:

-   Um escopo de implantação para componentes COM.
-   Um escopo de configuração comum para componentes COM, incluindo limites de segurança e enfileiramento.
-   Armazenamento de atributos de componente não fornecidos pelo desenvolvedor de componentes (por exemplo, transações e sincronização).
-   Bibliotecas de vínculo dinâmico (DLLs) do componente carregadas em processos (DLLHost.exe) sob demanda.
-   Processos de servidor gerenciado para hospedar componentes.
-   Criação e gerenciamento de threads usados por componentes.
-   Acesso ao objeto de contexto para dispensadores de recursos, permitindo que os recursos adquiridos sejam associados automaticamente ao contexto. (Para obter mais informações sobre componentes COM e contextos, consulte [contextos do com+](com--contexts.md).)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo aplicativos COM+](developing-com--applications.md)
</dt> <dt>

[Partes de um aplicativo COM+](parts-of-a-com--application.md)
</dt> <dt>

[Tipos de aplicativos COM+](types-of-com--applications.md)
</dt> </dl>

 

 



