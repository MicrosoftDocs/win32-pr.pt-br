---
description: O sistema fornece seis fontes de estoque.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Usando uma fonte de estoque para desenhar texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a7e580175956185bcc26a7ebbae8d46dfff078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922498"
---
# <a name="using-a-stock-font-to-draw-text"></a><span data-ttu-id="508bb-103">Usando uma fonte de estoque para desenhar texto</span><span class="sxs-lookup"><span data-stu-id="508bb-103">Using a Stock Font to Draw Text</span></span>

<span data-ttu-id="508bb-104">O sistema fornece seis fontes de estoque.</span><span class="sxs-lookup"><span data-stu-id="508bb-104">The system provides six stock fonts.</span></span> <span data-ttu-id="508bb-105">Uma fonte de ações é uma fonte lógica que um aplicativo pode obter chamando a função [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) e especificando a fonte solicitada.</span><span class="sxs-lookup"><span data-stu-id="508bb-105">A stock font is a logical font that an application can obtain by calling the [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function and specifying the requested font.</span></span> <span data-ttu-id="508bb-106">A lista a seguir contém os valores que você pode especificar para obter uma fonte de estoque.</span><span class="sxs-lookup"><span data-stu-id="508bb-106">The following list contains the values that you can specify to obtain a stock font.</span></span>



| <span data-ttu-id="508bb-107">Valor</span><span class="sxs-lookup"><span data-stu-id="508bb-107">Value</span></span>                 | <span data-ttu-id="508bb-108">Significado</span><span class="sxs-lookup"><span data-stu-id="508bb-108">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="508bb-109">\_fonte fixa \_ ANSI</span><span class="sxs-lookup"><span data-stu-id="508bb-109">ANSI\_FIXED\_FONT</span></span>     | <span data-ttu-id="508bb-110">Especifica uma fonte monospace com base no conjunto de caracteres do Windows.</span><span class="sxs-lookup"><span data-stu-id="508bb-110">Specifies a monospace font based on the Windows character set.</span></span> <span data-ttu-id="508bb-111">Uma fonte Courier normalmente é usada.</span><span class="sxs-lookup"><span data-stu-id="508bb-111">A Courier font is typically used.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="508bb-112">\_fonte de var ANSI \_</span><span class="sxs-lookup"><span data-stu-id="508bb-112">ANSI\_VAR\_FONT</span></span>       | <span data-ttu-id="508bb-113">Especifica uma fonte proporcional com base no conjunto de caracteres do Windows.</span><span class="sxs-lookup"><span data-stu-id="508bb-113">Specifies a proportional font based on the Windows character set.</span></span> <span data-ttu-id="508bb-114">MS Sans Serif é normalmente usado.</span><span class="sxs-lookup"><span data-stu-id="508bb-114">MS Sans Serif is typically used.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="508bb-115">\_fonte padrão do dispositivo \_</span><span class="sxs-lookup"><span data-stu-id="508bb-115">DEVICE\_DEFAULT\_FONT</span></span> | <span data-ttu-id="508bb-116">Especifica a fonte preferencial para o dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="508bb-116">Specifies the preferred font for the specified device.</span></span> <span data-ttu-id="508bb-117">Normalmente, essa é a fonte do sistema para dispositivos de vídeo; no entanto, para algumas impressoras de matriz de pontos, essa é uma fonte residente no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="508bb-117">This is typically the System font for display devices; however, for some dot-matrix printers this is a font that is resident on the device.</span></span> <span data-ttu-id="508bb-118">(A impressão com essa fonte geralmente é mais rápida do que a impressão com uma fonte de bitmap baixada).</span><span class="sxs-lookup"><span data-stu-id="508bb-118">(Printing with this font is usually faster than printing with a downloaded, bitmap font).</span></span>    |
| <span data-ttu-id="508bb-119">\_fonte fixa do OEM \_</span><span class="sxs-lookup"><span data-stu-id="508bb-119">OEM\_FIXED\_FONT</span></span>      | <span data-ttu-id="508bb-120">Especifica uma fonte monospace com base em um conjunto de caracteres OEM.</span><span class="sxs-lookup"><span data-stu-id="508bb-120">Specifies a monospace font based on an OEM character set.</span></span> <span data-ttu-id="508bb-121">Para computadores IBM e compatíveis, a fonte OEM é baseada no conjunto de caracteres do PC IBM.</span><span class="sxs-lookup"><span data-stu-id="508bb-121">For IBM computers and compatibles, the OEM font is based on the IBM PC character set.</span></span>                                                                                                                                                 |
| <span data-ttu-id="508bb-122">fonte do sistema \_</span><span class="sxs-lookup"><span data-stu-id="508bb-122">SYSTEM\_FONT</span></span>          | <span data-ttu-id="508bb-123">Especifica a fonte do sistema.</span><span class="sxs-lookup"><span data-stu-id="508bb-123">Specifies the System font.</span></span> <span data-ttu-id="508bb-124">Essa é uma fonte proporcional baseada no conjunto de caracteres do Windows e é usada pelo sistema operacional para exibir títulos de janela, nomes de menu e texto nas caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="508bb-124">This is a proportional font based on the Windows character set, and is used by the operating system to display window titles, menu names, and text in dialog boxes.</span></span> <span data-ttu-id="508bb-125">A fonte do sistema está sempre disponível.</span><span class="sxs-lookup"><span data-stu-id="508bb-125">The System font is always available.</span></span> <span data-ttu-id="508bb-126">Outras fontes estarão disponíveis somente se tiverem sido instaladas.</span><span class="sxs-lookup"><span data-stu-id="508bb-126">Other fonts are available only if they have been installed.</span></span> |
| <span data-ttu-id="508bb-127">\_fonte fixa do sistema \_</span><span class="sxs-lookup"><span data-stu-id="508bb-127">SYSTEM\_FIXED\_FONT</span></span>   | <span data-ttu-id="508bb-128">Especifica uma fonte monospace compatível com a fonte do sistema nas versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="508bb-128">Specifies a monospace font compatible with the System font in early versions of Windows.</span></span>                                                                                                                                                                                                        |



 

<span data-ttu-id="508bb-129">Para obter mais informações sobre fontes, consulte [about fonts](about-fonts.md).</span><span class="sxs-lookup"><span data-stu-id="508bb-129">For more information on fonts, see [About Fonts](about-fonts.md).</span></span>

<span data-ttu-id="508bb-130">O exemplo a seguir recupera um identificador para a fonte de ações da variável, seleciona-a em um contexto de dispositivo e, em seguida, grava uma cadeia de caracteres usando essa fonte:</span><span class="sxs-lookup"><span data-stu-id="508bb-130">The following example retrieves a handle to the variable stock font, selects it into a device context, and then writes a string using that font:</span></span>


```C++
HFONT hFont, hOldFont; 

// Retrieve a handle to the variable stock font.  
hFont = (HFONT)GetStockObject(ANSI_VAR_FONT); 

// Select the variable stock font into the specified device context. 
if (hOldFont = (HFONT)SelectObject(hdc, hFont)) 
{
    // Display the text string.  
    TextOut(hdc, 10, 50, L"Sample ANSI_VAR_FONT text", 25); 

    // Restore the original font.        
    SelectObject(hdc, hOldFont); 
}
```



<span data-ttu-id="508bb-131">Se outras fontes de estoque não estiverem disponíveis, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) retornará um identificador para a fonte do sistema (fonte do sistema \_ ).</span><span class="sxs-lookup"><span data-stu-id="508bb-131">If other stock fonts are not available, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) returns a handle to the System font (SYSTEM\_FONT).</span></span> <span data-ttu-id="508bb-132">Você deve usar fontes de estoque somente se o modo de mapeamento para o contexto do dispositivo do seu aplicativo for um \_ texto mm.</span><span class="sxs-lookup"><span data-stu-id="508bb-132">You should use stock fonts only if the mapping mode for your application's device context is MM\_TEXT.</span></span>

 

 



