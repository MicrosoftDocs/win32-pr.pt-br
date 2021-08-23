---
title: Painéis de tarefas de serviço
description: Painéis de tarefas de serviço
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Windows Media Player lojas online, painéis de tarefas de serviço
- lojas online, painéis de tarefas de serviço
- Digite 2 lojas online, painéis de tarefas de serviço
- Windows Media Player lojas online, painéis de tarefas
- lojas online, painéis de tarefas
- Digite 2 lojas online, painéis de tarefas
- Windows Media Player, painéis de tarefas de serviço
- Windows Media Player, painéis de tarefas
- painéis de tarefas de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d445e3fa5393dddb8e3dcc835317c8e5a284cb46f0a4a0e2b1f65fe2ea2d7b30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646506"
---
# <a name="service-task-panes"></a>Painéis de tarefas de serviço

no Windows Media Player 10, os provedores de loja online podem configurar Windows Media Player para exibir até três painéis de tarefas, chamados painéis de tarefas de serviço. cada painel de tarefas de serviço é representado por um botão personalizável que Windows Media Player é exibido no lado direito da barra de tarefas de recursos.

Cada painel de tarefas de serviço hospeda uma página da Web que é a interface do usuário para um recurso de loja online específico. A aparência dos painéis de tarefas de serviço é definida pelo documento XML serviceInfo. Neste documento, os painéis de tarefas de serviço são representados por três elementos: **ServiceTask1**, **ServiceTask2** e **ServiceTask3**. Esses painéis de tarefas de serviço têm a finalidade de fornecer o seguinte:

-   Um serviço de música.
-   Um serviço de vídeo.
-   Um serviço de rádio.

você pode posicionar esses recursos em Windows Media Player em qualquer ordem que desejar, mas **ServiceTask1** deve ser o painel de tarefas principal para participar de atividades comerciais.

A página da web hospedada em cada painel de tarefas de serviço tem acesso ao objeto **externo** . Esse objeto fornece métodos, propriedades e um evento que fornecem funcionalidade especial para páginas da Web no Windows Media Player. Por exemplo, você pode usar o evento e as propriedades de **externo** para fazer com que a aparência da página da Web corresponda ao esquema de cores escolhido pelo usuário para Windows Media Player.

no Windows Media Player 11, não há painéis de tarefas de serviço. Em vez disso, há uma única guia **repositórios online** , que hospeda a página da Web principal para o repositório online ativo. No documento do serviceInfo, a guia **lojas online** é representada pelo elemento **ServiceTask1** ; os elementos **ServiceTask2** e **ServiceTask3** são ignorados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre as lojas online do tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Objeto externo para lojas online do tipo 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**Documento do serviceInfo para uma loja online tipo 2**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




