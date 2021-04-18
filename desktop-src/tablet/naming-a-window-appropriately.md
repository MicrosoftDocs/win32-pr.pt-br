---
description: Visão geral de nomear uma janela adequadamente e definir a legenda da janela para o Tablet PC.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Nomeando uma janela adequadamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaee320f621acf834d7c0ec5978a9e42f0811e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771764"
---
# <a name="naming-a-window-appropriately"></a><span data-ttu-id="1506e-103">Nomeando uma janela adequadamente</span><span class="sxs-lookup"><span data-stu-id="1506e-103">Naming a Window Appropriately</span></span>

<span data-ttu-id="1506e-104">Atribua a cada janela uma legenda amigável, mesmo se a janela ou sua legenda estiver invisível.</span><span class="sxs-lookup"><span data-stu-id="1506e-104">Assign every window a user-friendly caption, even if the window or its caption is invisible.</span></span> <span data-ttu-id="1506e-105">Isso permite que a funcionalidade de fala identifique a janela e a hierarquia da janela.</span><span class="sxs-lookup"><span data-stu-id="1506e-105">This allows the speech functionality to identify the window and the window hierarchy.</span></span> <span data-ttu-id="1506e-106">Essa recomendação se aplica a todas as janelas: janelas de nível superior com quadros visíveis; janelas filhas, como paletas flutuantes; controles personalizados; barras e painéis dentro de uma janela, quando implementados como janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="1506e-106">This recommendation applies to all windows: top-level windows with visible frames; child windows, such as floating palettes; custom controls; toolbars; and panes within a window, when implemented as child windows.</span></span>

<span data-ttu-id="1506e-107">Há três maneiras de definir a legenda da janela:</span><span class="sxs-lookup"><span data-stu-id="1506e-107">There are three ways to set the window caption:</span></span>

-   <span data-ttu-id="1506e-108">Defina a cadeia de caracteres no script de recurso ao chamar [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou funções relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1506e-108">Set the string in your resource script when calling [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or related functions.</span></span>
-   <span data-ttu-id="1506e-109">Chame a função [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="1506e-109">Call the [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) function.</span></span>
-   <span data-ttu-id="1506e-110">Defina o nome dos controles nas caixas de diálogo usando as técnicas descritas em [controles de nomenclatura nas caixas de diálogo](naming-controls-in-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="1506e-110">Define the name of controls in dialog boxes by using the techniques described in [Naming Controls in Dialog Boxes](naming-controls-in-dialog-boxes.md).</span></span> <span data-ttu-id="1506e-111">Esse é o único método para rotular um controle de edição, pois definir o rótulo intrínseco dos controles altera o conteúdo dos controles.</span><span class="sxs-lookup"><span data-stu-id="1506e-111">This is the only method for labeling an edit control, because setting the controls intrinsic label changes the controls contents.</span></span>

<span data-ttu-id="1506e-112">Você pode consultar a legenda usando o Microsoft Acessibilidade Ativa ou a mensagem de \_ gettext do WM.</span><span class="sxs-lookup"><span data-stu-id="1506e-112">You can query the caption by using either Microsoft Active Accessibility or the WM\_GETTEXT message.</span></span>

<span data-ttu-id="1506e-113">Para obter mais informações sobre como consultar a legenda usando Acessibilidade Ativa, consulte a seção [acessibilidade](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="1506e-113">For more information about querying the caption by using Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
