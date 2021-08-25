---
description: O gerenciador de distribuidores fornece pool de recursos para os distribuidores de recursos e garante que um recurso fornecido por um distribuidor de recursos seja inscrito corretamente na transação de objetos de aplicativo.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: Com+ Gerenciador de Distribuidores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec090ba8c6324363c80a00685e4bc9cfa11185fa1b95ad5db3575608c9fe60ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991685"
---
# <a name="com-dispenser-manager"></a>Com+ Gerenciador de Distribuidores

O gerenciador de distribuidores fornece pool de recursos para os distribuidores de recursos e garante que um recurso fornecido por um distribuidor de recursos seja inscrito corretamente na transação do objeto de aplicativo. O gerenciador do distribuidor recupera automaticamente os recursos que ainda estão reservados no final do tempo de vida de um objeto, eliminando a possibilidade de "vazamentos" do recurso. O gerenciador do distribuidor pode pedir a um distribuidor de recursos para criar um novo recurso ou destruir recursos ociosos quando necessário para ajustar os níveis de inventário, em vez de usar configurações estáticas.

> [!Note]  
> Como as interfaces do distribuidor de recursos expostas ao aplicativo não precisam ser interfaces COM, o gerenciador do distribuidor pode ser usado em um processo sem inicializar o COM, por exemplo, para dar suporte ao distribuidor de recursos ODBC.

 

Após a criação de recursos, o distribuidor de recursos pode especificar por quanto tempo um recurso ocioso pode permanecer no pool antes de ser destruído. Um thread que é executado no gerenciador do distribuidor está sempre procurando esses recursos ociosos.

## <a name="the-inventory-statistics-manager"></a>O Gerenciador de Estatísticas de Inventário

O gerenciador do distribuidor usa o gerenciador *de estatísticas de inventário para* gerenciar os níveis de inventário de recursos do pool. O gerenciador de estatísticas de inventário mantém um registro de quando cada recurso foi usado e remove recursos do inventário quando eles não foram usados por *x* segundos, em que o valor de *x* é definido por recurso quando o recurso é criado.

## <a name="the-holder-component"></a>O componente Holder

O gerente do distribuidor sonda cada *titular,* um componente criado pelo gerenciador do distribuidor que lista o inventário de recursos para cada distribuidor de recursos, a cada 10 segundos, para permitir que ele reajuste seu inventário de recursos. Cada titular chama o gerente de estatísticas de inventário para sugerir níveis de inventário para cada tipo de recurso. Como resultado, o titular pode pedir ao distribuidor de recursos para criar ou destruir algum inventário.

O titular e o distribuidor de recursos se comunicam para solicitar recursos de um tipo específico. As seguintes relações existem entre o titular e o distribuidor de recursos:

-   O titular pode solicitar um recurso do distribuidor de recursos. O distribuidor de recursos retorna um recurso disponível ou cria um novo.
-   O titular pode notificar o distribuidor de recursos de que um aplicativo não precisa mais de um recurso e, em seguida, devolvê-lo ao pool de recursos.
-   O titular e o distribuidor de recursos trabalham juntos para manter o tamanho do pool de recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Com+ Resource Dispenser](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



