---
description: Os dois modos de mapeamento definidos pelo aplicativo (MM \_ ISOTROPIC e mm \_ ANISOTROPIC) são fornecidos para modos de mapeamento específicos do aplicativo.
ms.assetid: c4c4e352-63fc-4e97-a218-a1b7deac02e8
title: Modos de mapeamento de Application-Defined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d800a3ce631ebffeef8223fc53ec505c10cb69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988847"
---
# <a name="application-defined-mapping-modes"></a><span data-ttu-id="399b1-103">Modos de mapeamento de Application-Defined</span><span class="sxs-lookup"><span data-stu-id="399b1-103">Application-Defined Mapping Modes</span></span>

<span data-ttu-id="399b1-104">Os dois modos de mapeamento definidos pelo aplicativo (MM \_ ISOTROPIC e mm \_ ANISOTROPIC) são fornecidos para modos de mapeamento específicos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="399b1-104">The two application-defined mapping modes (MM\_ISOTROPIC and MM\_ANISOTROPIC) are provided for application-specific mapping modes.</span></span> <span data-ttu-id="399b1-105">O \_ modo ISOTROPIC de mm garante que as unidades lógicas na direção x e na direção y sejam iguais, enquanto o \_ modo ANISOTROPIC mm permite que as unidades sejam diferentes.</span><span class="sxs-lookup"><span data-stu-id="399b1-105">The MM\_ISOTROPIC mode guarantees that logical units in the x-direction and in the y-direction are equal, while the MM\_ANISOTROPIC mode allows the units to differ.</span></span> <span data-ttu-id="399b1-106">Um aplicativo CAD ou de desenho pode se beneficiar do \_ modo de mapeamento ISOTROPIC mm, mas pode ser necessário especificar unidades lógicas que correspondam aos incrementos na escala de um engenheiro (1/64 polegadas).</span><span class="sxs-lookup"><span data-stu-id="399b1-106">A CAD or drawing application can benefit from the MM\_ISOTROPIC mapping mode but may need to specify logical units that correspond to the increments on an engineer's scale (1/64 inch).</span></span> <span data-ttu-id="399b1-107">Essas unidades seriam difíceis de obter com os modos de mapeamento predefinidos (MM \_ HIENGLISH ou mm \_ HIMETRIC); no entanto, elas podem ser obtidas facilmente selecionando o \_ modo mm ISOTROPIC (ou mm \_ ANISOTROPIC).</span><span class="sxs-lookup"><span data-stu-id="399b1-107">These units would be difficult to obtain with the predefined mapping modes (MM\_HIENGLISH or MM\_HIMETRIC); however, they can easily be obtained by selecting the MM\_ISOTROPIC (or MM\_ANISOTROPIC) mode.</span></span> <span data-ttu-id="399b1-108">O exemplo a seguir mostra como definir unidades lógicas como 1/64 polegadas:</span><span class="sxs-lookup"><span data-stu-id="399b1-108">The following example shows how to set logical units to 1/64 inch:</span></span>


```C++
SetMapMode(hDC, MM_ISOTROPIC); 
SetWindowExtEx(hDC, 64, 64, NULL); 
SetViewportExtEx(hDC, GetDeviceCaps(hDC, LOGPIXELSX), 
                      GetDeviceCaps(hDC, LOGPIXELSY), NULL); 
```



 

 



