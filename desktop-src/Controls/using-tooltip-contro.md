---
title: Usando controles de dica de ferramenta
description: Esta seção contém exemplos que demonstram como criar diferentes tipos de dicas de ferramenta.
ms.assetid: 4486b406-a069-4250-b7ab-671d895b79f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fd4a0cef452be3f9700f8466959043ac8d30b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635743"
---
# <a name="using-tooltip-controls"></a><span data-ttu-id="9be4f-103">Usando controles de dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="9be4f-103">Using Tooltip Controls</span></span>

<span data-ttu-id="9be4f-104">Esta seção contém exemplos que demonstram como criar diferentes tipos de dicas de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="9be4f-104">This section contains examples that demonstrate how to create different types of tooltips.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9be4f-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9be4f-105">In this section</span></span>



| <span data-ttu-id="9be4f-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="9be4f-106">Topic</span></span>                                                                                                    | <span data-ttu-id="9be4f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9be4f-107">Description</span></span>                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9be4f-108">Como criar uma dica de ferramenta para um controle</span><span class="sxs-lookup"><span data-stu-id="9be4f-108">How to Create a Tooltip for a Control</span></span>](create-a-tooltip-for-a-control.md)<br/>                   | <span data-ttu-id="9be4f-109">A função de exemplo a seguir cria uma dica de ferramenta e a associa ao controle cuja ID de recurso é passada.</span><span class="sxs-lookup"><span data-stu-id="9be4f-109">The following example function creates a tooltip and associates it with the control whose resource ID is passed in.</span></span> <br/>                                                                                                                                                  |
| [<span data-ttu-id="9be4f-110">Como criar uma dica de ferramenta para uma área retangular</span><span class="sxs-lookup"><span data-stu-id="9be4f-110">How to Create a Tooltip for a Rectangular Area</span></span>](create-a-tooltip-for-a-rectangular-area.md)<br/> | <span data-ttu-id="9be4f-111">O exemplo a seguir demonstra como criar um controle de dica de ferramenta padrão para a área inteira do cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="9be4f-111">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span> <br/>                                                                                                                                                       |
| [<span data-ttu-id="9be4f-112">Como implementar dicas de ferramentas de rastreamento</span><span class="sxs-lookup"><span data-stu-id="9be4f-112">How to Implement Tracking Tooltips</span></span>](implement-tracking-tooltips.md)<br/>                         | <span data-ttu-id="9be4f-113">As dicas de ferramentas de rastreamento permanecem visíveis até que sejam explicitamente fechadas pelo aplicativo e podem alterar a posição na tela dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="9be4f-113">Tracking tooltips remain visible until they are explicitly closed by the application, and can change position on the screen dynamically.</span></span> <span data-ttu-id="9be4f-114">Eles têm suporte da [versão 4,70](common-control-versions.md) e posterior dos controles comuns.</span><span class="sxs-lookup"><span data-stu-id="9be4f-114">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span> <br/>                         |
| [<span data-ttu-id="9be4f-115">Como implementar dicas de ferramentas de várias linhas</span><span class="sxs-lookup"><span data-stu-id="9be4f-115">How to Implement Multiline Tooltips</span></span>](implement-multiline-tooltips.md)<br/>                       | <span data-ttu-id="9be4f-116">As dicas de ferramentas de várias linhas permitem que o texto seja exibido em mais de uma linha.</span><span class="sxs-lookup"><span data-stu-id="9be4f-116">Multiline tooltips allow text to be displayed on more than one line.</span></span> <br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="9be4f-117">Como implementar dicas de ferramentas de balão</span><span class="sxs-lookup"><span data-stu-id="9be4f-117">How to Implement Balloon Tooltips</span></span>](implement-balloon-tooltips.md)<br/>                           | <span data-ttu-id="9be4f-118">As dicas de ferramentas de balão são semelhantes às dicas de ferramenta padrão, mas são exibidas em um "balão" estilo animado com uma haste apontando para a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="9be4f-118">Balloon tooltips are similar to standard tooltips, but are displayed in a cartoon-style "balloon" with a stem pointing to the tool.</span></span> <span data-ttu-id="9be4f-119">As dicas de ferramentas de balão podem ser de linha única ou de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="9be4f-119">Balloon tooltips can be either single-line or multiline.</span></span> <span data-ttu-id="9be4f-120">Eles são criados e manipulados quase da mesma forma que as dicas de ferramentas padrão.</span><span class="sxs-lookup"><span data-stu-id="9be4f-120">They are created and handled in much the same way as standard tooltips.</span></span> <br/> |
| [<span data-ttu-id="9be4f-121">Como implementar dicas de ferramenta para ícones da barra de status</span><span class="sxs-lookup"><span data-stu-id="9be4f-121">How to Implement Tooltips for Status Bar Icons</span></span>](implement-tooltips-for-status-bar-icons.md)<br/> | <span data-ttu-id="9be4f-122">Uma maneira não intrusiva de exibir uma mensagem explicativa para um ícone da barra de status é implementar uma dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="9be4f-122">A nonintrusive way to display an explanatory message for a status bar icon is to implement a tooltip.</span></span> <span data-ttu-id="9be4f-123">A dica de ferramenta desaparece quando clicada, mas você também pode especificar um valor de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="9be4f-123">The tooltip disappears when clicked, but you can also specify a time-out value.</span></span> <br/>                                                                                |
| [<span data-ttu-id="9be4f-124">Como implementar dicas de ferramentas de In-Place</span><span class="sxs-lookup"><span data-stu-id="9be4f-124">How to Implement In-Place Tooltips</span></span>](implement-in-place-tooltips.md)<br/>                         | <span data-ttu-id="9be4f-125">Dicas de ferramenta in-loco são usadas para exibir cadeias de caracteres de texto para objetos que foram recortados.</span><span class="sxs-lookup"><span data-stu-id="9be4f-125">In-place tooltips are used to display text strings for objects that have been clipped.</span></span> <span data-ttu-id="9be4f-126">Para obter uma ilustração, consulte [sobre os controles de dica de ferramenta](tooltip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="9be4f-126">For an illustration, see [About Tooltip Controls](tooltip-controls.md).</span></span> <br/>                                                                                                      |



 

 

 





