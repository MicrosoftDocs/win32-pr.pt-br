---
title: IAgentCommandWindow setVisible
description: IAgentCommandWindow setVisible
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ddff54f4869cbe36016f30d775eeea017ae6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005714"
---
# <a name="iagentcommandwindowsetvisible"></a><span data-ttu-id="0679c-103">IAgentCommandWindow:: setVisible</span><span class="sxs-lookup"><span data-stu-id="0679c-103">IAgentCommandWindow::SetVisible</span></span>

<span data-ttu-id="0679c-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0679c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

<span data-ttu-id="0679c-105">Defina a propriedade [**Visible**](visible-property.md) para a janela de comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="0679c-105">Set the [**Visible**](visible-property.md) property for the Voice Commands Window.</span></span>

-   <span data-ttu-id="0679c-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0679c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0679c-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="0679c-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="0679c-108">Configuração da propriedade [**visível**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="0679c-108">[**Visible**](visible-property.md) property setting.</span></span> <span data-ttu-id="0679c-109">Um valor **true** exibe a janela de comandos de voz; **False** oculta-o.</span><span class="sxs-lookup"><span data-stu-id="0679c-109">A value of **True** displays the Voice Commands Window; **False** hides it.</span></span>

</dd> </dl>

<span data-ttu-id="0679c-110">O usuário pode substituir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="0679c-110">The user can override this property.</span></span>

## <a name="see-also"></a><span data-ttu-id="0679c-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0679c-111">See Also</span></span>

[<span data-ttu-id="0679c-112">**IAgentCommandWindow:: getVisible**</span><span class="sxs-lookup"><span data-stu-id="0679c-112">**IAgentCommandWindow::GetVisible**</span></span>](iagentcommandwindow--getvisible.md)


 

 




