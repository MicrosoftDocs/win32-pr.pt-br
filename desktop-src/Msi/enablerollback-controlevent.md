---
description: Esse ControlEvent pode ser usado para ativar ou desativar os recursos de re rollback do instalador.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: EnableRollback ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3b0cd93a65a9402c915606585f3eb1cd43c058847e2907b1134e1c84982b76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143107"
---
# <a name="enablerollback-controlevent"></a>EnableRollback ControlEvent

Esse ControlEvent pode ser usado para ativar ou desativar os recursos de re rollback do instalador.

Esse evento pode ser publicado por um [controle PushButton ou](pushbutton-control.md)um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser autor na [tabela ControlEvent](controlevent-table.md).

Esse ControlEvent exige que a interface do usuário seja executado no [*nível completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida ou*](r-gly.md) interface do usuário [*básica.*](b-gly.md) Para obter informações, consulte [Interface do Usuário níveis](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Este ControlEvent é publicado pelo instalador.

## <a name="argument"></a>Argumento

False desliga os recursos de reação do instalador. True liga os recursos de reação do instalador.

## <a name="action-on-subscribers"></a>Ação em Assinantes

Este ControlEvent não executa uma ação em assinantes.

## <a name="typical-use"></a>Usos comum

Pode ser usado para desativar os recursos de reação se o instalador detectar que não há espaço em disco suficiente disponível para concluir a instalação. Nesse caso, o ControlEvent deve ser usado com as propriedades [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)e [**PROMPTROLLBACKCOST.**](promptrollbackcost.md)

 

 



