---
description: O serviço de ativação Just-in-time (JIT) permite que o COM+ desative um objeto enquanto um cliente ainda mantém uma referência ativa para esse objeto.
ms.assetid: dbc7b257-8506-42c8-8a78-3474c6d4f4b6
title: Conceitos de ativação Just-in-time COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c942bfeb342ea305083e0c7d7ebdea2fe96bf24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812395"
---
# <a name="com-just-in-time-activation-concepts"></a>Conceitos de ativação Just-in-time COM+

O serviço de ativação Just-in-time (JIT) permite que o COM+ desative um objeto enquanto um cliente ainda mantém uma referência ativa para esse objeto. Na próxima vez que o cliente chamar um método no objeto, que o cliente acredita que ainda esteja ativo, o serviço de ativação JIT do COM+ reativará o objeto de forma transparente para o cliente, just in time.

A principal vantagem de usar o COM + ativação JIT é que você pode permitir que os clientes contenham referências a objetos enquanto eles precisarem, sem necessariamente ligar recursos de servidor valiosos, como memória. Outros benefícios importantes incluem o seguinte:

-   O uso do serviço de ativação JIT do COM+ simplifica bastante o modelo de programação para o cliente, pois o cliente não precisa pensar em como ele usa objetos caros de servidor e recursos de servidor. Sem a ativação JIT, os clientes podem incorrer em uma penalidade significativa quando freqüentemente precisam chamar e liberar objetos.
    > [!Note]  
    > Você pode refinar ainda mais esse benefício de desempenho usando o serviço de [pooling de objetos com+](com--object-pooling.md) . Ao agrupar objetos ativados por JIT, você pode acelerar muito a reativação de objetos para clientes ao reutilizar quaisquer recursos que eles possam estar mantendo, dando a você um controle mais preciso sobre a quantidade de memória usada por um determinado objeto no servidor. Para obter mais detalhes, consulte [pooling de objetos e ativação JIT do com+](object-pooling-and-com--jit-activation.md).

     

-   Com aplicativos distribuídos, uma viagem de ida e volta de rede cara é necessária para a criação de cada objeto, e o mais distante do cliente é o servidor, quanto maior os custos de ativação e marshaling do objeto de servidor, abertura do canal e configuração do proxy e do stub. Usando o serviço de ativação JIT do COM+, você pode minimizar a frequência de criação de objeto para melhorar significativamente o desempenho do seu aplicativo.
-   Quando você usa a ativação JIT do COM+ para ativar esses objetos nos quais os clientes contêm referências de longa duração, mas que não estão necessariamente usando o tempo todo, a memória do servidor nem sempre está presa, mantendo esses objetos ativos. Isso pode aumentar significativamente a escalabilidade do seu aplicativo. O único impacto sobre o desempenho que os clientes veem é o tempo que leva para o COM+ reativar o objeto, geralmente apenas com margens mais tempo do que é necessário para alocar memória para o objeto e substancialmente menor do que a viagem de ida e volta da rede para a criação remota de objetos.

## <a name="enabling-com-jit-activation"></a>Habilitando a ativação JIT do COM+

Você pode habilitar o serviço de ativação JIT do COM+ para um componente usando a ferramenta administrativa serviços de componentes ou as funções administrativas. Para obter detalhes sobre como fazer isso, consulte [habilitando a ativação JIT para um componente](enabling-jit-activation-for-a-component.md).

A ativação JIT do COM+ pode interagir com outros serviços COM+, como o seguinte:

-   Quando seu componente requer transações, a ativação JIT é habilitada automaticamente para ela. Para obter mais detalhes, consulte [Transações e ativação JIT do com+](transactions-and-com--jit-activation.md).
-   Quando o componente está habilitado para ativação JIT, a sincronização é definida automaticamente como necessária. Isso significa que, se dois clientes chamarem simultaneamente um componente ativado por JIT e uma chamada de método para um deles retornar, fazendo com que o objeto seja desativado, o outro não será mantido à esquerda.

## <a name="how-deactivation-is-triggered"></a>Como a desativação é disparada

O COM+ desativa um objeto com base no status do bit de conclusão no contexto do objeto. O objeto pode usar esse bit para sinalizar se ele está concluído — ou seja, pronto para ser desativado — durante uma determinada chamada de método. Para obter mais informações, consulte [definindo o bit concluído](setting-the-done-bit.md).

## <a name="using-the-auto-done-property"></a>Usando a propriedade auto-Done

Usando a ferramenta administrativa serviços de componentes, você pode configurar um método de modo que o objeto seja desativado automaticamente no retorno do método. (Consulte [habilitando auto-pronto para um método](enabling-auto-done-for-a-method.md) para obter instruções sobre como definir essa propriedade.) Ao selecionar essa opção, você pode eliminar as chamadas de método repetitivas para votação em transações. Como a configuração padrão para o bit de consistência é true, se você tiver alterado o bit Done para true também e não tomar nenhuma ação para alterar essas configurações, [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) será chamado automaticamente depois que o método retornar.

No entanto, há uma limitação para esse comportamento: COM+ examinará o HRESULT que o método retorna. Se esse HRESULT indicar falha, o bit de consistência será definido como false e o resultado será o mesmo que se você tivesse chamado [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort).

Para resumir, se você selecionar automático para um método e não tomar nenhuma ação para definir quaisquer bits e se um HRESULT (HR) for retornado, o seguinte se aplicará:

-   Se for bem sucedido (HR), é como se você tivesse chamado [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete).
-   Se falha (HR), é como se você tivesse chamado [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort).

## <a name="using-iobjectcontrol-to-manage-object-activation-and-deactivation"></a>Usando o Controledeobjetoi para gerenciar a ativação e a desativação de objetos

Você pode implementar a interface [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) para que o tempo de execução do com+ gerencie automaticamente a desativação e a reativação para seus objetos. Quando um objeto implementa essa interface, o COM+ chama [**controledeobjetoi::D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) quando ele desativa o objeto e [**Controledeobjetoi:: Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) quando o reativa. Esses métodos habilitam a inicialização automática de contexto na ativação do objeto e na limpeza do estado na desativação.

Se você estiver agrupando objetos que usam a ativação JIT do COM+, é altamente recomendável que você implemente [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Para obter mais detalhes, consulte [pooling de objetos e ativação JIT do com+](object-pooling-and-com--jit-activation.md).

## <a name="statelessness-and-jit-activation"></a>Sem estado e ativação JIT

Os objetos transacionais são necessariamente sem estado porque não é possível compartilhar o estado em um limite de transação. Portanto, você usaria a ativação JIT somente quando o objeto não mantiver nenhum estado que seria perdido na desativação; caso contrário, você viola o isolamento das transações. Devido aos padrões de uso natural de objetos transacionais, eles fazem alguma unidade de trabalho e liberam o objeto quando a transação é confirmada ou anulada — a ativação JIT e as transações automáticas estão relacionadas diretamente. Configurar um objeto para exigir transações habilita a ativação JIT do COM+ automaticamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas de ativação Just-in-time COM+](com--just-in-time-activation-tasks.md)
</dt> <dt>

[Pooling de objetos e ativação JIT do COM+](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[Transações e ativação JIT do COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



