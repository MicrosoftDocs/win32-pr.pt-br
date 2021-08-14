---
description: Conceitos de partições COM+
ms.assetid: 9fc35bef-ecc1-4764-bf69-ec89560daff4
title: Conceitos de partições COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c4a2aaaf44d7c4346e4de44cfdb59ca0d75e593122342afe875a6eea71d9f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307963"
---
# <a name="com-partitions-concepts"></a>Conceitos de partições COM+

Em ambientes de computação em que é necessário usar diferentes versões ou configurações de um aplicativo no mesmo computador, os conflitos podem surgir quando uma versão do aplicativo requer componentes diferentes do outro ou quando uma versão requer um componente no computador que é incompatível com a outra versão do aplicativo. No passado, a única maneira de resolver esse problema era manter vários computadores e executar uma versão diferente do aplicativo em cada computador. Essa abordagem é dispendiosa e ineficiente porque aumenta os custos de hardware e a sobrecarga administrativa.

O COM+ resolve esse problema fornecendo o recurso de partições COM+. Você pode usar partições COM+ para instalar versões diferentes de um aplicativo COM+ em um computador e executá-las simultaneamente.

Para entender e usar esse recurso, consulte os seguintes tópicos:

-   [O que são partições COM+?](what-are-com--partitions-.md)
-   [Implementação de partição](partition-implementation.md)
-   [Registrando e ativando componentes em partições](registering-and-activating-components-in-partitions.md)
-   [Componentes e partições em fila COM+](com--queued-components-and-partitions.md)
-   [Restrições de design de aplicativo](application-design-restrictions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas de partições COM+](com--partitions-tasks.md)
</dt> </dl>

 

 



