---
title: Mensagens em Active Directory Domain Services
description: As mensagens no Active Directory Domain Services são funcionais no Windows 2000 e no Windows NT 4,0 com Service Pack 6a (SP6a) e posterior com o DSClient.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- ANÚNCIO de mensagens de Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6895aee711af04778318cf42920d0b0416725205
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105769082"
---
# <a name="messages-in-active-directory-domain-services"></a>Mensagens em Active Directory Domain Services

As mensagens no Active Directory Domain Services são funcionais no Windows 2000 e no Windows NT 4,0 com Service Pack 6a (SP6a) e posterior com o DSClient. Eles também são funcionais em estações de trabalho do Windows 98/95 com o IE 4.01 e posterior e o DSClient. No entanto, se as páginas de propriedades de seleção ascada forem iniciadas no Shell, a mensagem de [**erro de notificação do WM \_ \_ \_ ADSPROP**](wm-adsprop-notify-error.md) e suas funções auxiliares correspondentes, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) e [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) não serão funcionais e não serão exibidas. Se as páginas de propriedades de seleção ascada forem iniciadas dentro de uma ferramenta de administração, por exemplo, usuários e computadores do AD, todas as mensagens estarão funcionais e disponíveis para serem exibidas dentro das páginas de propriedades de seleção.

Active Directory Domain Services use as seguintes mensagens:

-   [**aplicação de notificação do WM \_ ADSPROP \_ \_**](wm-adsprop-notify-apply.md)
-   [**alteração de notificação do WM \_ ADSPROP \_ \_**](wm-adsprop-notify-change.md)
-   [**erro de notificação do WM \_ ADSPROP \_ \_**](wm-adsprop-notify-error.md)
-   [**saída de notificação do WM \_ ADSPROP \_ \_**](wm-adsprop-notify-exit.md)
-   [**\_ \_ primeiro plano de notificação do WM ADSPROP \_**](wm-adsprop-notify-foreground.md)
-   [**PAGEHWND de notificação do WM \_ ADSPROP \_ \_**](wm-adsprop-notify-pagehwnd.md)
-   [**PAGEINIT de notificação do WM \_ ADSPROP \_ \_**](wm-adsprop-notify-pageinit.md)
-   [**WM \_ ADSPROP \_ notificar \_ SETFOCUS**](wm-adsprop-notify-setfocus.md)
-   [**criação da planilha do WM \_ ADSPROP \_ \_**](wm-adsprop-sheet-create.md)
-   [**\_notificação de \_ fechamento da folha DSA \_ do WM \_**](wm-dsa-sheet-close-notify.md)
-   [**\_notificação de \_ criação da folha DSA \_ do WM \_**](wm-dsa-sheet-create-notify.md)

 

 




