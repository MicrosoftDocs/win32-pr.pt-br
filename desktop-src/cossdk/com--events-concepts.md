---
description: Conceitos de eventos COM+
ms.assetid: 6bfe4852-4029-4dd4-92ad-3061618b1b23
title: Conceitos de eventos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811dbca17c4e90ba5e8c2bcb8c918ce6634487e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646546"
---
# <a name="com-events-concepts"></a>Conceitos de eventos COM+

O serviço de eventos COM+ é um sistema de eventos automatizado e *menos* rígido que armazena informações de eventos de editores diferentes no catálogo com+. Os assinantes podem consultar esse repositório de eventos e selecionar os eventos sobre os quais desejam saber.

> [!Note]  
> Um *evento* é identificado por um método em uma interface com+, conhecido como um *método de evento*, e é originado por um Publicador e despachado para o assinante ou assinantes corretos por meio do serviço de eventos com+. Os métodos de evento devem ser nomeados exclusivamente e podem conter apenas parâmetros de entrada (sem parâmetros de saída ou de entrada/saída). O valor de retorno deve ser um **HRESULT**.

 

O serviço de eventos COM+ lida com a maioria das semânticas de evento para o Publicador e o Assinante. Os editores oferecem para publicar tipos de evento e os assinantes solicitam tipos de evento de Publicadores. Ao contrário de um sistema de *eventos rigidamente acoplado* , em que os editores devem lidar com a sobrecarga dos assinantes de chamada diretamente, o serviço de eventos com+ mantém os dados de assinatura no catálogo com+, independentemente do Publicador e do Assinante. Isso simplifica o modelo de programação para o Publicador e o assinante porque o componente de assinante do COM+ não precisa conter a lógica para a criação de assinaturas.

Como o ciclo de vida dos dados de assinatura de eventos COM+ é separado do Publicador ou do Assinante, as assinaturas podem ser criadas antes que o assinante ou os aplicativos do Publicador estejam ativos. Isso também significa que os editores e assinantes podem ser desenvolvidos e implantados separadamente. O Publicador pode ser escrito sem o conhecimento do número e do local dos assinantes. Os assinantes usam o serviço de eventos COM+ para localizar o Publicador e gerenciar suas assinaturas.

Os tópicos a seguir nesta seção fornecem informações detalhadas sobre os principais elementos do serviço de eventos COM+ e como usá-los.

-   [O objeto de classe de evento COM+](the-com--event-class-object.md)
-   [Assinaturas](subscriptions.md)
-   [Publicando e fornecendo eventos no COM+](publishing-and-delivering-events-in-com-.md)
-   [Filtrando eventos no COM+](filtering-events-in-com-.md)
-   [Usando eventos COM+ com componentes em fila COM+](using-com--events-with-com--queued-components.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Considerações de segurança de eventos COM+](com--events-security-considerations.md)
</dt> <dt>

[Tarefas de eventos COM+](com--events-tasks.md)
</dt> </dl>

 

 



