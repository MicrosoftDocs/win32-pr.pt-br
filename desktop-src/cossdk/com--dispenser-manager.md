---
description: O Gerenciador do dispensador fornece o pool de recursos para os dispensadores de recursos e garante que um recurso fornecido por um dispensador de recursos seja inscrito corretamente na transação de objetos de aplicativo.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: Gerenciador do dispensador COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2422b7debb8ee12ed97444f3b16f31e663e1e71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500932"
---
# <a name="com-dispenser-manager"></a>Gerenciador do dispensador COM+

O Gerenciador do dispensador fornece o pool de recursos para os dispensadores de recursos e garante que um recurso fornecido por um dispensador de recursos seja inscrito corretamente na transação do objeto de aplicativo. O Gerenciador do dispensador recupera automaticamente os recursos que ainda estão reservados no final do tempo de vida de um objeto, eliminando a possibilidade de "vazamentos" de recursos. O Gerenciador do dispensador pode pedir que um dispensador de recursos crie um novo recurso ou destrua recursos ociosos quando necessário para ajustar os níveis de inventário, em vez de usar configurações estáticas.

> [!Note]  
> Como as interfaces do dispensador de recursos expostas ao aplicativo não precisam ser interfaces COM, o Gerenciador do dispensador pode ser usado em um processo sem inicializar COM, por exemplo, para dar suporte ao dispensador de recursos ODBC.

 

Após a criação do recurso, o dispensador de recursos pode especificar quanto tempo um recurso ocioso tem permissão para permanecer no pool antes de ser destruído. Um thread que é executado no Gerenciador do dispensador está sempre procurando esses recursos ociosos.

## <a name="the-inventory-statistics-manager"></a>O Gerenciador de estatísticas de inventário

O Gerenciador do dispensador usa o *Gerenciador de estatísticas de inventário* para gerenciar os níveis de inventário de recursos de pool. O Gerenciador de estatísticas de inventário mantém um registro de quando cada recurso foi usado e remove recursos do inventário quando eles não são usados por *x* segundos, em que o valor de *x* é definido por recurso quando o recurso é criado.

## <a name="the-holder-component"></a>O componente de detentor

O gerente do dispensador sonda cada *portador*, um componente criado pelo Gerenciador do dispensador que lista o inventário de recursos para cada dispensador de recursos, a cada 10 segundos, para permitir que ele reajuste seu inventário de recursos. Cada portador chama o Gerenciador de estatísticas de inventário para sugerir os níveis de estoque para cada tipo de recurso. Como resultado, o detentor pode pedir que o dispensador de recursos crie ou destrua algum inventário.

O detentor e o dispensador de recursos se comunicam com os recursos de solicitação de um tipo específico. As seguintes relações existem entre o detentor e o dispensador de recursos:

-   O detentor pode solicitar um recurso do dispensador de recursos. O dispensador de recursos retorna um recurso disponível ou cria um novo.
-   O detentor pode notificar o dispensador de recursos de que um aplicativo não precisa mais de um recurso e, em seguida, retorná-lo ao pool de recursos.
-   O detentor e o dispensador de recursos trabalham juntos para manter o tamanho do pool de recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



