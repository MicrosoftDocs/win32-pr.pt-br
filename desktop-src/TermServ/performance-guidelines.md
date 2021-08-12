---
title: Diretrizes de desempenho
description: Diretrizes para o desenvolvimento de aplicativos que têm bom desempenho em um ambiente de Serviços de Área de Trabalho Remota.
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97a8211f12e4a89c5dfb309bb4e3c0f998159738b46185aeb5dcee7a5cd29f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605308"
---
# <a name="performance-guidelines"></a>Diretrizes de desempenho

As seções a seguir fornecem diretrizes para o desenvolvimento de aplicativos que têm bom desempenho em um ambiente de Serviços de Área de Trabalho Remota.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Efeitos gráficos](graphic-effects.md)
</dt> <dd>

Uma lista de recursos que devem ser desabilitados durante a execução como uma sessão remota em um ambiente de Serviços de Área de Trabalho Remota.

</dd> <dt>

[Diretrizes para tarefas em segundo plano no Serviços de Área de Trabalho Remota](background-tasks.md)
</dt> <dd>

Para maximizar a disponibilidade da CPU para todos os usuários, desabilite as tarefas em segundo plano ao executar em um ambiente de Serviços de Área de Trabalho Remota ou crie tarefas em segundo plano eficientes que não usam muitos recursos.

</dd> <dt>

[Uso de thread](thread-usage.md)
</dt> <dd>

Você deve ajustar e balancear o uso de threads de aplicativo para um ambiente multiusuário, multiprocessador Serviços de Área de Trabalho Remota.

</dd> <dt>

[Detectando o ambiente de Serviços de Área de Trabalho Remota](detecting-the-terminal-services-environment.md)
</dt> <dd>

Para otimizar o desempenho, é uma boa prática para os aplicativos detectarem se eles estão sendo executados em uma sessão de cliente Serviços de Área de Trabalho Remota.

</dd> </dl>

Verifique se há vazamento de memória no aplicativo e resolva quaisquer problemas. É claro que esse é um bom conselho para qualquer aplicativo, mas em um ambiente de Serviços de Área de Trabalho Remota, um aplicativo pode ser executado várias vezes por vários usuários, aumentando rapidamente o efeito de um vazamento de memória.

Animações, imagens grandes, áudio e outros serviços com uso intensivo de largura de banda devem ser configuráveis. Quando esses serviços não são a função principal, eles podem estar desativados por padrão para sessões remotas, mas habilitados quando uma sessão está em execução localmente ou em uma conexão de largura de banda alta. Se a finalidade de um aplicativo é fornecer serviços de alta largura de banda, como streaming de transmissão de vídeo, o serviço não precisa estar desativado por padrão.

 

 




