---
description: Um componente COM configurado geralmente é ativado em seu próprio contexto; ou seja, COM+ faz referência às informações do catálogo de componentes para fornecer quaisquer serviços configurados.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Impondo a ativação no contexto padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d188fb50521e09c88a9c61136e33928176faa1f70a94680b31cf0cc1e75cb8eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070756"
---
# <a name="enforcing-activation-in-the-default-context"></a>Impondo a ativação no contexto padrão

Um componente COM configurado geralmente é ativado em seu próprio contexto; ou seja, COM+ faz referência às informações do catálogo do componente para fornecer quaisquer serviços configurados. No entanto, você pode optar por ativar um componente configurado no contexto padrão. Um componente COM base – um componente registrado que não tem informações de catálogo COM+ – geralmente é ativado no contexto padrão.

A ativação de um componente COM no contexto padrão oferece três benefícios principais de desempenho, da seguinte forma:

-   Salve os recursos do sistema limitando o número de contextos criados.
-   Você aumenta o desempenho limitando o número de chamadas entre contextos. Como as chamadas entre contextos exigem marshaling, é muito mais rápido para um objeto COM ativado no contexto padrão fazer chamadas para outros objetos no contexto padrão. Nesse caso, o desempenho (de chamadas dentro do mesmo contexto) é semelhante ao de chamar uma sub-rotina.
-   Você pode importar aplicativos COM mais antigos para COM+ e execute-os sem problemas. Por exemplo, você pode ter vários aplicativos COM mais antigos implementados com a suposição de que era possível passar referências de objeto dentro de um apartment sem marshaling das referências. Esses aplicativos COM não funcionam quando importados para COM+ porque as referências de objeto são passadas entre limites de contexto. No entanto, você pode fazer com que esse tipo de aplicativo COM seja executado quando importado se você usar a ferramenta administrativa dos Serviços de Componentes para marcar todas as classes no aplicativo como Deve ser ativada no **contexto padrão**.

A principal desvantagem de ativar um componente configurado no contexto padrão é que o COM+ não fornece nenhum dos serviços configurados do componente. Há uma troca entre o desempenho aprimorado e a capacidade de usar serviços COM+.

Por exemplo, suponha que um componente COM não exige nenhum serviço COM+ (como Transações, Ativação [](com--synchronization.md) [Just-In-Time,](com--just-in-time-activation.md)Eventos [,](com--events.md)Componentes En en ensuados, [](com--queued-components.md)Sincronização ou [Pooling](com--object-pooling.md)de Objetos ) e que o componente faça várias chamadas para outros [componentes](com--transactions.md)COM que podem ser ativados no contexto padrão. Nesse caso, seria uma boa ideia ativar o componente de chamada no contexto padrão.

Se o componente COM exigir serviços COM+, ele não poderá ser marcado como **Deve ser ativado no contexto padrão**. Além disso, não haverá nenhum ganho real de desempenho se um objeto COM ativado no contexto padrão fizer várias chamadas a objetos em outros contextos. (Para obter mais detalhes, consulte [Contextos](com--contexts.md).)

**Para impor a ativação no contexto padrão**

1.  No painel de detalhes da ferramenta administrativa serviços de componentes,  clique com o botão direito do mouse no componente (localizado na pasta Componentes de qualquer aplicativo COM+ selecionado) que você deseja ativar no contexto padrão e clique em **Propriedades**.

2.  Na caixa de diálogo propriedades do componente, clique na **guia Ativação.**

3.  Marque a **caixa de seleção Deve ser ativada na caixa de seleção de contexto** padrão.

4.  Clique em **OK**.

> [!Note]  
> Quando você executar um componente configurado no contexto padrão, o COM+ não ativará nenhum dos serviços configurados para esse componente. Esses serviços estão disponíveis novamente quando você desmarca a caixa de seleção Deve ser ativada no contexto padrão e, posteriormente, executar o componente configurado em seu próprio contexto.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de ativação Just-In-Time do COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Impondo a ativação no contexto do chamador](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



