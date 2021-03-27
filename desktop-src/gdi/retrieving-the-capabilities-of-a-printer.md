---
description: Nem todo dispositivo de saída dá suporte a todo o conjunto de funções gráficas.
ms.assetid: 7989d393-7be4-47fc-af8d-26dd549c48be
title: Recuperando os recursos de uma impressora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d84db8d46255f4dfd33ce62ab4ab6735b0f2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967587"
---
# <a name="retrieving-the-capabilities-of-a-printer"></a><span data-ttu-id="a6072-103">Recuperando os recursos de uma impressora</span><span class="sxs-lookup"><span data-stu-id="a6072-103">Retrieving the Capabilities of a Printer</span></span>

<span data-ttu-id="a6072-104">Nem todo dispositivo de saída dá suporte a todo o conjunto de funções gráficas.</span><span class="sxs-lookup"><span data-stu-id="a6072-104">Not every output device supports the entire set of graphics functions.</span></span> <span data-ttu-id="a6072-105">Por exemplo, devido a limitações de hardware, a maioria das plotadoras de vetor não oferece suporte a transferências de bloco de bits.</span><span class="sxs-lookup"><span data-stu-id="a6072-105">For example, because of hardware limitations, most vector plotters do not support bit-block transfers.</span></span> <span data-ttu-id="a6072-106">Um aplicativo pode determinar se um dispositivo dá suporte a uma função gráfica específica chamando a função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , especificando o índice apropriado e examinando o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a6072-106">An application can determine whether a device supports a particular graphics function by calling the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function, specifying the appropriate index, and examining the return value.</span></span>

<span data-ttu-id="a6072-107">O exemplo a seguir mostra como um aplicativo testa uma impressora para determinar se ela oferece suporte a transferências de bloco de bits.</span><span class="sxs-lookup"><span data-stu-id="a6072-107">The following example shows how an application tests a printer to determine whether it supports bit-block transfers.</span></span>


```C++
// Examine the raster capabilities of the device  
// identified by hdcPrint to verify that it supports  
// the BitBlt function.  
 
if ((GetDeviceCaps(hdcPrint, RASTERCAPS) 
       & RC_BITBLT) == 0) 
{ 
   DeleteDC(hdcPrint); 
   break; 
} 

else 
{ 
    // Print the bitmap using the printer DC.  
}
```



 

 



