---
description: Esse evento notifica o controle Directorylist que o usuário deseja selecionar o pai do diretório atual. Para obter informações relacionadas, consulte caixa de diálogo procurar.
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: DirectoryListUp ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99fb0731a06f30cf788e3565e0988bf5b20ebce7abec8be351f4d1fe9d2aab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086176"
---
# <a name="directorylistup-controlevent"></a>DirectoryListUp ControlEvent,

Esse evento notifica o [controle directorylist](directorylist-control.md) que o usuário deseja selecionar o pai do diretório atual. Para obter informações relacionadas, consulte [caixa de diálogo Procurar](browse-dialog.md).

Esse evento deve ser publicado por um [controle de pressão](pushbutton-control.md) localizado na mesma caixa de diálogo que o controle assinando esse evento. O evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

Se o diretório atual for o diretório raiz da unidade, um evento DirectoryListUp desabilitará quaisquer outros controles que publiquem um evento DirectoryListUp.

## <a name="published-by"></a>Publicada por

[Directorylist](directorylist-control.md)

## <a name="argument"></a>Argumento

Este ControlEvent, não usa um argumento.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Este ControlEvent, não executa uma ação nos assinantes.

## <a name="typical-use"></a>Usos comum

Um controle de [supressão](pushbutton-control.md) na mesma caixa de diálogo modal que a directorylist é usado para disparar a reversão no caminho.

 

 



