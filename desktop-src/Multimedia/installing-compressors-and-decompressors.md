---
title: Instalando os compactadores e os descompactadores
description: Instalando os compactadores e os descompactadores
ms.assetid: 8bcca000-c4c7-47e7-a4c0-5d0d1750176f
keywords:
- VCM (Gerenciador de compactação de vídeo), instalando os compactadores
- VCM (Gerenciador de compactação de vídeo), instalando os compactadores
- Função ICInstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8c3421b3d7f59e7f6b16150fcd0d641deaef17
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292008"
---
# <a name="installing-compressors-and-decompressors"></a>Instalando os compactadores e os descompactadores

O exemplo a seguir mostra como um aplicativo pode instalar uma função como um compactador ou descompactador usando a função [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) .


```C++
// This function looks like a DriverProc entry point. 

LRESULT MyCodecFunction(DWORD dwID, HDRVR hDriver, 
    UINT uiMessage, LPARAM lParam1, LPARAM lParam2); 
 
// This function installs the MyCodecFunction as a compressor. 

result = ICInstall ( ICTYPE_VIDEO, mmioFOURCC('s','a','m','p'), 
    (LPARAM)(FARPROC)&MyCodecFunction, NULL, ICINSTALL_FUNCTION); 
 
```



 

 




