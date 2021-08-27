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
ms.openlocfilehash: b023a8f82fa92aa78a2a2dcf47a8f6c9447f943ac0f68440c6d7aff3123fc84e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038436"
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



 

 




