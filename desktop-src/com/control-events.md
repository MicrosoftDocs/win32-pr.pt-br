---
title: Eventos de controle (COM)
description: Além de fornecer propriedades e métodos, um controle também fornece interfaces de saída para notificar seu cliente de eventos.
ms.assetid: e7085bc0-c087-4cc8-9c69-ba05b0923b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1833e1396847e09366d1e06193196cfcf981d330
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008719"
---
# <a name="control-events-com"></a>Eventos de controle (COM)

Além de fornecer propriedades e métodos, um controle também fornece interfaces de saída para notificar seu cliente de eventos. O cliente deve dar suporte ao tratamento desses eventos. Consulte [eventos em objetos com e conectáveis](events-in-com-and-connectable-objects.md) para obter mais informações sobre como os objetos conectáveis funcionam.

Um controle pode dar suporte a diferentes interfaces de saída para finalidades diferentes. Todas as interfaces de saída são marcadas como interfaces de origem nas informações de tipo do controle, mas apenas uma é marcada como padrão para indicar que é a interface de saída primária.

Um contêiner pode dar suporte a uma ou mais das interfaces de saída definidas por um controle. O controle deve ser preparado para lidar com contêineres que dão suporte apenas a algumas de suas interfaces de saída.

Os controles dão suporte a quatro tipos de eventos:

-   Eventos de solicitação. Um controle solicita permissão de seu cliente para fazer algo chamando um método na interface de saída, disparando assim um evento de solicitação. O cliente sinaliza o controle por meio de um booliano, out-Parameter no método chamado pelo controle. O cliente pode, portanto, impedir que o controle execute a ação.
-   Eventos Before. Um controle notifica seu Client Hat que fará algo chamando um método na interface de saída, disparando assim um evento Before. O cliente não tem a oportunidade de evitar a ação, mas pode executar todas as etapas necessárias, dada a ação que está prestes a ocorrer.
-   Após eventos. Um controle notifica seu cliente de que acabou de fazer algo chamando um método na interface de saída, disparando assim um evento After. Novamente, o cliente não pode cancelar essa ação, mas pode tomar as medidas necessárias devido à ação que ocorreu.
-   Fazer eventos. Um controle dispara um evento do para permitir que seu cliente substitua a ação do controle e forneça algumas ações alternativas ou complementares. Normalmente, o método que um controle chama para um evento do tem um número de parâmetros para negociar com o cliente sobre as ações que ocorrerão.

Os seguintes DISPIDs são definidos para eventos padrão aos quais os controles podem dar suporte: clique, DblClick, KeyDown, KeyPress, KeyUp, MouseMove, MouseUp e erro. Todos esses eventos padrão têm valores DISPID negativos, indicando seu status padrão.

O método [**IOleControl:: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) , quando chamado com **true**, informa a um controle se o contêiner irá se preocupar em manipular eventos do controle até que **FreezeEvents** seja chamado novamente com **false**. Durante esse tempo, o controle não pode depender do contêiner que realmente manipula todos os eventos. Se for necessário manipular um evento, o controle deverá enfileirar o evento para que ele seja acionado quando **FreezeEvents** for chamado com **false**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 




