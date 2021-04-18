---
description: Impondo a ativação no contexto de chamadores
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Impondo a ativação no contexto de chamadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70af40f92056e679a9211964b8a614cbeaeb4a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760426"
---
# <a name="enforcing-activation-in-the-callers-context"></a>Impondo a ativação no contexto do chamador

Você pode controlar se um objeto é ativado em seu próprio contexto. Quando você usa a ferramenta administrativa serviços de componentes para exigir a ativação de componentes no contexto do chamador, ocorre o seguinte quando o COM+ ativa uma instância do componente em um contexto:

-   O objeto é ativado no contexto do criador, se possível.
-   A ativação do objeto falhará se exigir seu próprio contexto; \_ \_ A tentativa co e \_ de criar o \_ contexto de \_ \_ cliente externo \_ é retornada.

Se o objeto requer ou não seu próprio contexto depende de sua configuração relativa ao estado atual das propriedades de contexto do chamador. Para obter mais detalhes, consulte [contextos com+](com--contexts.md).

Você desejaria controlar a ativação com esse nível de multa se algum aspecto do seu objeto não funcionar corretamente se ele tiver seu próprio contexto. Por exemplo, se o componente não oferecer suporte a marshaling e tiver seu próprio contexto, todas as chamadas para ele falharão porque as chamadas de contexto cruzado são interceptadas e um Marshal leve realizado.

**Para impor a ativação no contexto do chamador**

1.  No painel de detalhes da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no componente (localizado na pasta **componentes** de qualquer aplicativo com+ selecionado) para o qual você está definindo as propriedades de ativação e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do componente, clique na guia **ativação** .

3.  Selecione a caixa de seleção **deve ser ativada no contexto de chamadores** .

4.  Clique em **OK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de ativação Just-in-time COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Impondo ativação no contexto padrão](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



