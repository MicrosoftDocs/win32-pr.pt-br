---
title: IAgentPropertySheet GetSize
description: IAgentPropertySheet GetSize
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5e185a6e8d55d87e561f727c8dc9df8a8cfd63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789292"
---
# <a name="iagentpropertysheetgetsize"></a><span data-ttu-id="4ffb9-103">IAgentPropertySheet::GetSize</span><span class="sxs-lookup"><span data-stu-id="4ffb9-103">IAgentPropertySheet::GetSize</span></span>

<span data-ttu-id="4ffb9-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4ffb9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

<span data-ttu-id="4ffb9-105">Recupera o tamanho da janela da folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4ffb9-105">Retrieves the size of the Microsoft Agent property sheet window.</span></span>

-   <span data-ttu-id="4ffb9-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4ffb9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4ffb9-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="4ffb9-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="4ffb9-108">Endereço de uma variável que recebe a largura da folha de propriedades em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="4ffb9-108">Address of a variable that receives the width of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="4ffb9-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="4ffb9-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="4ffb9-110">Endereço de uma variável que recebe a altura da folha de propriedades em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="4ffb9-110">Address of a variable that receives the height of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="4ffb9-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4ffb9-111">See Also</span></span>

[<span data-ttu-id="4ffb9-112">**IAgentPropertySheet:: GetPosition**</span><span class="sxs-lookup"><span data-stu-id="4ffb9-112">**IAgentPropertySheet::GetPosition**</span></span>](iagentpropertysheet--getposition.md)


 

 




