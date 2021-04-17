---
description: Controlando o tempo de vida e o estado do objeto
ms.assetid: 172e07a2-1711-4353-9099-ff9d31a564c6
title: Controlando o tempo de vida e o estado do objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cc1d582d85bc84ef2b1749a427711d1fe26fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784584"
---
# <a name="controlling-object-lifetime-and-state"></a>Controlando o tempo de vida e o estado do objeto

Um objeto em pool pode participar de como o COM+ gerencia sua atividade no pool implementando [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Quando um objeto em pool é criado, ele é agregado em um objeto maior que gerenciará o objeto chamando os seguintes métodos em **controledeobjetoi** em pontos regulares no ciclo de vida do objeto:

-   [**Ativar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)— chamado sempre que o objeto é retornado a um cliente, ativado em um contexto específico.
-   [**Desativar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)— chamado sempre que um objeto é liberado pelo cliente ou, no caso de um objeto ativado por JIT, quando é desativado.
-   [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)— chamado sempre que um objeto deve ser retornado para o pool geral.

A implementação de [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) é opcional, exceto para objetos transacionais, que sempre devem implementar [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) para monitorar o estado dos recursos que eles contêm. No entanto, é aconselhável implementar **controledeobjetoi** na maioria dos casos porque ele fornece uma maneira eficiente de gerenciar o comportamento de um objeto em pool, conforme descrito abaixo.

## <a name="performing-context-specific-initialization"></a>Executando inicialização de Context-Specific

Usando [**Ativar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), você pode inicializar o objeto no contexto no qual ele é ativado para um determinado cliente. Por exemplo, para determinar se o objeto tem afinidade de transação (seus recursos já podem estar inscritos), você pode obter a ID de transação associada ao contexto.

Normalmente, você usaria [**Ativar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)para executar a inicialização consistente em todos os métodos expostos pelo objeto, tratando-o como a parte específica do contexto do construtor do objeto.

## <a name="cleaning-up-any-client-state"></a>Limpando qualquer estado do cliente

Usando [**desativar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), você pode livrar-se de qualquer estado específico do cliente que possa existir para que seu objeto retorne ao pool em um estado completamente genérico e possa ser usado por qualquer cliente sem comprometer a segurança ou o isolamento.

## <a name="controlling-reuse-of-the-object"></a>Controlando a reutilização do objeto

Usando o [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), você pode monitorar o estado interno do seu objeto e relatar se ele se ajusta à sua reutilização. Se **CanBePooled** retornar true e o máximo do pool não tiver sido atingido, o objeto será colocado de volta no pool geral. Se **CanBePooled** retornar false, o objeto será Descartado. No caso de componentes transacionais, retornar false irá destruição a transação atual.

Normalmente, você manteria algum membro de dados globais para o objeto e, se detectar uma conexão como insatisfatório ou um recurso de algum tipo para estar em um estado inadequado, defina isso para refletir a situação atual e retorná-la por meio de [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).

Se um objeto não implementar [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), as instâncias continuarão sendo reutilizadas até que o nível máximo do pool seja atingido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cadeias de caracteres do construtor do objeto COM+](com--object-constructor-strings.md)
</dt> <dt>

[Como o pool de objetos funciona](how-object-pooling-works.md)
</dt> <dt>

[Melhorando o desempenho com o pooling de objetos](improving-performance-with-object-pooling.md)
</dt> <dt>

[Pooling de objetos transacionais](pooling-transactional-objects.md)
</dt> <dt>

[Requisitos para objetos pooling](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



