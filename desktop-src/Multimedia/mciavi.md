---
title: MCIAVI
description: MCIAVI
ms.assetid: 68639f35-bc20-457d-b937-760af8323dce
keywords:
- Dispositivos MCI, Driver MCIAVI
- Comandos MCI, Driver MCIAVI
- Driver MCIAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a7a6bc8da314cc5cb891846e46289396fefb6be60d92ddd38f17ab1aff0ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783425"
---
# <a name="mciavi"></a>MCIAVI

Um arquivo AVI pode conter mais de dois fluxos — por exemplo, uma sequência de vídeo, uma trilha sonora em inglês e uma trilha sonora francesa. Seu aplicativo pode usar um fluxo independentemente dos outros fluxos no arquivo.

O tipo de dispositivo **DigitalVideo** controla arquivos de vídeo. Para obter uma lista dos comandos MCI reconhecidos por dispositivos de vídeo digital, consulte [conjunto de comandos de vídeo digital](digital-video-command-set.md).

O driver MCIAVI reproduz sequências de vídeo e outros fluxos de dados sob o controle de comandos MCI. Os fluxos de dados podem conter imagens, áudio e paletas. Os dados da imagem podem consistir em imagens com paletas de cores ou informações true-color.

O áudio é sincronizado com o vídeo dentro de um thirtieth de um segundo. No entanto, se o hardware de áudio não estiver disponível, o driver reproduzirá apenas o fluxo de vídeo. O driver MCIAVI pode descartar quadros de vídeo, se necessário, para reproduzir um fluxo sem interrupção de áudio.

Seu aplicativo pode usar os serviços de classe de janela MCIWnd em vez da interface de comando MCI para controlar qualquer driver MCI. Essa classe de janela lida com muitos dos detalhes do gerenciamento da janela que oferece suporte ao dispositivo MCI e simplifica a programação necessária para enviar os comandos MCI. Seu aplicativo pode usar os serviços de biblioteca do MCIWnd diretamente para controlar o dispositivo MCI ou pode ter MCIWnd exibir uma barra de ferramentas, barra de rolagem e menus que permitem ao usuário controlar o dispositivo. Para obter mais informações sobre a classe de janela MCIWnd, consulte [classe de janela MCIWnd](mciwnd-window-class.md).

 

 




