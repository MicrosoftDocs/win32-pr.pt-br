---
description: Objetos em pool devem atender a determinados requisitos para permitir que uma única instância de objeto seja usada por vários clientes.
ms.assetid: 2cd4211e-be12-4197-8b43-5cb9f2321016
title: Requisitos para objetos em pool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af3e3b67f7d796c199649b64f711ec32a75374bff60ebf900b34871ed4bc310
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047284"
---
# <a name="requirements-for-poolable-objects"></a>Requisitos para objetos em pool

Objetos em pool devem atender a determinados requisitos para permitir que uma única instância de objeto seja usada por vários clientes.

## <a name="stateless"></a>Sem estado

Para manter a segurança, a consistência e o isolamento, os objetos em pool não devem conter nenhum estado específico do cliente para o cliente. Você pode gerenciar qualquer estado por cliente usando [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), executando a inicialização específica do contexto com [**IObjectControl::Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) e limpando qualquer estado do cliente com [**IObjectControl::D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate). Para obter mais detalhes, consulte [Controlando o tempo de vida do objeto e o estado](controlling-object-lifetime-and-state.md).

## <a name="no-thread-affinity"></a>Sem afinidade de thread

Objetos em pool não podem ser vinculados a um thread específico; caso contrário, o desempenho poderá ser potencialmente desastroso. Por esse motivo, objetos em pool não podem ser marcados para serem executados no modelo de apartment; eles devem ser executados no apartment multithreaded ou no apartment neutro. Além disso, objetos em pool não devem usar o armazenamento local de threads nem devem agregar o marshaler de thread livre. Para obter mais detalhes sobre o threading no COM+, consulte [Modelos de threading COM+.](com--threading-models.md)

> [!Note]  
> O Microsoft Visual Basic 6.0 e ambientes de desenvolvimento anteriores podem criar apenas componentes de modelo de apartment. No entanto, no Visual Basic .NET, os componentes podem ser em pool.

 

## <a name="aggregatable"></a>Agregável

Objetos em pool devem dar suporte à agregação , ou seja, eles devem dar suporte à criação invocando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) com um argumento *pUnkOuter* não NULL. Quando o COM+ ativa um objeto em pool, ele cria uma agregação para gerenciar o tempo de vida do objeto em pool e chamar métodos em [**IObjectControl.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) Para obter detalhes sobre como escrever objetos agregáveis, consulte [Agregação](/windows/desktop/com/aggregation).

## <a name="transactional-components"></a>Componentes transacionais

Objetos em pool que participam de transações devem inscrever manualmente recursos gerenciados. Enquanto estiver em pool, se o objeto tiver um recurso gerenciado, como uma conexão de banco de dados, não haverá como o gerenciador de recursos se inscrever automaticamente em uma transação quando o objeto for ativado em determinado contexto. Portanto, o próprio objeto deve lidar com a lógica de detecção da transação, desligar a inspeção automática do gerenciador de recursos e inscrever manualmente todos os recursos que ela contém. Além disso, um objeto em pool transacional deve refletir o estado atual de seus recursos nos valores de parâmetro [**de IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled). Para obter mais detalhes, consulte [Pooling Transactional Objects](pooling-transactional-objects.md).

## <a name="implement-iobjectcontrol-to-manage-the-object-lifetime"></a>Implementar IObjectControl para gerenciar o tempo de vida do objeto

Objetos em pool devem implementar [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), embora não seja estritamente necessário fazer isso. No entanto, os componentes transacionais que estão em pool devem implementar **IObjectControl.** Esses componentes devem monitorar o estado dos recursos que eles têm e indicar quando não podem ser reutilizados; quando [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) retornar false, ele irá acioná-la. Para obter mais detalhes, consulte [Controlando o tempo de vida do objeto e o estado](controlling-object-lifetime-and-state.md).

## <a name="language-restrictions"></a>Restrições de idioma

Componentes desenvolvidos usando o Microsoft Visual Basic 6.0 e anteriores não podem ser em pool porque esses componentes serão threaded apartment-model. No entanto, no Visual Basic .NET, os componentes podem ser em pool.

## <a name="legacy-components"></a>Componentes herdados

Desde que eles sejam não transacionais e estão em conformidade com os requisitos anteriores apropriados, os componentes poderão ser em pool mesmo se não foram escritos especificamente com a funcionalidade de pooling em mente. Não é necessário implementar [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol); um componente que não faz isso simplesmente não participará do gerenciamento de seu tempo de vida. Se [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) não for implementado, o objeto continuará a ser reutilizado até que o pool atinja o tamanho máximo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cadeias de caracteres do construtor de objeto COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controlando o tempo de vida e o estado do objeto](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Como funciona o pool de objetos](how-object-pooling-works.md)
</dt> <dt>

[Melhorando o desempenho com o pool de objetos](improving-performance-with-object-pooling.md)
</dt> <dt>

[Pooling de objetos transacionais](pooling-transactional-objects.md)
</dt> </dl>

 

 
