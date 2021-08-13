---
description: Melhorando o desempenho com o pooling de objetos
ms.assetid: 7a8a38d8-6549-4686-a298-f3b427b380e3
title: Melhorando o desempenho com o pooling de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ce6a86e76f7a97395973cc9cab4c4e9e81177f4312a389c2b01ec2d88eb7a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547843"
---
# <a name="improving-performance-with-object-pooling"></a>Melhorando o desempenho com o pooling de objetos

O pooling de objetos pode ser extremamente eficaz em determinadas circunstâncias, gerando aumentos substanciais no desempenho. A ideia geral para reutilizar objetos para a melhor vantagem é agrupar o máximo possível de recursos, fatorar a inicialização a partir do trabalho real realizado e, em seguida, adaptar administrativamente as características do pool ao hardware real no momento da implantação. Ou seja, você deve continuar de acordo com as seguintes etapas:

1.  Escreva o objeto para fatorar a inicialização cara e a aquisição de recursos que são executadas para qualquer cliente como um pré-requisito para fazer o trabalho real em nome do cliente. Grave construtores de objeto pesado no pool o máximo de recursos possível para que eles sejam mantidos pelo objeto e imediatamente disponíveis quando os clientes obtiverem um objeto do pool.
2.  Configure administrativamente o pool para obter o melhor equilíbrio entre os recursos de hardware disponíveis, normalmente negociando a memória dedicada à manutenção de um pool de um determinado tamanho no Exchange para o acesso de cliente e o uso de objetos mais rápidos. Em um determinado ponto, o pooling atingirá os retornos e você poderá obter um bom desempenho suficiente ao mesmo tempo em que limita o possível uso de recursos por um componente específico.

## <a name="doing-actual-work-or-acquiring-resources"></a>Fazendo trabalho real ou adquirindo recursos

Se você tiver um componente que os clientes usarão brevemente e em uma rápida sucessão, em que uma parte significativa do tempo de uso do objeto é gasta na aquisição de recursos ou inicialização antes de fazer um trabalho específico para o cliente, é provável que escrever seu componente para usar o pooling de objetos será um grande ganho para você.

Você pode escrever o componente de modo que, no construtor do objeto, você execute o trabalho demorado que seja uniforme para todos os clientes, adquirindo uma ou várias conexões, executando scripts, buscando dados de inicialização de arquivos ou em uma rede e assim por diante. Isso tem o efeito de agrupar todos esses recursos. Você está agrupando a combinação de recursos e o estado genérico necessário para executar algum trabalho.

Nessa circunstância, quando os clientes obtêm um objeto do pool, eles têm esses recursos imediatamente disponíveis. Normalmente, eles usarão o objeto para fazer alguma pequena unidade de trabalho, enviar ou extrair dados e, em seguida, o objeto chamará [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) ou [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) e Return. Com padrões de uso de incêndio rápido, como esse, o pooling gera excelentes benefícios de desempenho. Você pode aproveitar totalmente a simplicidade do modelo de programação de transação automática sem estado e, ainda assim, obter desempenho em comparação com componentes com estado tradicional.

No entanto, se os clientes usarem um objeto por um longo tempo toda vez que chamá-lo, o pooling fará menos sentido. A vantagem da velocidade obtida é marginal, pois o tempo de uso aumenta em relação ao tempo de inicialização. Você fica diminuindo os retornos que podem não justificar o custo da memória necessária para manter um pool de objetos ativos.

## <a name="sharing-cost-across-multiple-clients"></a>Compartilhando custos entre vários clientes

Uma variação na inicialização de fatoração é que você pode usar o pooling para amortizar estatisticamente o custo de aquisição de recursos caros. Se você tomar a queda de aquisição ou inicialização uma vez e, em seguida, reutilizar o objeto, você compartilhará esse custo em todos os clientes que usam o objeto durante seu tempo de vida. O tempo de construção pesado é incorrido apenas uma vez por objeto.

## <a name="preallocating-objects"></a>Pré-alocando objetos

Se você especificar um tamanho mínimo de pool diferente de zero, esse número mínimo de objetos será criado e agrupado quando o aplicativo for iniciado, pronto para todos os clientes que chamarem para o aplicativo.

## <a name="governing-resource-use-with-pool-management"></a>Controlando o uso de recursos com o gerenciamento de pool

Você pode usar o tamanho máximo do pool para controlar muito precisamente como você usa os recursos. Por exemplo, se você tiver licenciado um determinado número de conexões de banco de dados, poderá controlar quantas conexões você abriu a qualquer momento.

Quando você leva em consideração padrões de uso do cliente, características de uso de objeto e recursos físicos como memória e conexões, é provável que você encontre algum ponto de equilíbrio ideal ao fazer o ajuste de desempenho. Os objetos de Pooling produzirão uma redução de retornos após um determinado ponto. Você pode determinar o nível de desempenho que você precisa e equilibrar isso em relação aos recursos necessários para obtê-lo.

Para facilitar o ajuste de desempenho ao configurar o pool de objetos, você pode monitorar as estatísticas de objeto dos componentes em um aplicativo. Para obter detalhes, consulte [monitorando estatísticas de objeto](monitoring-object-statistics.md).

## <a name="improve-performance-of-jit-activated-components"></a>Melhorar o desempenho de componentes de JIT-Activated

O pool de objetos funciona muito bem com o serviço de [ativação Just-in-time do com+](com--just-in-time-activation.md) . Ao agrupar objetos que estão sendo ativados por JIT, você pode acelerar a reativação de objetos. Você Obtém os benefícios de manter o canal aberto pela ativação JIT e, ao mesmo tempo, reduzir o custo da reativação. Você pode usar o pooling nesse caso para controlar a quantidade de memória que deseja alocar a objetos que têm referências ativas.

É mais provável que você esteja agrupando componentes ativados por JIT quando eles são transacionais. O pooling de objetos é otimizado para manipular componentes transacionais. Para obter mais informações, consulte [pooling de objetos transacionais](pooling-transactional-objects.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cadeias de caracteres do construtor do objeto COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controlando o tempo de vida e o estado do objeto](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Como o pool de objetos funciona](how-object-pooling-works.md)
</dt> <dt>

[Pooling de objetos transacionais](pooling-transactional-objects.md)
</dt> <dt>

[Requisitos para objetos pooling](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



