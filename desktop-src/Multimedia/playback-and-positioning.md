---
title: Reprodução e posicionamento
description: Reprodução e posicionamento
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9993c2ed4402184d2b15d5c3e54bb0137d1e7a3fe34f8cca36559ca329ada9d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892966"
---
# <a name="playback-and-positioning"></a>Reprodução e posicionamento

Vários comandos MCI, como [**play**](play.md) ([**MCI \_ PLAY**](mci-play.md)), [**stop**](stop.md) ([**MCI \_ STOP**](mci-stop.md)), [**pause**](pause.md) ([**MCI \_ PAUSE**](mci-pause.md)), [**resume**](resume.md) ([**MCI \_ RESUME**](mci-resume.md)) e [**seek**](seek.md) ([**MCI \_ SEEK**](mci-seek.md)), afetam a reprodução ou o posicionamento de um arquivo multimídia. Se um dispositivo MCI receber um comando de reprodução enquanto outro comando de reprodução estiver em andamento, ele aceitará o comando e para ou sobressanda o comando anterior.

Muitos comandos MCI, como [**set**](set.md) ([**MCI \_ SET**](mci-set.md)), não afetam a reprodução. Uma notificação de um desses comandos não interfere na reprodução ou nos comandos de posição pendentes, desde que as notificações não sejam executadas na mesma instância do driver. Por exemplo, você pode emitir um comando **set** ou [**status**](status.md) [**\_ (STATUS da MCI)**](mci-status.md)enquanto um dispositivo está executando um comando **seek** sem parar ou sobressu por meio **do comando seek.**

No entanto, pode haver apenas uma notificação pendente. Por exemplo, se um aplicativo  solicitar uma notificação para reprodução e seguir  essa solicitação com **o status** "notificação de posição inicial", a notificação de reprodução retornará "sobressalo" e a notificação para o comando de status retornará quando ela for concluída. Nesse caso, no entanto, o **comando play** ainda terá êxito, mesmo que o aplicativo não tenha recebido a notificação.

 

 




