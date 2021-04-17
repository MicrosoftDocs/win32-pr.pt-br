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
# <a name="messages-in-active-directory-domain-services"></a><span data-ttu-id="7b00c-104">Mensagens em Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="7b00c-104">Messages in Active Directory Domain Services</span></span>

<span data-ttu-id="7b00c-105">As mensagens no Active Directory Domain Services são funcionais no Windows 2000 e no Windows NT 4,0 com Service Pack 6a (SP6a) e posterior com o DSClient.</span><span class="sxs-lookup"><span data-stu-id="7b00c-105">Messages in Active Directory Domain Services are functional in Windows 2000 and Windows NT 4.0 with Service Pack 6a (SP6a) and later with DSClient.</span></span> <span data-ttu-id="7b00c-106">Eles também são funcionais em estações de trabalho do Windows 98/95 com o IE 4.01 e posterior e o DSClient.</span><span class="sxs-lookup"><span data-stu-id="7b00c-106">They are also functional in Windows 98/95 workstations with IE4.01 and later and DSClient.</span></span> <span data-ttu-id="7b00c-107">No entanto, se as páginas de propriedades de seleção ascada forem iniciadas no Shell, a mensagem de [**erro de notificação do WM \_ \_ \_ ADSPROP**](wm-adsprop-notify-error.md) e suas funções auxiliares correspondentes, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) e [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) não serão funcionais e não serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="7b00c-107">However, if multiselect property pages are launched from the shell, then the [**WM\_ADSPROP\_NOTIFY\_ERROR**](wm-adsprop-notify-error.md) message and its corresponding helper functions, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) and [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) are not functional and will not be displayed.</span></span> <span data-ttu-id="7b00c-108">Se as páginas de propriedades de seleção ascada forem iniciadas dentro de uma ferramenta de administração, por exemplo, usuários e computadores do AD, todas as mensagens estarão funcionais e disponíveis para serem exibidas dentro das páginas de propriedades de seleção.</span><span class="sxs-lookup"><span data-stu-id="7b00c-108">If multiselect property pages are launched within an admin tool, for example, AD Users and Computers, then all messages are functional and available to be displayed within the multiselect property pages.</span></span>

<span data-ttu-id="7b00c-109">Active Directory Domain Services use as seguintes mensagens:</span><span class="sxs-lookup"><span data-stu-id="7b00c-109">Active Directory Domain Services use the following messages:</span></span>

-   [<span data-ttu-id="7b00c-110">**aplicação de notificação do WM \_ ADSPROP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b00c-110">**WM\_ADSPROP\_NOTIFY\_APPLY**</span></span>](wm-adsprop-notify-apply.md)
-   [<span data-ttu-id="7b00c-111">**alteração de notificação do WM \_ ADSPROP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b00c-111">**WM\_ADSPROP\_NOTIFY\_CHANGE**</span></span>](wm-adsprop-notify-change.md)
-   [<span data-ttu-id="7b00c-112">**erro de notificação do WM \_ ADSPROP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b00c-112">**WM\_ADSPROP\_NOTIFY\_ERROR**</span></span>](wm-adsprop-notify-error.md)
-   [<span data-ttu-id="7b00c-113">**saída de notificação do WM \_ ADSPROP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b00c-113">**WM\_ADSPROP\_NOTIFY\_EXIT**</span></span>](wm-adsprop-notify-exit.md)
-   [<span data-ttu-id="7b00c-114">**\_ \_ primeiro plano de notificação do WM ADSPROP \_**</span><span class="sxs-lookup"><span data-stu-id="7b00c-114">**WM\_ADSPROP\_NOTIFY\_FOREGROUND**</span></span>](wm-adsprop-notify-foreground.md)
-   [<span data-ttu-id="7b00c-115">**PAGEHWND de notificação do WM \_ ADSPROP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b00c-115">**WM\_ADSPROP\_NOTIFY\_PAGEHWND**</span></span>](wm-adsprop-notify-pagehwnd.md)
-   [<span data-ttu-id="7b00c-116">**PAGEINIT de notificação do WM \_ ADSPROP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b00c-116">**WM\_ADSPROP\_NOTIFY\_PAGEINIT**</span></span>](wm-adsprop-notify-pageinit.md)
-   [<span data-ttu-id="7b00c-117">**WM \_ ADSPROP \_ notificar \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="7b00c-117">**WM\_ADSPROP\_NOTIFY\_SETFOCUS**</span></span>](wm-adsprop-notify-setfocus.md)
-   [<span data-ttu-id="7b00c-118">**criação da planilha do WM \_ ADSPROP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b00c-118">**WM\_ADSPROP\_SHEET\_CREATE**</span></span>](wm-adsprop-sheet-create.md)
-   [<span data-ttu-id="7b00c-119">**\_notificação de \_ fechamento da folha DSA \_ do WM \_**</span><span class="sxs-lookup"><span data-stu-id="7b00c-119">**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**</span></span>](wm-dsa-sheet-close-notify.md)
-   [<span data-ttu-id="7b00c-120">**\_notificação de \_ criação da folha DSA \_ do WM \_**</span><span class="sxs-lookup"><span data-stu-id="7b00c-120">**WM\_DSA\_SHEET\_CREATE\_NOTIFY**</span></span>](wm-dsa-sheet-create-notify.md)

 

 




