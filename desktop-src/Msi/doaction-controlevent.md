---
description: O ControlEvent, DoAction notifica o instalador para executar uma ação personalizada. Esse evento pode ser publicado por um controle de pressão, controle de caixa de seleção ou um controle SelectionTree. Esse evento deve ser criado na tabela ControlEvent,.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: ControlEvent, de doação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cc16c918522408e4cdf046e95d3d822ba3ac5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089990"
---
# <a name="doaction-controlevent"></a>ControlEvent, de doação

O ControlEvent, DoAction notifica o instalador para executar uma ação personalizada. Esse evento pode ser publicado por um controle de [pressão](pushbutton-control.md) , controle de [caixa de seleção](checkbox-control.md) ou um controle [SelectionTree](selectiontree-control.md) . Esse evento deve ser criado na tabela [ControlEvent,](controlevent-table.md) .

Observe que as ações personalizadas iniciadas por uma ControlEvent, de doação podem enviar uma mensagem com o [**método Message**](session-message.md), mas não podem enviar uma mensagem com [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). Em sistemas anteriores ao Windows Server 2003, as ações personalizadas iniciadas por uma ação ControlEvent, não podem enviar mensagens com o método **MsiProcessMessage** ou **Message**. Para obter mais informações, consulte [enviando mensagens para Windows Installer usando MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter mais informações, consulte [níveis de interface do usuário](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Uma cadeia de caracteres, o nome da ação personalizada a ser executada.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Este ControlEvent, não executa uma ação nos assinantes.

## <a name="typical-use"></a>Usos comum

Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo é vinculado a esse evento na tabela [ControlEvent,](controlevent-table.md) para invocar uma ação personalizada.

 

 



