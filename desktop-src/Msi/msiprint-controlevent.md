---
description: Esse evento é publicado pelo controle ScrollableText para permitir que o usuário imprima o conteúdo desse controle.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: MsiPrint ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0dd876f1a98e68c6ad61c7c122e1b51fa9c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837202"
---
# <a name="msiprint-controlevent"></a>MsiPrint ControlEvent,

Esse evento é publicado pelo [controle ScrollableText](scrollabletext-control.md) para permitir que o usuário imprima o conteúdo desse controle.

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Esse ControlEvent, está disponível a partir do Windows Installer 5,0.

Esse evento deve ser assinado por um controle de [pressão](pushbutton-control.md) localizado na mesma caixa de diálogo que o [controle ScrollableText](scrollabletext-control.md). TheMsiPrint ControlEvent, deve ser criado na [tabela ControlEvent,](controlevent-table.md).

## <a name="published-by"></a>Publicada por

[ScrollableText](scrollabletext-control.md)

## <a name="argument"></a>Argumento

Este ControlEvent, não usa um argumento.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Este ControlEvent, não executa uma ação nos assinantes.

## <a name="typical-use"></a>Usos comum

Um controle de [pressão](pushbutton-control.md) na mesma caixa de diálogo que o [controle ScrollableText](scrollabletext-control.md) pode ser usado para exibir uma caixa de diálogo modal, permitindo que o usuário imprima o conteúdo do controle ScrollableText.

 

 



