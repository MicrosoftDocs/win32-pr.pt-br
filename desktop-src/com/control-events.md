---
title: Eventos de controle (COM)
description: Além de fornecer propriedades e métodos, um controle também fornece interfaces de saída para notificar seu cliente de eventos.
ms.assetid: e7085bc0-c087-4cc8-9c69-ba05b0923b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b987202cb4e4e635a947ed60e9f947cc428f0aaaacb3d27c27d60ad536b636
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119243626"
---
# <a name="control-events-com"></a>Eventos de controle (COM)

Além de fornecer propriedades e métodos, um controle também fornece interfaces de saída para notificar seu cliente de eventos. O cliente deve dar suporte à manipulação desses eventos. Consulte [Eventos em OBJETOS COM e Conectáveis para](events-in-com-and-connectable-objects.md) obter mais informações sobre como os objetos conectáveis funcionam.

Um controle pode dar suporte a diferentes interfaces de saída para finalidades diferentes. Todas as interfaces de saída são marcadas como interfaces de origem nas informações de tipo do controle, mas apenas uma é marcada como padrão para indicar que é a interface de saída primária.

Um contêiner pode dar suporte a uma ou mais das interfaces de saída definidas por um controle . O controle deve estar preparado para lidar com contêineres que só dão suporte a algumas de suas interfaces de saída.

Os controles são suportados por quatro tipos de eventos:

-   Solicitar eventos. Um controle solicita permissão de seu cliente para fazer algo chamando um método na interface de saída, disparando assim um evento de solicitação. O cliente sinaliza o controle por meio de um parâmetro booliana, out no método que o controle chamou. Assim, o cliente pode impedir que o controle executa a ação.
-   Antes dos eventos. Um controle notifica seu cliente de que ele fará algo chamando um método na interface de saída, disparando um evento anterior. O cliente não tem a oportunidade de impedir a ação, mas pode seguir as etapas necessárias, considerando a ação que está prestes a ocorrer.
-   Após eventos. Um controle notifica seu cliente de que ele acabou de fazer algo chamando um método na interface de saída, disparando um evento after. Novamente, o cliente não pode cancelar essa ação, mas pode tomar as etapas necessárias, considerando a ação que ocorreu.
-   Faça eventos. Um controle dispara um evento do para permitir que seu cliente substitua a ação do controle e forneça algumas ações alternativas ou complementares. Normalmente, o método que um controle chama para um evento do tem vários parâmetros para negociar com o cliente sobre as ações que ocorrerão.

Os seguintes dispids são definidos para eventos padrão que os controles podem dar suporte: Click, DblClick, KeyDown, KeyPress, KeyUp, MouseMove, MouseUp e Error. Todos esses eventos padrão têm valores DISPID negativos, indicando seu status padrão.

O [**método IOleControl::FreezeEvents,**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) quando chamado com **TRUE,** informa a um controle se o contêiner manipulará eventos do controle até **que FreezeEvents** seja chamado novamente com **FALSE.** Durante esse tempo, o controle não pode depender do contêiner realmente manipular eventos. Se um evento deve ser tratado, o controle deve enfilar o evento para a disparar quando **FreezeEvents** é chamado com **FALSE**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[ActiveX Controles](activex-controls.md)
</dt> </dl>

 

 




