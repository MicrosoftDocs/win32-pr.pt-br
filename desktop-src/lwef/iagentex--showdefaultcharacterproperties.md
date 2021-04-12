---
title: IAgentEx ShowDefaultCharacterProperties
description: IAgentEx ShowDefaultCharacterProperties
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65436135d9763f1cb75db6fb92b9e5f0672e17a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454050"
---
# <a name="iagentexshowdefaultcharacterproperties"></a><span data-ttu-id="bed67-103">IAgentEx::ShowDefaultCharacterProperties</span><span class="sxs-lookup"><span data-stu-id="bed67-103">IAgentEx::ShowDefaultCharacterProperties</span></span>

<span data-ttu-id="bed67-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bed67-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

<span data-ttu-id="bed67-105">Exibe a janela Propriedades de caractere padrão.</span><span class="sxs-lookup"><span data-stu-id="bed67-105">Displays default character properties window.</span></span>

-   <span data-ttu-id="bed67-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bed67-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bed67-107"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="bed67-107"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="bed67-108">A coordenada x da janela em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="bed67-108">The x-coordinate of the window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="bed67-109"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="bed67-109"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="bed67-110">A coordenada y da janela em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="bed67-110">The y-coordinate of the window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="bed67-111"><span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*</span><span class="sxs-lookup"><span data-stu-id="bed67-111"><span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*</span></span>
</dt> <dd>

<span data-ttu-id="bed67-112">Sinalizador de posição padrão.</span><span class="sxs-lookup"><span data-stu-id="bed67-112">Default position flag.</span></span> <span data-ttu-id="bed67-113">Se esse parâmetro for **true**, o Microsoft Agent exibirá a janela da folha de propriedades para o caractere padrão no último local exibido.</span><span class="sxs-lookup"><span data-stu-id="bed67-113">If this parameter is **True**, Microsoft Agent displays the property sheet window for the default character at the last location it appeared.</span></span>

> [!Note]  
> <span data-ttu-id="bed67-114">Para o Windows 2000, pode ser necessário chamar a nova API [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) para garantir que essa janela se torne a janela em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="bed67-114">For Windows 2000, it may be necessary to call the new [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) API to ensure that this window becomes the foreground window.</span></span> <span data-ttu-id="bed67-115">Para obter mais informações sobre como configurar a janela em primeiro plano no Windows 2000, consulte a documentação do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="bed67-115">For more information about setting the foreground window under Windows 2000, see the Platform SDK documentation.</span></span>

 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="bed67-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="bed67-116">See Also</span></span>

[<span data-ttu-id="bed67-117">**IAgentNotifySinkEx::D efaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="bed67-117">**IAgentNotifySinkEx::DefaultCharacterChange**</span></span>](iagentnotifysinkex--defaultcharacterchange.md)


 

 