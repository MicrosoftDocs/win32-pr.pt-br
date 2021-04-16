---
title: Reprodução e posicionamento
description: Reprodução e posicionamento
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efbd6256fbd0d258f5d5c9d3da9b01c72a203dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105751173"
---
# <a name="playback-and-positioning"></a>Reprodução e posicionamento

Vários comandos MCI, como [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)), [**Stop**](stop.md) ([**MCI \_ Stop**](mci-stop.md)), [**Pause**](pause.md) ([**MCI \_ Pause**](mci-pause.md)), [**retomar**](resume.md) ([**MCI \_ resume**](mci-resume.md)) e [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)), afetam a reprodução ou o posicionamento de um arquivo de multimídia. Se um dispositivo MCI receber um comando de reprodução enquanto outro comando de reprodução estiver em andamento, ele aceitará o comando e interromperá ou substituirá o comando anterior.

Muitos comandos MCI, como [**set**](set.md) ([**MCI \_ set**](mci-set.md)), não afetam a reprodução. Uma notificação de um desses comandos não interfere nos comandos de reprodução ou de posição pendentes, desde que as notificações não sejam executadas da mesma instância do driver. Por exemplo, você pode emitir um comando **set** ou [**status**](status.md) ([**\_ status MCI**](mci-status.md)) enquanto um dispositivo estiver executando um comando de **busca** sem interromper ou substituir o comando de **busca** .

No entanto, pode haver apenas uma notificação pendente. Por exemplo, se um aplicativo solicitar uma notificação para **reproduzir** e seguir essa solicitação com o **status** "Iniciar notificação de posição", a notificação de **reprodução** retornará "substituída" e a notificação para o comando de status retornará quando for concluída. Nesse caso, no entanto, o comando **Play** ainda terá sucesso, embora o aplicativo não tenha recebido a notificação.

 

 




