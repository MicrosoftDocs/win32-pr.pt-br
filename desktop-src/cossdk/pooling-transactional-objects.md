---
description: Os componentes transacionais que devem ser agrupados têm requisitos especiais.
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: Pooling de objetos transacionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006ba32ad2ac550be4fa4418dde322ded26c64c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807903"
---
# <a name="pooling-transactional-objects"></a>Pooling de objetos transacionais

Os componentes transacionais que devem ser agrupados têm requisitos especiais.

## <a name="manually-enlisting-resources"></a>Listando manualmente os recursos

Objetos com pooláveis que participam de transações devem inscrever manualmente os recursos gerenciados. Se um objeto mantiver recursos gerenciados entre clientes, não haverá nenhuma maneira para o Gerenciador de recursos se inscrever automaticamente em uma transação quando o objeto for ativado em um determinado contexto.

O próprio objeto deve lidar com a lógica de detecção da transação, desativando a inscrição automática do Resource Manager e inscrita manualmente todos os recursos que ele contém. As etapas para fazer isso são específicas do Gerenciador de recursos que você está usando. Se você precisar fazer inscrição manual, consulte a documentação do Gerenciador de recursos.

Conforme descrito abaixo, os objetos podem ser agrupados com afinidade de transação enquanto uma transação está ativa e pode ser ativada com afinidade de transação, se chamada por um cliente associado a essa transação. Antes de inscrever os recursos, primeiro você deve verificar a afinidade de transação. Se o objeto tiver sido extraído do pool específico para essa transação, ele já terá feito trabalho nessa transação e inscrito em seus recursos.

## <a name="turning-off-automatic-enlistment"></a>Desativando inscrição automática

A inscrição automática deve ser desativada após o recurso ser adquirido, geralmente no construtor do objeto. Ou seja, você desabilita a inscrição automática e, em seguida, se conecta.

Desabilitar a inscrição automática às vezes pode ser um procedimento sutil, especialmente no caso de provedores de acesso a dados em camadas. Às vezes, a inscrição automática é acoplada ao pool de conexões, como com o ODBC e, às vezes, não, assim como ocorre com OLE DB. Talvez seja necessário garantir que a inscrição automática esteja desativada em vários níveis de provedores.

## <a name="implementing-iobjectcontrol"></a>Implementando Controledeobjetoi

Objetos com pooláveis que participam de transações devem monitorar o estado atual dos recursos que eles estão mantendo. Se o objeto detectar que está em um estado não reutilizável — por exemplo, se uma conexão for inadequada, ela deverá retornar false para [**controledeobjetoi:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled). Isso terá o efeito de descartar a instância do objeto e decretado por a transação atual.

## <a name="transaction-specific-pools"></a>Pools de Transaction-Specific

Um pool de objetos é geralmente homogêneo e qualquer objeto em pool que não esteja em uso no momento é bom retornar a qualquer cliente. A única exceção a essa regra é no caso de objetos transacionais, para os quais o pool de objetos é otimizado. Quando o cliente que solicita um objeto tiver uma transação associada, o COM+ verificará o pool em busca de um objeto disponível que já esteja associado a essa transação. Se um objeto com afinidade de transação for encontrado, ele será retornado para o cliente; caso contrário, um objeto do pool geral será retornado.

Dessa maneira, os subpools especiais são mantidos contendo objetos com afinidade para uma transação específica. Quando a transação é confirmada ou anulada, esses objetos são retornados ao pool geral sem afinidade de transação, prontos para serem usados por qualquer cliente.

Por esse motivo, quando o componente inscreve manualmente seus recursos gerenciados em uma transação, ele deve primeiro verificar se eles já estão inscritos. Nesse caso, não há necessidade de se inscrever.

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

[Requisitos para objetos pooling](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



