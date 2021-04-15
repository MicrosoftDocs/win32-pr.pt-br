---
title: Como implementar dicas de ferramenta para ícones da barra de status
description: Uma maneira não intrusiva de exibir uma mensagem explicativa para um ícone da barra de status é implementar uma dica de ferramenta. A dica de ferramenta desaparece quando clicada, mas você também pode especificar um valor de tempo limite.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277fb8d15654ae51565c1a461a9a8414d3e9213c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454385"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a><span data-ttu-id="2d465-104">Como implementar dicas de ferramenta para ícones da barra de status</span><span class="sxs-lookup"><span data-stu-id="2d465-104">How to Implement Tooltips for Status Bar Icons</span></span>

<span data-ttu-id="2d465-105">Uma maneira não intrusiva de exibir uma mensagem explicativa para um ícone da barra de status é implementar uma dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="2d465-105">A nonintrusive way to display an explanatory message for a status bar icon is to implement a tooltip.</span></span> <span data-ttu-id="2d465-106">A dica de ferramenta desaparece quando clicada, mas você também pode especificar um valor de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="2d465-106">The tooltip disappears when clicked, but you can also specify a time-out value.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="2d465-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="2d465-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2d465-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="2d465-108">Technologies</span></span>

-   [<span data-ttu-id="2d465-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="2d465-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="2d465-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="2d465-110">Prerequisites</span></span>

-   <span data-ttu-id="2d465-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="2d465-111">C/C++</span></span>
-   <span data-ttu-id="2d465-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="2d465-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="2d465-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="2d465-113">Instructions</span></span>

### <a name="implement-tooltips-for-status-bar-icons"></a><span data-ttu-id="2d465-114">Implementar dicas de ferramentas para ícones da barra de status</span><span class="sxs-lookup"><span data-stu-id="2d465-114">Implement Tooltips for Status Bar Icons</span></span>

<span data-ttu-id="2d465-115">O fragmento de código a seguir ilustra como adicionar uma dica de ferramenta de balão a um ícone de barra de status.</span><span class="sxs-lookup"><span data-stu-id="2d465-115">The following code fragment illustrates how to add a balloon tooltip to a status bar icon.</span></span>


```C++
#define ARRAYSIZE(a) (sizeof(a)/sizeof(a[0]))

NOTIFYICONDATA IconData = {0};

IconData.cbSize = sizeof(IconData);
IconData.hWnd   = hwndNI;
IconData.uFlags = NIF_INFO;

HRESULT hr = StringCchCopy(IconData.szInfo, 
                           ARRAYSIZE(IconData.szInfo), 
                           TEXT("Your message text goes here."));

if(FAILED(hr))
{
  // TODO: Write an error handler in case the call to StringCchCopy fails.
}
IconData.uTimeout = 15000; // in milliseconds

Shell_NotifyIcon(NIM_MODIFY, &IconData);
            
```



## <a name="remarks"></a><span data-ttu-id="2d465-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d465-116">Remarks</span></span>

<span data-ttu-id="2d465-117">Para obter uma discussão detalhada sobre a barra de status, consulte [a barra de tarefas](/windows/desktop/shell/taskbar).</span><span class="sxs-lookup"><span data-stu-id="2d465-117">For a detailed discussion of the status bar, see [The Taskbar](/windows/desktop/shell/taskbar).</span></span>

<span data-ttu-id="2d465-118">Para exibir uma dica de ferramenta de balão, você precisa definir o sinalizador de informações de nse \_ na estrutura [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) e usar os membros **szInfo** e **uTimeout** para especificar o texto da dica de ferramenta e a duração do tempo limite.</span><span class="sxs-lookup"><span data-stu-id="2d465-118">To display a balloon tooltip, you need to set the NIF\_INFO flag in the [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) structure, and use the **szInfo** and **uTimeout** members to specify the tooltip text and time-out duration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d465-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d465-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d465-120">Usando controles de dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="2d465-120">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 