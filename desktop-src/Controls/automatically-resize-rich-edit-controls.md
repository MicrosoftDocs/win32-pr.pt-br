---
title: Como redimensionar automaticamente os controles de edição avançados
description: Um aplicativo pode redimensionar um controle de edição rico conforme necessário para que seja sempre o mesmo tamanho que seu conteúdo.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ead05c4c04526a9290dc115f7a2fa7741397
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008456"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a><span data-ttu-id="1d0c9-103">Como redimensionar automaticamente os controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="1d0c9-103">How to Automatically Resize Rich Edit Controls</span></span>

<span data-ttu-id="1d0c9-104">Um aplicativo pode redimensionar um controle de edição rico conforme necessário para que seja sempre o mesmo tamanho que seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1d0c9-104">An application can resize a rich edit control as needed so that it is always the same size as its contents.</span></span> <span data-ttu-id="1d0c9-105">Um controle de edição rico dá suporte a essa chamada de funcionalidade *inferior* , enviando sua janela pai um código de notificação [en \_ REQUESTRESIZE](en-requestresize.md) sempre que o tamanho do conteúdo do controle é alterado.</span><span class="sxs-lookup"><span data-stu-id="1d0c9-105">A rich edit control supports this so-called *bottomless* functionality by sending its parent window an [EN\_REQUESTRESIZE](en-requestresize.md) notification code whenever the size of the control's content changes.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1d0c9-106">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="1d0c9-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1d0c9-107">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="1d0c9-107">Technologies</span></span>

-   [<span data-ttu-id="1d0c9-108">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="1d0c9-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1d0c9-109">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="1d0c9-109">Prerequisites</span></span>

-   <span data-ttu-id="1d0c9-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="1d0c9-110">C/C++</span></span>
-   <span data-ttu-id="1d0c9-111">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="1d0c9-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1d0c9-112">Instruções</span><span class="sxs-lookup"><span data-stu-id="1d0c9-112">Instructions</span></span>

### <a name="automatically-resize-a-rich-edit-control"></a><span data-ttu-id="1d0c9-113">Redimensionar automaticamente um controle de edição rico</span><span class="sxs-lookup"><span data-stu-id="1d0c9-113">Automatically Resize a Rich Edit Control</span></span>

<span data-ttu-id="1d0c9-114">Ao processar o código de notificação [en \_ REQUESTRESIZE](en-requestresize.md) , um aplicativo deve redimensionar o controle para as dimensões na estrutura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) especificada.</span><span class="sxs-lookup"><span data-stu-id="1d0c9-114">When processing the [EN\_REQUESTRESIZE](en-requestresize.md) notification code, an application should resize the control to the dimensions in the specified [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) structure.</span></span> <span data-ttu-id="1d0c9-115">Um aplicativo também pode mover qualquer informação que esteja perto do controle para acomodar a alteração do controle na altura.</span><span class="sxs-lookup"><span data-stu-id="1d0c9-115">An application might also move any information that is near the control to accommodate the control's change in height.</span></span> <span data-ttu-id="1d0c9-116">Para redimensionar o controle, você pode usar a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) .</span><span class="sxs-lookup"><span data-stu-id="1d0c9-116">To resize the control, you can use the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function.</span></span>

<span data-ttu-id="1d0c9-117">Você pode forçar um controle de edição mais baixo para enviar um código de notificação [en \_ REQUESTRESIZE](en-requestresize.md) usando a mensagem em [**\_ REQUESTRESIZE**](em-requestresize.md) .</span><span class="sxs-lookup"><span data-stu-id="1d0c9-117">You can force a bottomless rich edit control to send an [EN\_REQUESTRESIZE](en-requestresize.md) notification code by using the [**EM\_REQUESTRESIZE**](em-requestresize.md) message.</span></span> <span data-ttu-id="1d0c9-118">Essa mensagem pode ser útil ao processar a mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) .</span><span class="sxs-lookup"><span data-stu-id="1d0c9-118">This message can be useful when processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d0c9-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d0c9-119">Remarks</span></span>

<span data-ttu-id="1d0c9-120">Para receber códigos de notificação do [en \_ REQUESTRESIZE](en-requestresize.md) , você deve habilitar a notificação usando a mensagem em [ \_ SETEVENTMASK](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="1d0c9-120">To receive [EN\_REQUESTRESIZE](en-requestresize.md) notification codes, you must enable the notification by using the [EM\_SETEVENTMASK](em-seteventmask.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d0c9-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d0c9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d0c9-122">Usando controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="1d0c9-122">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="1d0c9-123">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="1d0c9-123">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 