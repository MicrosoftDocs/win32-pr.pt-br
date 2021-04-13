---
description: A ativação JIT do COM+ essencialmente atinge um comprometimento entre os clientes de ávido e os servidores de velocidade para obter o desempenho ideal. Os clientes obtêm a manutenção de referências de objeto, enquanto os servidores podem gerenciar mais de forma mais minuciosa a utilização de memória.
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: Pooling de objetos e ativação JIT do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8042d838aaaae62eace6f61a8fe1aa820e17d079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370502"
---
# <a name="object-pooling-and-com-jit-activation"></a>Pooling de objetos e ativação JIT do COM+

A ativação JIT do COM+ essencialmente atinge um comprometimento entre os clientes de ávido e os servidores de velocidade para obter o desempenho ideal. Os clientes obtêm a manutenção de referências de objeto, enquanto os servidores podem gerenciar mais de forma mais minuciosa a utilização de memória.

Você pode refinar isso ainda mais usando o [pool de objetos com+](com--object-pooling.md). Ao agrupar objetos que são ativados por JIT, você pode dedicar uma determinada quantidade de memória para manter um determinado número de objetos ativos na memória, prontos para reutilização imediata. Isso faz mais sentido quando os objetos são caros de criar, como no caso em que contêm vários recursos.

Pooling de objetos ativados por JIT dessa maneira, você pode obter os seguintes benefícios:

-   Tempos de reativação de objetos muito acelerados.
-   Reutilização de recursos caros que os objetos estão mantendo.
-   Controle mais preciso da memória e do uso de recursos para os objetos em pool.
-   Retenção de flexibilidade administrativa para que seu aplicativo possa ser dimensionado para usar os recursos disponíveis e adaptar-se aos requisitos de desempenho em constante mudança.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de ativação Just-in-time COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Pool de objetos COM+](com--object-pooling.md)
</dt> <dt>

[Habilitando a ativação JIT para um componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Transações e ativação JIT do COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



