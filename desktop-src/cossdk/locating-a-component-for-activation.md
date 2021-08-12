---
description: Localizando um componente para ativação
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Localizando um componente para ativação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51badf0b33f7c133cdea1fa95c859c2f36e282bc748c75c560d57abeead802c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306210"
---
# <a name="locating-a-component-for-activation"></a>Localizando um componente para ativação

Quando o COM+ tiver localizado a partição correta — por meio do conjunto de partições padrão da identidade do usuário, um moniker da partição ou a ID da partição no contexto do objeto, COM + deverá localizar o componente correto dentro dessa partição. A ilustração a seguir mostra como um componente é encontrado e ativado quando esse componente reside em uma partição.

> [!Note]  
> Antes de qualquer ativação de componente, COM+ executa uma validação para verificar se a identidade do usuário que está tentando ativar o componente tem direitos para acessar o conjunto de partições no qual o componente reside.

 

![Diagrama que mostra uma árvore de solução de problemas para localizar um componente para ativação.](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

A ilustração anterior mostra o seguinte:

-   Se o componente que está sendo chamado residir em uma partição e estiver no mesmo aplicativo que o componente de chamada, o componente será ativado se o componente que está sendo chamado estiver marcado como público ou privado.
-   Se o componente que está sendo chamado residir em uma partição, mas não existir no mesmo aplicativo que o componente de chamada, o COM+ verificará se o componente está marcado como público. Se nenhuma versão pública for encontrada, o COM+ pesquisará a partição global para localizar uma versão pública do componente. Se nenhuma versão pública do componente for encontrada na partição global ou se a identidade do usuário não tiver direitos para a partição, a ativação falhará.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Localizando partições durante a ativação](locating-partitions-during-activation.md)
</dt> </dl>

 

 



