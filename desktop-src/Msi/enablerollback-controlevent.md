---
description: Esse ControlEvent, pode ser usado para ativar ou desativar os recursos de reversão do instalador.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: EnableRollback ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc651ef90b46c87431453f50c7ee5a28953e4d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747551"
---
# <a name="enablerollback-controlevent"></a>EnableRollback ControlEvent,

Esse ControlEvent, pode ser usado para ativar ou desativar os recursos de reversão do instalador.

Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

False desativa os recursos de reversão do instalador. True ativa os recursos de reversão do instalador.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Este ControlEvent, não executa uma ação nos assinantes.

## <a name="typical-use"></a>Usos comum

Pode ser usado para desativar os recursos de reversão se o instalador detectar que não há espaço em disco suficiente disponível para concluir a instalação. Para esse caso, o ControlEvent, deve ser usado com as propriedades [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)e [**PROMPTROLLBACKCOST**](promptrollbackcost.md) .

 

 



