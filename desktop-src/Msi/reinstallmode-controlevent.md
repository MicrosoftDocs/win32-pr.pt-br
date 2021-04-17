---
description: Permite que o autor especifique o modo de validação ou os modos durante uma reinstalação e enquanto a caixa de diálogo atual está em execução.
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: Reinstalar o ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ff5ff662b2880a3f4ab0fb79738b49cdeeccd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749781"
---
# <a name="reinstallmode-controlevent"></a>Reinstalar o ControlEvent,

A reinstalação do ControlEventallows o autor para especificar o modo de validação ou os modos durante uma reinstalação e enquanto a caixa de diálogo atual está em execução.

Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md) ou um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md)e requer que a interface do usuário seja executada no nível [*completo da interface*](f-gly.md) . Esse evento não funciona com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter mais informações, consulte [níveis de interface do usuário](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Uma cadeia de caracteres. Para obter uma lista de valores possíveis, consulte Propriedade [**REinstallmode**](reinstallmode.md) .

## <a name="action-on-subscribers"></a>Ação nos assinantes

Este ControlEvent, não executa uma ação nos assinantes.

## <a name="typical-use"></a>Usos comum

Esse evento é vinculado a um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal. O mesmo controle de [pressão](pushbutton-control.md) também deve ser vinculado a um ControlEvent, de [reinstalação](reinstall-controlevent.md) .

 

 



