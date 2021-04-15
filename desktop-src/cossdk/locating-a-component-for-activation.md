---
description: Localizando um componente para ativação
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Localizando um componente para ativação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bd90068c34469d61af36e6de8c409cb02e078c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104554837"
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

 

 



