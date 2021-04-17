---
description: Um componente COM configurado geralmente é ativado em seu próprio contexto; ou seja, o COM+ faz referência às informações do catálogo de componentes para fornecer quaisquer serviços configurados.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Impondo ativação no contexto padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41599f71dc37c37c1a9a574d274ca2858835e2df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501128"
---
# <a name="enforcing-activation-in-the-default-context"></a>Impondo ativação no contexto padrão

Um componente COM configurado geralmente é ativado em seu próprio contexto; ou seja, COM+ faz referência às informações de catálogo do componente para fornecer quaisquer serviços configurados. No entanto, você pode optar por ativar um componente configurado no contexto padrão. Um componente COM base — um componente registrado que não tem informações de catálogo COM+ — geralmente é ativado no contexto padrão.

Ativar um componente COM no contexto padrão fornece três principais benefícios de desempenho, da seguinte maneira:

-   Você salva os recursos do sistema limitando o número de contextos que são criados.
-   Você aumenta o desempenho limitando o número de chamadas de contexto cruzado. Como as chamadas entre contextos exigem marshaling, é muito mais rápida para um objeto COM ativado no contexto padrão para fazer chamadas para outros objetos no contexto padrão. O desempenho nesse caso (de chamadas dentro do mesmo contexto) é semelhante ao de chamar uma sub-rotina.
-   Você pode importar aplicativos COM mais antigos para o COM+ e executá-los sem problemas. Por exemplo, você pode ter vários aplicativos COM mais antigos implementados sob a suposição de que era possível passar referências de objeto em um apartamento sem realizar marshaling das referências. Esses aplicativos COM não funcionam quando importados para o COM+ porque as referências de objeto são passadas entre limites de contexto. No entanto, você pode fazer COM que esse tipo de aplicativo COM seja executado quando importado se você usar a ferramenta administrativa serviços de componentes para marcar todas as classes no aplicativo como **deve ser ativado no contexto padrão**.

A principal desvantagem de ativar um componente configurado no contexto padrão é que o COM+ não fornece nenhum dos serviços configurados do componente. Há uma compensação entre o desempenho aprimorado e a capacidade de usar os serviços COM+.

Por exemplo, suponha que um componente COM não exija serviços COM+ (como [Transações](com--transactions.md), [ativação Just-in-time](com--just-in-time-activation.md), [eventos](com--events.md), [componentes enfileirados](com--queued-components.md), [sincronização](com--synchronization.md)ou [pool de objetos](com--object-pooling.md)) e que o componente faça várias chamadas para outros componentes com que possam ser ativados no contexto padrão. Nesse caso, seria uma boa ideia ativar o componente de chamada no contexto padrão.

Se o componente COM exigir serviços COM+, ele não poderá ser marcado como **deve ser ativado no contexto padrão**. Além disso, não haverá nenhum benefício de desempenho real se um objeto COM ativado no contexto padrão fizer várias chamadas para objetos em outros contextos. (Para obter mais detalhes, consulte [contextos](com--contexts.md).)

**Para impor a ativação no contexto padrão**

1.  No painel de detalhes da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no componente (localizado na pasta **componentes** de qualquer aplicativo com+ selecionado) que você deseja ativar no contexto padrão e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do componente, clique na guia **ativação** .

3.  Selecione a caixa de seleção **deve ser ativada no contexto padrão**.

4.  Clique em **OK**.

> [!Note]  
> Quando você executa um componente configurado no contexto padrão, o COM+ não ativa nenhum dos serviços configurados para esse componente. Esses serviços estão disponíveis novamente quando você desmarca a caixa de seleção **deve ser ativada no contexto padrão** e, posteriormente, executa o componente configurado em seu próprio contexto.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de ativação Just-in-time COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Impondo a ativação no contexto do chamador](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



