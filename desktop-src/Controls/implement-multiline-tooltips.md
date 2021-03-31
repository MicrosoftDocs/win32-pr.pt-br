---
title: Como implementar dicas de ferramentas de várias linhas
description: As dicas de ferramentas de várias linhas permitem que o texto seja exibido em mais de uma linha.
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d6f32d638b2d33ea6270aa5f8ce2c09f0f4174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635289"
---
# <a name="how-to-implement-multiline-tooltips"></a><span data-ttu-id="a1953-103">Como implementar dicas de ferramentas de várias linhas</span><span class="sxs-lookup"><span data-stu-id="a1953-103">How to Implement Multiline Tooltips</span></span>

<span data-ttu-id="a1953-104">As dicas de ferramentas de várias linhas permitem que o texto seja exibido em mais de uma linha.</span><span class="sxs-lookup"><span data-stu-id="a1953-104">Multiline tooltips allow text to be displayed on more than one line.</span></span>

<span data-ttu-id="a1953-105">Eles têm suporte da [versão 4,70](common-control-versions.md) e posterior dos controles comuns.</span><span class="sxs-lookup"><span data-stu-id="a1953-105">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span> <span data-ttu-id="a1953-106">Seu aplicativo cria uma dica de ferramenta de várias linhas enviando uma mensagem [**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) , especificando a largura do retângulo de exibição.</span><span class="sxs-lookup"><span data-stu-id="a1953-106">Your application creates a multiline tooltip by sending a [**TTM\_SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) message, specifying the width of the display rectangle.</span></span> <span data-ttu-id="a1953-107">O texto que excede essa largura é quebrado para a próxima linha em vez de alargar a região de exibição.</span><span class="sxs-lookup"><span data-stu-id="a1953-107">Text that exceeds this width wraps to the next line rather than widening the display region.</span></span> <span data-ttu-id="a1953-108">A altura do retângulo é aumentada conforme necessário para acomodar as linhas adicionais.</span><span class="sxs-lookup"><span data-stu-id="a1953-108">The rectangle height is increased as needed to accommodate the additional lines.</span></span> <span data-ttu-id="a1953-109">O controle ToolTip encapsula as linhas automaticamente, ou você pode usar uma combinação de retorno de carro/alimentação de linha, \\ r \\ n, para forçar quebras de linha em locais específicos.</span><span class="sxs-lookup"><span data-stu-id="a1953-109">The tooltip control wraps the lines automatically, or you can use a carriage return/line feed combination, \\r\\n, to force line breaks at particular locations.</span></span>

<span data-ttu-id="a1953-110">A exibição resultante é mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="a1953-110">The resulting display is shown in the following illustration.</span></span>

![captura de tela de uma caixa de diálogo com uma dica de ferramenta que contém texto organizado como um parágrafo de várias linhas](images/tt-multiline.png)

> [!Note]  
> <span data-ttu-id="a1953-112">O buffer de texto especificado pelo membro **szText** da estrutura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) pode acomodar apenas 80 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a1953-112">The text buffer specified by the **szText** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure can accommodate only 80 characters.</span></span> <span data-ttu-id="a1953-113">Se você precisar usar uma cadeia de caracteres mais longa, aponte o membro **lpszText** de **NMTTDISPINFO** para um buffer que contém o texto desejado.</span><span class="sxs-lookup"><span data-stu-id="a1953-113">If you need to use a longer string, point the **lpszText** member of **NMTTDISPINFO** to a buffer containing the desired text.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="a1953-114">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="a1953-114">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a1953-115">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="a1953-115">Technologies</span></span>

-   [<span data-ttu-id="a1953-116">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="a1953-116">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a1953-117">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a1953-117">Prerequisites</span></span>

-   <span data-ttu-id="a1953-118">C/C++</span><span class="sxs-lookup"><span data-stu-id="a1953-118">C/C++</span></span>
-   <span data-ttu-id="a1953-119">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="a1953-119">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a1953-120">Instruções</span><span class="sxs-lookup"><span data-stu-id="a1953-120">Instructions</span></span>

### <a name="implement-multiline-tooltips"></a><span data-ttu-id="a1953-121">Implementar dicas de ferramentas de várias linhas</span><span class="sxs-lookup"><span data-stu-id="a1953-121">Implement Multiline Tooltips</span></span>

<span data-ttu-id="a1953-122">O fragmento de código a seguir é um exemplo de um manipulador de notificação [TTN \_ GETDISPINFO](ttn-getdispinfo.md) simples.</span><span class="sxs-lookup"><span data-stu-id="a1953-122">The following code fragment is an example of a simple [TTN\_GETDISPINFO](ttn-getdispinfo.md) notification handler.</span></span> <span data-ttu-id="a1953-123">Ele habilita uma dica de ferramenta de várias linhas definindo o retângulo de exibição como 150 pixels.</span><span class="sxs-lookup"><span data-stu-id="a1953-123">It enables a multiline tooltip by setting the display rectangle to 150 pixels.</span></span> <span data-ttu-id="a1953-124">Uma quebra de linha manual é inserida após a primeira palavra para mostrar que as quebras de linha podem ser difíceis e flexíveis.</span><span class="sxs-lookup"><span data-stu-id="a1953-124">A manual line break is inserted after the first word to show that line breaks can be hard as well as soft.</span></span>


```C++
    case WM_NOTIFY:
    {
        switch (((LPNMHDR)lParam)->code)
        {
        case TTN_GETDISPINFO:
            LPNMTTDISPINFO pInfo = (LPNMTTDISPINFO)lParam;
            SendMessage(pInfo->hdr.hwndFrom, TTM_SETMAXTIPWIDTH, 0, 150);
            wcscpy_s(pInfo->szText, ARRAYSIZE(pInfo->szText), 
                L"This\nis a very long text string " \
                L"that must be broken into several lines.");
            break;
        }
        break;
    }
```



## <a name="related-topics"></a><span data-ttu-id="a1953-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1953-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1953-126">Usando controles de dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="a1953-126">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




