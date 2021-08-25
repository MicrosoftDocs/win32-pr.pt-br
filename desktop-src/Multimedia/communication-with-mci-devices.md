---
title: Comunicação com dispositivos MCI
description: Comunicação com dispositivos MCI
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- Dispositivos MCI, comunicando
- Macro MCIWndGetDeviceID
- Função mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd04187b948adf144a317a1d9eab80efb60bab8e7b05eaccffeb34722baa98a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785896"
---
# <a name="communication-with-mci-devices"></a>Comunicação com dispositivos MCI

É possível que cada dispositivo MCI use um ou mais dos seguintes como identificadores:

-   um identificador de dispositivo
-   um nome de dispositivo
-   um alias
-   o nome do arquivo do conteúdo carregado no momento.

O MCIWnd fornece macros que você pode usar para recuperar essas informações. Em seguida, você pode usar essas informações para se comunicar por meio da MCI diretamente com dispositivos MCI associados às janelas MCIWnd.

Você pode recuperar o identificador do dispositivo MCI atual usando a macro [**MCIWndGetDeviceID.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) O identificador de dispositivo MCI é um valor numérico que identifica a instância do dispositivo MCI que seu aplicativo está usando. Seu aplicativo pode usar esse identificador ao se comunicar com um dispositivo MCI usando a [**função mciSendCommand.**](/previous-versions//dd757160(v=vs.85))

Para recuperar o nome do dispositivo MCI atual, use a macro [**MCIWndGetDevice.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) O nome do dispositivo MCI é uma cadeia de caracteres terminada em nulo que identifica o tipo de dispositivo associado a uma janela MCIWnd. Seu aplicativo pode usar esse nome ao se comunicar com um dispositivo MCI usando **mciSendCommand**.

Você pode recuperar o alias do dispositivo MCI atual usando a macro [**MCIWndGetAlias.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) Seu aplicativo pode usar esse alias ao se comunicar com um dispositivo MCI usando a [**função mciSendString.**](/previous-versions//dd757161(v=vs.85))

Por fim, você pode recuperar o nome de arquivo usado por um dispositivo MCI usando a macro [**MCIWndGetFileName.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) O nome do arquivo identifica o conteúdo atualmente associado a uma janela MCIWnd. Seu aplicativo pode usar esse nome de arquivo ao se comunicar com um dispositivo MCI usando **mciSendCommand** ou **mciSendString**.

 

 