---
description: Uma janela filho é uma janela com o \_ estilo WS Child ou WS \_ CHILDWINDOW.
ms.assetid: d8110492-c1b9-4b49-9b34-587adb7c65c9
title: Região de atualização da janela filho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf702855e506424a08e5be6c6b0cfe514035f1c54348306475140fb7fc440a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105891"
---
# <a name="child-window-update-region"></a>Região de atualização da janela filho

Uma janela filho é uma janela com o \_ estilo WS Child ou WS \_ CHILDWINDOW. Como outros estilos de janela, as janelas filhas recebem mensagens de [**\_ pintura do WM**](wm-paint.md) para solicitar a atualização. Cada janela filho tem uma região de atualização, que o sistema ou o aplicativo pode definir para gerar mensagens eventuales de **\_ pintura do WM** .

As regiões de atualização e visíveis de uma janela filho são afetadas pela janela pai do filho; Isso não é verdade para o Windows de outros estilos. O sistema geralmente define a região de atualização da janela filho quando define a região de atualização da janela pai, fazendo com que a janela filho receba mensagens do [**WM \_ Paint**](wm-paint.md) quando a janela pai as recebe. O sistema limita o local da região visível da janela filho para dentro da área do cliente da janela pai e corta qualquer parte da janela filho movida para fora da janela pai.

O sistema define a região de atualização para uma janela filho sempre que parte da região de atualização da janela pai inclui uma parte da janela filho. Nesses casos, o sistema primeiro envia uma mensagem [**de \_ pintura do WM**](wm-paint.md) para a janela pai e, em seguida, envia uma mensagem para a janela filho, permitindo que o filho restaure qualquer parte da janela que o pai tenha desenhado.

O sistema não define a região de atualização do pai quando o filho é definido. Um aplicativo não pode gerar uma mensagem de [**\_ pintura do WM**](wm-paint.md) para a janela pai invalidando a janela filho. Da mesma forma, um aplicativo não pode gerar uma mensagem do **WM \_ Paint** para o filho ao invalidar uma parte da área do cliente pai que está inteiramente sob a janela filho. Nesses casos, nenhuma janela recebe uma mensagem do **WM \_ Paint** .

Um aplicativo pode impedir que uma região de atualização da janela filho seja definida quando a janela pai é definida especificando o estilo WS \_ CLIPCHILDREN ao criar a janela pai. Quando esse estilo é definido, o sistema exclui as janelas filhas da região visível do pai e, portanto, ignora qualquer parte da região de atualização que possa conter as janelas filhas. Quando o aplicativo pinta na janela pai, qualquer desenho que cubra a janela filho é recortado, tornando desnecessária uma mensagem [**de \_ pintura do WM**](wm-paint.md) subsequente para a janela filho.

As regiões de atualização e visíveis de uma janela filho também são afetadas pelos irmãos da janela filho. As janelas irmãos são todas as janelas que têm uma janela pai comum. Se a sobreposição de janelas irmãos, a configuração da região de atualização para uma afetará a região de atualização de outra, fazendo com que as mensagens do [**WM \_ Paint**](wm-paint.md) sejam enviadas para ambas as janelas. Se uma janela na cadeia pai for composta (uma janela com WX \_ ex \_ composta), o Windows irmão receberá mensagens **de \_ pintura do WM** na ordem inversa de sua posição na ordem Z. Considerando isso, a janela mais alta na ordem Z (na parte superior) recebe sua mensagem do **WM \_ Paint** por último e vice-versa. Se uma janela na cadeia pai não for composta, o Windows irmão receberá mensagens de **\_ pintura do WM** na ordem Z.

As janelas irmãs não são recortadas automaticamente. Um irmão pode desenhar sobre outro irmão sobreposto, mesmo se a janela que está sendo desenhada tiver uma posição inferior na ordem Z. Um aplicativo pode impedir isso especificando o estilo WS \_ CLIPSIBLINGS ao criar as janelas. Quando esse estilo é definido, o sistema exclui todas as partes de uma janela irmã sobreposta da região visível de uma janela se a janela irmã sobreposta tiver uma posição mais alta na ordem Z.

> [!Note]  
> As regiões de atualização e visíveis para Windows que têm o \_ estilo WS Popup ou WS \_ POPUPWINDOW não são afetadas por suas janelas pai.

 

 

 



