---
description: Permite que o autor inicie uma reinstalação de alguns ou todos os recursos, enquanto a caixa de diálogo atual está em execução.
ms.assetid: bc667f20-3abe-4ef3-b51e-dc74da63f651
title: Reinstalar o ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f943d7e5950c9455909dad2d1a4677178a6608d4d8fe9bdfbd4cbf7ef752f2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339716"
---
# <a name="reinstall-controlevent"></a>Reinstalar o ControlEvent,

A reinstalação ControlEventallows o autor para iniciar uma reinstalação de alguns ou todos os recursos, enquanto a caixa de diálogo atual está em execução.

Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md) ou um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md)e requer que a interface do usuário seja executada no nível [*completo da interface*](f-gly.md) . Esse evento não funciona com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter mais informações, consulte [níveis de interface do usuário](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Uma cadeia de caracteres que é o nome do recurso ou "todos".

## <a name="action-on-subscribers"></a>Ação nos assinantes

Este ControlEvent, não executa uma ação nos assinantes.

## <a name="typical-use"></a>Usos comum

Esse evento é vinculado a um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal. O mesmo controle de [pressão](pushbutton-control.md) também deve ser vinculado a um ControlEvent, [REINSTALLMODE](reinstallmode-controlevent.md) .

 

 



