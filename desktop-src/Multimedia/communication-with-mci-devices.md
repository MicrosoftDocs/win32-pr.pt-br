---
title: Comunicação com dispositivos MCI
description: Comunicação com dispositivos MCI
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- Dispositivos MCI, comunicando-se
- Macro MCIWndGetDeviceID
- função mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b5bfb7909b94bf8e71745adeeaeda61cae20ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293918"
---
# <a name="communication-with-mci-devices"></a>Comunicação com dispositivos MCI

É possível que cada dispositivo MCI use um ou mais dos seguintes como identificadores:

-   um identificador de dispositivo
-   um nome de dispositivo
-   um alias
-   o nome de arquivo do conteúdo carregado no momento.

O MCIWnd fornece macros que você pode usar para recuperar essas informações. Você pode usar essas informações para se comunicar por meio do MCI diretamente com dispositivos MCI associados ao MCIWnd Windows.

Você pode recuperar o identificador do dispositivo MCI atual usando a macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) . O identificador do dispositivo MCI é um valor numérico que identifica a instância do dispositivo MCI que seu aplicativo está usando. Seu aplicativo pode usar esse identificador ao se comunicar com um dispositivo MCI usando a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .

Para recuperar o nome do dispositivo MCI atual, use a macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) . O nome do dispositivo MCI é uma cadeia de caracteres terminada em nulo que identifica o tipo de dispositivo associado a uma janela MCIWnd. Seu aplicativo pode usar esse nome ao se comunicar com um dispositivo MCI usando o **mciSendCommand**.

Você pode recuperar o alias do dispositivo MCI atual usando a macro [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) . Seu aplicativo pode usar esse alias ao se comunicar com um dispositivo MCI usando a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .

Por fim, você pode recuperar o nome de arquivo usado por um dispositivo MCI usando a macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) . O nome do arquivo identifica o conteúdo atualmente associado a uma janela MCIWnd. Seu aplicativo pode usar esse nome de arquivo ao se comunicar com um dispositivo MCI usando **mciSendCommand** ou **mciSendString**.

 

 