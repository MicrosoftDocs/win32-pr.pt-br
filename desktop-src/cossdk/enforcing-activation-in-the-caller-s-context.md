---
description: Impondo a ativação no contexto de chamadores
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Impondo a ativação no contexto de chamadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42cb657ad7d11f61de0737ca7ac935d1d570649c3e0da9db9b63c79edea38cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567416"
---
# <a name="enforcing-activation-in-the-callers-context"></a>Impondo a ativação no contexto do chamador

Você pode controlar se um objeto é ativado em seu próprio contexto. Quando você usa a ferramenta administrativa serviços de componentes para exigir a ativação de componentes no contexto do chamador, o seguinte ocorre quando o COM+ ativa uma instância do componente em um contexto:

-   O objeto é ativado no contexto do criador, se possível.
-   A ativação do objeto falhará se exigir seu próprio contexto; A \_ TENTATIVA DE CO E PARA CRIAR FORA DO CONTEXTO DO CLIENTE é \_ \_ \_ \_ \_ \_ retornada.

Se o objeto requer ou não seu próprio contexto depende de sua configuração em relação ao estado atual das propriedades de contexto do chamador. Para obter mais detalhes, consulte [Contextos COM+.](com--contexts.md)

Você deseja controlar a ativação nesse nível se algum aspecto do objeto não funcionar corretamente se ele tiver seu próprio contexto. Por exemplo, se o componente não dá suporte ao marshaling e tem seu próprio contexto, todas as chamadas a ele falharão porque as chamadas entre contextos são interceptadas e um marshal leve é executado.

**Para impor a ativação no contexto do chamador**

1.  No painel de detalhes da ferramenta administrativa serviços de componentes,  clique com o botão direito do mouse no componente (localizado na pasta Componentes de qualquer aplicativo COM+ selecionado) para o qual você está definindo propriedades de ativação e clique em **Propriedades**.

2.  Na caixa de diálogo propriedades do componente, clique na **guia Ativação.**

3.  Marque a **caixa de seleção Deve ser ativada no contexto dos chamadores.**

4.  Clique em **OK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de ativação Just-In-Time do COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Impondo a ativação no contexto padrão](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



