---
title: Obtendo informações sobre compactadores e descompactadores
description: Obtendo informações sobre compactadores e descompactadores
ms.assetid: 2f1edfd0-dd30-42ea-a5ae-24265d3f8af3
keywords:
- VCM (Gerenciador de compactação de vídeo), obtendo informações sobre os compactadores
- VCM (Gerenciador de compactação de vídeo), obtendo informações sobre os compactadores
- Função ICGetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874793233ef0aec4de5b372573fb8dcd79f5d875
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363781"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a>Obtendo informações sobre compactadores e descompactadores

O exemplo a seguir usa a função [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) para obter informações sobre um compactador ou descompactador.


```C++
ICINFO ICInfo; 
ICGetInfo(hIC, &ICInfo, sizeof(ICInfo)); 
 
```



O exemplo a seguir usa as macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) e [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) para obter os valores padrão.


```C++
DWORD dwKeyFrameRate, dwQuality; 
dwKeyFrameRate = ICGetDefaultKeyFrameRate(hIC); 
dwQuality = ICGetDefaultQuality(hIC); 
 
```



O exemplo a seguir usa as macros [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) e [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) para exibir uma caixa de diálogo about para o compressor ou o descompactador, se a caixa de diálogo existir.


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




