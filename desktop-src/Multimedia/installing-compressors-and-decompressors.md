---
title: Instalando os descompactores e os descompactores
description: Instalando os descompactores e os descompactores
ms.assetid: 8bcca000-c4c7-47e7-a4c0-5d0d1750176f
keywords:
- VCM (gerenciador de compactação de vídeo), instalando os vcms
- VCM (gerenciador de compactação de vídeo), instalando os vcs
- Função ICInstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27a9bacc946a17bf4d70260cb077a7e3f17fe85760837cc7086144297f1f86c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140532"
---
# <a name="installing-compressors-and-decompressors"></a>Instalando os descompactores e os descompactores

O exemplo a seguir mostra como um aplicativo pode instalar uma função como um descompactador ou um descompactador usando a [**função ICInstall.**](/windows/desktop/api/Vfw/nf-vfw-icinstall)


```C++
// This function looks like a DriverProc entry point. 

LRESULT MyCodecFunction(DWORD dwID, HDRVR hDriver, 
    UINT uiMessage, LPARAM lParam1, LPARAM lParam2); 
 
// This function installs the MyCodecFunction as a compressor. 

result = ICInstall ( ICTYPE_VIDEO, mmioFOURCC('s','a','m','p'), 
    (LPARAM)(FARPROC)&MyCodecFunction, NULL, ICINSTALL_FUNCTION); 
 
```



 

 




