---
description: Os objetos pooling devem atender a certos requisitos para permitir que uma única instância de objeto seja usada por vários clientes.
ms.assetid: 2cd4211e-be12-4197-8b43-5cb9f2321016
title: Requisitos para objetos pooling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d6834210f180ad8b514b51b6926b5cd30714fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920335"
---
# <a name="requirements-for-poolable-objects"></a>Requisitos para objetos pooling

Os objetos pooling devem atender a certos requisitos para permitir que uma única instância de objeto seja usada por vários clientes.

## <a name="stateless"></a>Sem estado

Para manter a segurança, a consistência e o isolamento, os objetos pooling não devem conter estado específico do cliente do cliente para o cliente. Você pode gerenciar qualquer estado por cliente usando o [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), executando a inicialização específica de contexto com [**Controledeobjetoi:: ativar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) e limpando qualquer estado do cliente com [**controledeobjetoi::D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate). Para obter mais detalhes, consulte [controlando o tempo de vida e o estado do objeto](controlling-object-lifetime-and-state.md).

## <a name="no-thread-affinity"></a>Sem afinidade de thread

Objetos com poolable não podem ser associados a um thread específico; caso contrário, o desempenho poderia ser potencialmente desastroso. Por esse motivo, os objetos pooling não podem ser marcados para execução no modelo de apartamento; Eles devem ser executados no apartamento multithread ou no apartamento neutro. Além disso, objetos pooling não devem usar o armazenamento local de thread nem devem agregar o marshaler de thread livre. Para obter mais detalhes sobre Threading em COM+, consulte [modelos de Threading com+](com--threading-models.md).

> [!Note]  
> O Microsoft Visual Basic 6,0 e os ambientes de desenvolvimento anteriores podem criar somente componentes de modelo de apartamento. No entanto, no Visual Basic .NET, os componentes podem ser agrupados.

 

## <a name="aggregatable"></a>Agregável

Os objetos pooling devem dar suporte à agregação, ou seja, eles devem dar suporte à criação invocando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) com um argumento *pUnkOuter* não nulo. Quando o COM+ ativa um objeto em pool, ele cria uma agregação para gerenciar o tempo de vida do objeto em pool e chamar métodos em [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Para obter detalhes sobre como escrever objetos agregáveis, consulte [agregação](/windows/desktop/com/aggregation).

## <a name="transactional-components"></a>Componentes transacionais

Objetos com pooláveis que participam de transações devem inscrever manualmente os recursos gerenciados. Enquanto ele estiver em pool, se o seu objeto mantiver um recurso gerenciado, como uma conexão de banco de dados, não haverá nenhuma maneira para o Gerenciador de recursos se inscrever automaticamente em uma transação quando o objeto for ativado no contexto especificado. Portanto, o próprio objeto deve lidar com a lógica de detecção da transação, desativando a inscrição automática do Resource Manager e manualmente listando os recursos que ela contém. Além disso, um objeto em pool transacional deve refletir o estado atual de seus recursos nos valores de parâmetro de [**controledeobjetoi:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled). Para obter mais detalhes, consulte [pooling de objetos transacionais](pooling-transactional-objects.md).

## <a name="implement-iobjectcontrol-to-manage-the-object-lifetime"></a>Implementar Controledeobjetoi para gerenciar o tempo de vida do objeto

Os objetos pooling devem implementar [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), embora não seja estritamente necessário. No entanto, os componentes transacionais que são agrupados devem implementar **controledeobjetoi**. Esses componentes devem monitorar o estado dos recursos que eles contêm e indicar quando eles não podem ser reutilizados; Quando [**controledeobjetoi:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) retorna false, ele destruição uma transação. Para obter mais detalhes, consulte [controlando o tempo de vida e o estado do objeto](controlling-object-lifetime-and-state.md).

## <a name="language-restrictions"></a>Restrições de idioma

Os componentes desenvolvidos usando o Microsoft Visual Basic 6,0 e versões anteriores não podem ser agrupados porque esses componentes serão segmentados no modelo de apartamento. No entanto, no Visual Basic .NET, os componentes podem ser agrupados.

## <a name="legacy-components"></a>Componentes herdados

Desde que eles não sejam transacionais e estejam em conformidade com os requisitos anteriores apropriados, os componentes podem ser agrupados mesmo que não tenham sido especificamente escritos com o recurso de Pooling em mente. Não é necessário implementar [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol); um componente que não faz isso simplesmente não participará do gerenciamento de seu tempo de vida. Se [**controledeobjetoi:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) não for implementado, o objeto continuará a ser reutilizado até que o pool atinja o tamanho máximo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cadeias de caracteres do construtor do objeto COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controlando o tempo de vida e o estado do objeto](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Como o pool de objetos funciona](how-object-pooling-works.md)
</dt> <dt>

[Melhorando o desempenho com o pooling de objetos](improving-performance-with-object-pooling.md)
</dt> <dt>

[Pooling de objetos transacionais](pooling-transactional-objects.md)
</dt> </dl>

 

 
