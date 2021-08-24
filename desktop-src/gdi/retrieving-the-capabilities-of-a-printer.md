---
description: Nem todo dispositivo de saída dá suporte a todo o conjunto de funções gráficas.
ms.assetid: 7989d393-7be4-47fc-af8d-26dd549c48be
title: Recuperando os recursos de uma impressora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c332832efc62f28ee77a5476ef12f706eb2e97a2cd5e86877e4a71a48feb907
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779056"
---
# <a name="retrieving-the-capabilities-of-a-printer"></a>Recuperando os recursos de uma impressora

Nem todo dispositivo de saída dá suporte a todo o conjunto de funções gráficas. Por exemplo, devido a limitações de hardware, a maioria das plotadoras de vetor não oferece suporte a transferências de bloco de bits. Um aplicativo pode determinar se um dispositivo dá suporte a uma função gráfica específica chamando a função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , especificando o índice apropriado e examinando o valor de retorno.

O exemplo a seguir mostra como um aplicativo testa uma impressora para determinar se ela oferece suporte a transferências de bloco de bits.


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



 

 



