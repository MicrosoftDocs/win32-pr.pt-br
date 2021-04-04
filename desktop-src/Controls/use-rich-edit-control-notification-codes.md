---
title: Como usar códigos de notificação de controle de edição avançados
description: Uma janela pai do controle de edição rico pode processar códigos de notificação para monitorar eventos que afetam o controle. Os controles de edição avançados dão suporte a todos os códigos de notificação usados com controles de edição, bem como a vários outros.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68e510bf7c5abe6109862a01d8926c8956736f9
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103917089"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a><span data-ttu-id="fb434-104">Como usar códigos de notificação de controle de edição avançados</span><span class="sxs-lookup"><span data-stu-id="fb434-104">How to Use Rich Edit Control Notification Codes</span></span>

<span data-ttu-id="fb434-105">Uma janela pai do controle de edição rico pode processar códigos de notificação para monitorar eventos que afetam o controle.</span><span class="sxs-lookup"><span data-stu-id="fb434-105">A rich edit control's parent window can process notification codes to monitor events that affect the control.</span></span> <span data-ttu-id="fb434-106">Os controles de edição avançados dão suporte a todos os códigos de notificação usados com controles de edição, bem como a vários outros.</span><span class="sxs-lookup"><span data-stu-id="fb434-106">Rich edit controls support all of the notification codes that are used with edit controls, as well as several additional ones.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="fb434-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="fb434-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="fb434-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="fb434-108">Technologies</span></span>

-   [<span data-ttu-id="fb434-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="fb434-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="fb434-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="fb434-110">Prerequisites</span></span>

-   <span data-ttu-id="fb434-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="fb434-111">C/C++</span></span>
-   <span data-ttu-id="fb434-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="fb434-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="fb434-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="fb434-113">Instructions</span></span>

### <a name="use-a-rich-edit-control-notification-code"></a><span data-ttu-id="fb434-114">Usar um código de notificação de controle de edição rico</span><span class="sxs-lookup"><span data-stu-id="fb434-114">Use a Rich Edit Control Notification Code</span></span>

<span data-ttu-id="fb434-115">Você pode determinar quais códigos de notificação um controle de edição avançado envia sua janela pai definindo sua máscara de evento.</span><span class="sxs-lookup"><span data-stu-id="fb434-115">You can determine which notification codes a rich edit control sends its parent window by setting its event mask.</span></span> <span data-ttu-id="fb434-116">Para definir a máscara de evento para um controle de edição rico, use a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="fb434-116">To set the event mask for a rich edit control, use the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="fb434-117">Você pode recuperar a máscara de evento atual para um controle de edição rico usando a mensagem em [**\_ GETEVENTMASK**](em-geteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="fb434-117">You can retrieve the current event mask for a rich edit control by using the [**EM\_GETEVENTMASK**](em-geteventmask.md) message.</span></span> <span data-ttu-id="fb434-118">Para obter uma lista de sinalizadores de máscara de evento, consulte [sinalizadores de máscara de evento de controle de edição avançada](rich-edit-control-event-mask-flags.md).</span><span class="sxs-lookup"><span data-stu-id="fb434-118">For a list of event mask flags, see [Rich Edit Control Event Mask Flags](rich-edit-control-event-mask-flags.md).</span></span>

<span data-ttu-id="fb434-119">Uma janela pai do controle de edição rico pode filtrar todas as entradas de teclado e mouse para o controle processando o código de notificação [en \_ MSGFILTER](en-msgfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="fb434-119">A rich edit control's parent window can filter all keyboard and mouse input to the control by processing the [EN\_MSGFILTER](en-msgfilter.md) notification code.</span></span> <span data-ttu-id="fb434-120">A janela pai pode impedir que a mensagem de teclado ou mouse seja processada ou pode alterar a mensagem modificando a estrutura [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) especificada.</span><span class="sxs-lookup"><span data-stu-id="fb434-120">The parent window can prevent the keyboard or mouse message from being processed or can change the message by modifying the specified [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) structure.</span></span>

<span data-ttu-id="fb434-121">Um aplicativo pode processar o código de notificação [ \_ protegido do en](en-protected.md) para detectar quando o usuário tenta modificar o texto protegido.</span><span class="sxs-lookup"><span data-stu-id="fb434-121">An application can process the [EN\_PROTECTED](en-protected.md) notification code to detect when the user attempts to modify protected text.</span></span> <span data-ttu-id="fb434-122">Para marcar um intervalo de texto como protegido, você pode definir o efeito de caractere protegido.</span><span class="sxs-lookup"><span data-stu-id="fb434-122">To mark a range of text as protected, you can set the protected character effect.</span></span>

<span data-ttu-id="fb434-123">Você pode habilitar o usuário a soltar arquivos em um controle de edição rico processando o código de notificação [en \_ DropFiles](en-dropfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="fb434-123">You can enable the user to drop files in a rich edit control by processing the [EN\_DROPFILES](en-dropfiles.md) notification code.</span></span> <span data-ttu-id="fb434-124">A estrutura [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) especificada contém informações sobre os arquivos que estão sendo removidos.</span><span class="sxs-lookup"><span data-stu-id="fb434-124">The specified [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) structure contains information about the files that are being dropped.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb434-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fb434-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb434-126">Usando controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="fb434-126">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="fb434-127">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="fb434-127">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




