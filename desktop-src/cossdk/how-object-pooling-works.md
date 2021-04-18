---
description: Quando você configura um componente a ser agrupado, o COM+ manterá instâncias dele em um pool, pronto para ser ativado para qualquer cliente que solicite o componente. Qualquer solicitação de criação de objeto será manipulada por meio do Gerenciador de pool.
ms.assetid: 34978b50-cd20-42fd-ad46-410190478ef8
title: Como o pool de objetos funciona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78784fc0e5362c14ceb598b404976c6ca494a19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793972"
---
# <a name="how-object-pooling-works"></a>Como o pool de objetos funciona

Quando você configura um componente a ser agrupado, o COM+ manterá instâncias dele em um pool, pronto para ser ativado para qualquer cliente que solicite o componente. Qualquer solicitação de criação de objeto será manipulada por meio do Gerenciador de pool.

Os pools são configurados e mantidos em uma base por componente. Um pool consiste em objetos homogêneos que compartilham o mesmo CLSID. A única exceção é para objetos transacionais, para os quais os subpools são mantidos contendo objetos que têm afinidade de transação enquanto uma transação está pendente.

Quando o aplicativo for iniciado, o pool será preenchido até o nível mínimo que você especificou administrativamente, desde que a criação do objeto seja realizada com sucesso. À medida que as solicitações de cliente para o componente entram, elas são satisfeitas de acordo com a primeira base atendidas do pool. Se nenhum objeto em pool estiver disponível e o pool ainda não estiver no nível máximo especificado, um novo objeto será criado e ativado para o cliente.

Quando o pool atingir seu nível máximo, as solicitações de cliente serão enfileiradas e receberão o primeiro objeto disponível do pool. O número de objetos, incluindo ativado e desativado, nunca excederá o valor máximo do pool. As solicitações de criação de objeto atingirão o tempo limite após um período especificado administrativamente para que você possa controlar por quanto tempo os clientes aguardarão a criação do objeto. Após uma falha de tempo limite, o cliente obterá o erro E o \_ tempo limite de retorno de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Sempre que possível, o COM+ tentará reutilizar um objeto depois que um cliente o liberar, até que o pool atinja seu nível máximo. O objeto é responsável por monitorar seu estado para determinar se ele pode ser reutilizado e deve retornar um valor apropriado para [**controledeobjetoi:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).

Quando um objeto em pool é criado, ele é agregado em um objeto maior que gerenciará o tempo de vida do objeto. O objeto externo chama métodos em [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) em momentos apropriados no ciclo de vida do objeto, da seguinte maneira:

-   O método [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) é chamado sempre que o objeto é retornado a um cliente, ativado em um contexto específico.
-   O método [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) é chamado sempre que um objeto é liberado pelo cliente ou, no caso de um objeto ativado por JIT, quando ele é desativado.
-   O método [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) é chamado sempre que um objeto deve ser retornado para o pool geral. Se o objeto detectar que algum recurso reutilizável está em um estado inadequado, ele deverá retornar **false** para esse método e o Gerenciador de pool descartará o objeto.

Um objeto não necessariamente precisa implementar [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Caso contrário, as instâncias serão sempre reutilizadas até que o nível máximo do pool seja atingido.

Para obter detalhes sobre como configurar os componentes a serem agrupados, consulte [Configurando um componente a ser agrupado](configuring-a-component-to-be-pooled.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cadeias de caracteres do construtor do objeto COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controlando o tempo de vida e o estado do objeto](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Melhorando o desempenho com o pooling de objetos](improving-performance-with-object-pooling.md)
</dt> <dt>

[Pooling de objetos transacionais](pooling-transactional-objects.md)
</dt> <dt>

[Requisitos para objetos pooling](requirements-for-poolable-objects.md)
</dt> </dl>

 

 
