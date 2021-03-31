---
title: Painéis de tarefas de serviço
description: Painéis de tarefas de serviço
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Lojas online do Windows Media Player, painéis de tarefas de serviço
- lojas online, painéis de tarefas de serviço
- Digite 2 lojas online, painéis de tarefas de serviço
- Repositórios online do Windows Media Player, painéis de tarefas
- lojas online, painéis de tarefas
- Digite 2 lojas online, painéis de tarefas
- Windows Media Player, painéis de tarefas de serviço
- Windows Media Player, painéis de tarefas
- painéis de tarefas de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f882e46a7252792db5b551b25869c7711f9d31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005664"
---
# <a name="service-task-panes"></a>Painéis de tarefas de serviço

No Windows Media Player 10, os provedores de loja online podem configurar o Windows Media Player para exibir até três painéis de tarefas, chamados painéis de tarefas de serviço. Cada painel de tarefas de serviço é representado por um botão personalizável que o Windows Media Player exibe no lado direito da barra de tarefas de recursos.

Cada painel de tarefas de serviço hospeda uma página da Web que é a interface do usuário para um recurso de loja online específico. A aparência dos painéis de tarefas de serviço é definida pelo documento XML serviceInfo. Neste documento, os painéis de tarefas de serviço são representados por três elementos: **ServiceTask1**, **ServiceTask2** e **ServiceTask3**. Esses painéis de tarefas de serviço têm a finalidade de fornecer o seguinte:

-   Um serviço de música.
-   Um serviço de vídeo.
-   Um serviço de rádio.

Você pode posicionar esses recursos no Windows Media Player em qualquer ordem que desejar, mas o **ServiceTask1** deve ser o painel de tarefas principal para envolver atividades comerciais.

A página da web hospedada em cada painel de tarefas de serviço tem acesso ao objeto **externo** . Esse objeto fornece métodos, propriedades e um evento que fornecem funcionalidade especial para páginas da Web no Windows Media Player. Por exemplo, você pode usar o evento e as propriedades de **externo** para fazer com que a aparência da página da Web corresponda ao esquema de cores escolhido pelo usuário para o Windows Media Player.

No Windows Media Player 11, não há painéis de tarefas de serviço. Em vez disso, há uma única guia **repositórios online** , que hospeda a página da Web principal para o repositório online ativo. No documento do serviceInfo, a guia **lojas online** é representada pelo elemento **ServiceTask1** ; os elementos **ServiceTask2** e **ServiceTask3** são ignorados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre as lojas online do tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Objeto externo para lojas online do tipo 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**Documento do serviceInfo para uma loja online tipo 2**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




