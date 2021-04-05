---
title: Determinando se um driver pode manipular o formato de entrada
description: Determinando se um driver pode manipular o formato de entrada
ms.assetid: 456eab43-d830-4a28-b724-3ef35b852372
keywords:
- VCM (Gerenciador de compactação de vídeo), formato de entrada
- VCM (Gerenciador de compactação de vídeo), formato de entrada
- Macro ICDrawQuery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b3e2da69f8c061a7d0aefe847f40113d5104d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005501"
---
# <a name="determining-if-a-driver-can-handle-the-input-format"></a>Determinando se um driver pode manipular o formato de entrada

O exemplo a seguir mostra como verificar o formato de entrada com a macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .


```C++
// lpbiIn points to BITMAPINFOHEADER structure indicating the input 
// format. 

if (ICDrawQuery(hIC, lpbiIn) == ICERR_OK) 
{ 
    // Driver recognizes the input format. 
} 
else 
{ 
    // Need a different decompressor. 
} 
 
```



 

 




