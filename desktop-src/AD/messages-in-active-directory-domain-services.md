---
title: Mensagens em Active Directory Domain Services
description: As mensagens no Active Directory Domain Services são funcionais no Windows 2000 e Windows NT 4.0 com o Service Pack 6a (SP6a) e posterior com DSClient.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- AD de Mensagens do Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f5a9a5e92048f64cc1b49ea67cae05443eda685d588df0c78bb3f48cf0dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025914"
---
# <a name="messages-in-active-directory-domain-services"></a>Mensagens em Active Directory Domain Services

As mensagens no Active Directory Domain Services são funcionais no Windows 2000 e Windows NT 4.0 com o Service Pack 6a (SP6a) e posterior com DSClient. Eles também são funcionais em Windows de trabalho 98/95 com IE4.01 e posterior e DSClient. No entanto, se as páginas de propriedades de seleção multiseleção são lançadas do shell, a mensagem [**WM \_ ADSPROP \_ NOTIFY \_ ERROR**](wm-adsprop-notify-error.md) e suas funções auxiliares correspondentes, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) e [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) não serão funcionais e não serão exibidas. Se as páginas de propriedades de seleção multiseleção são lançadas em uma ferramenta de administração, por exemplo, Usuários e Computadores do AD, todas as mensagens são funcionais e disponíveis para serem exibidas nas páginas de propriedades de seleção multiseleção.

Active Directory Domain Services use as seguintes mensagens:

-   [**WM \_ ADSPROP \_ NOTIFY \_ APPLY**](wm-adsprop-notify-apply.md)
-   [**ALTERAÇÃO \_ DE \_ NOTIFICAÇÃO DO WM ADSPROP \_**](wm-adsprop-notify-change.md)
-   [**ERRO DE NOTIFICAÇÃO DO WM \_ ADSPROP \_ \_**](wm-adsprop-notify-error.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ EXIT**](wm-adsprop-notify-exit.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ FOREGROUND**](wm-adsprop-notify-foreground.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ PAGEHWND**](wm-adsprop-notify-pagehwnd.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ PAGEINIT**](wm-adsprop-notify-pageinit.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ SETFOCUS**](wm-adsprop-notify-setfocus.md)
-   [**WM \_ ADSPROP \_ SHEET \_ CREATE**](wm-adsprop-sheet-create.md)
-   [**NOTIFICAÇÃO DE FECHAMENTO DA PLANILHA DO WM \_ DSA \_ \_ \_**](wm-dsa-sheet-close-notify.md)
-   [**WM \_ DSA \_ SHEET \_ CREATE \_ NOTIFY**](wm-dsa-sheet-create-notify.md)

 

 




