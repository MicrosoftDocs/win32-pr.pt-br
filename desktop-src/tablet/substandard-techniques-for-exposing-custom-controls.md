---
description: Descrição de técnicas de subpadrão para expor controles personalizados.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Técnicas de subpadrão para expor controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194614474596b55e0b1cf0530a07f9b3c411f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812795"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a><span data-ttu-id="05cf8-103">Técnicas de subpadrão para expor controles personalizados</span><span class="sxs-lookup"><span data-stu-id="05cf8-103">Substandard Techniques for Exposing Custom Controls</span></span>

<span data-ttu-id="05cf8-104">Se um aplicativo não oferecer suporte ao Microsoft Acessibilidade Ativa, ele poderá não estar totalmente acessível.</span><span class="sxs-lookup"><span data-stu-id="05cf8-104">If an application does not support Microsoft Active Accessibility, it may not be fully accessible.</span></span> <span data-ttu-id="05cf8-105">As técnicas a seguir renderizam os controles parcialmente compatíveis:</span><span class="sxs-lookup"><span data-stu-id="05cf8-105">The following techniques render controls partially compatible:</span></span>

-   <span data-ttu-id="05cf8-106">Retornar uma cadeia de caracteres descritiva quando o controle for consultado usando a \_ mensagem de gettext do WM.</span><span class="sxs-lookup"><span data-stu-id="05cf8-106">Return a descriptive string when the control is queried by using the WM\_GETTEXT message.</span></span> <span data-ttu-id="05cf8-107">Por exemplo, permita que um equivalente personalizado de um controle de botão rotulado como "Print" para retornar a cadeia de caracteres "botão Imprimir".</span><span class="sxs-lookup"><span data-stu-id="05cf8-107">For example, allow a custom equivalent of a button control labeled "Print" to return the string "Print button."</span></span> <span data-ttu-id="05cf8-108">Isso identifica o tipo de controle e o rótulo.</span><span class="sxs-lookup"><span data-stu-id="05cf8-108">This identifies both control type and label.</span></span> <span data-ttu-id="05cf8-109">A mesma cadeia de caracteres é apropriada para um botão com um rótulo que seja algo diferente de texto, como um gráfico de uma impressora.</span><span class="sxs-lookup"><span data-stu-id="05cf8-109">The same string is appropriate for a button with a label that is something other than text, such as a graphic of a printer.</span></span> <span data-ttu-id="05cf8-110">Da mesma forma, permita que um controle personalizado se comporta como uma caixa de seleção para retornar a cadeia de caracteres de legenda "caixa de seleção de impressão habilitada, marcada".</span><span class="sxs-lookup"><span data-stu-id="05cf8-110">Similarly, allow a custom control that behaves like a check box to return the caption string "Printing Enabled check box, checked."</span></span>
-   <span data-ttu-id="05cf8-111">Dê suporte à \_ mensagem do WM GETDLGCODE, identificando a entrada do teclado com suporte.</span><span class="sxs-lookup"><span data-stu-id="05cf8-111">Support the WM\_GETDLGCODE message, identifying the keyboard input that is supported.</span></span> <span data-ttu-id="05cf8-112">Por exemplo, permita que um equivalente personalizado de um controle de edição manipule \_ o WM GETDLGCODE retornando DLGC \_ HASSETSEL se ele tratar as mensagens para definir a seleção, DLGC \_ WANTARROWS se usar as teclas de direção e DLGC \_ WANTCHARS para indicar que ela usa a entrada de caracteres.</span><span class="sxs-lookup"><span data-stu-id="05cf8-112">For example, allow a custom equivalent of an edit control to handle WM\_GETDLGCODE by returning DLGC\_HASSETSEL if it handles messages to set the selection, DLGC\_WANTARROWS if it uses arrow keys, and DLGC\_WANTCHARS to indicate that it uses character input.</span></span>
    > [!Note]  
    > <span data-ttu-id="05cf8-113">Somente controles que têm seus próprios identificadores de janela podem responder às \_ mensagens do WM gettext e do WM \_ GETDLGCODE.</span><span class="sxs-lookup"><span data-stu-id="05cf8-113">Only controls that have their own window handles can respond to the WM\_GETTEXT and WM\_GETDLGCODE messages.</span></span>

     

<span data-ttu-id="05cf8-114">Para evitar problemas de compatibilidade com auxílios de acessibilidade, você deve seguir as diretrizes de Acessibilidade Ativa de acordo ao criar controles personalizados.</span><span class="sxs-lookup"><span data-stu-id="05cf8-114">To avoid compatibility problems with accessibility aids, you should follow Active Accessibility guidelines closely when designing custom controls.</span></span> <span data-ttu-id="05cf8-115">Para obter mais informações sobre como evitar problemas de compatibilidade com auxílios de acessibilidade, consulte a seção [acessibilidade](../accessibility/accessibility.md) .</span><span class="sxs-lookup"><span data-stu-id="05cf8-115">For more information about how to avoid compatibility problems with accessibility aids, see the [Accessibility](../accessibility/accessibility.md) section.</span></span>

 

 
