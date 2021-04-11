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
# <a name="obtaining-information-about-compressors-and-decompressors"></a><span data-ttu-id="b2e33-106">Obtendo informações sobre compactadores e descompactadores</span><span class="sxs-lookup"><span data-stu-id="b2e33-106">Obtaining Information About Compressors and Decompressors</span></span>

<span data-ttu-id="b2e33-107">O exemplo a seguir usa a função [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) para obter informações sobre um compactador ou descompactador.</span><span class="sxs-lookup"><span data-stu-id="b2e33-107">The following example uses the [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) function to obtain information about a compressor or decompressor.</span></span>


```C++
ICINFO ICInfo; 
ICGetInfo(hIC, &ICInfo, sizeof(ICInfo)); 
 
```



<span data-ttu-id="b2e33-108">O exemplo a seguir usa as macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) e [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) para obter os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="b2e33-108">The following example uses the [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) and [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macros to obtain the default values.</span></span>


```C++
DWORD dwKeyFrameRate, dwQuality; 
dwKeyFrameRate = ICGetDefaultKeyFrameRate(hIC); 
dwQuality = ICGetDefaultQuality(hIC); 
 
```



<span data-ttu-id="b2e33-109">O exemplo a seguir usa as macros [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) e [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) para exibir uma caixa de diálogo about para o compressor ou o descompactador, se a caixa de diálogo existir.</span><span class="sxs-lookup"><span data-stu-id="b2e33-109">The following example uses the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) and [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macros to display an About dialog box for the compressor or decompressor, if the dialog box exists.</span></span>


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




