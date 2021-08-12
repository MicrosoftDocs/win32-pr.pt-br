---
description: Transações e ativação JIT COM+
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: Transações e ativação JIT COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2b496f46652dc8ab9f6d573e712a0aa83575cac0adbb86a7dc4cfa88b565ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546043"
---
# <a name="transactions-and-com-jit-activation"></a>Transações e ativação JIT COM+

A ativação JIT COM+ está intimamente vinculada a transações automáticas. Quando você configura um componente para que ele exija uma transação ou exija uma nova transação, a ativação JIT também é habilitada automaticamente. Os dois recursos naturalmente funcionam em conjunto. Componentes transacionais ativados por JIT compartilham as seguintes características:

-   Sem estado. Você não manteria o estado que violaria o isolamento da transação nem manteria o estado que seria perdido na desativação do objeto.

-   Uso rápido. O padrão de uso canônico para um objeto que executa o trabalho em uma transação automática é fazer uma pequena unidade de trabalho, votar e sair.

    > [!Note]  
    > As maneiras como você vota em transações COM+ e sinal de doneness para a ativação JIT também são estreitamente vinculadas. Para obter mais informações, consulte [Configurando o bit feito.](setting-the-done-bit.md)

     

-   Uso repetido. Quando o trabalho transacional é dividido corretamente, os clientes usam os mesmos objetos de novo e de novo para executar pequenos lotes de trabalho atômico.

-   Desativado ao fazer commit ou anulação. No COM+, todos os objetos dentro do limite de transação são desativados quando a transação é confirmada ou anulada.

Em conjunto com componentes transacionais COM+, a ativação JIT serve como um grande aprimoramento de desempenho mantendo o canal aberto, pois os clientes mantêm referências de longa duração a objetos transacionais. Como aprimoramentos adicionais, você pode optar por pool dos objetos transacionais para reutilizar os recursos que eles têm, acelerar o tempo de reativação do objeto e gerenciar de perto como você usa recursos de memória para determinados objetos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de ativação Just-In-Time do COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Habilitando a ativação JIT para um componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Pool de objetos e ativação JIT COM+](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



