---
description: Formatos de arquivo personalizados
ms.assetid: 4dc77cfa-0cab-4055-9e11-f036e2d1dcca
title: Formatos de arquivo personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a478e7818701008c31d1d0c5a6e4924540ed818be19f7b50fe3ed278aa6f3ba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998686"
---
# <a name="custom-file-formats"></a>Formatos de arquivo personalizados

Se você tiver um filtro personalizado mux ou de file-writer que dá suporte ao seu próprio formato de arquivo, poderá especificar o CLSID como o primeiro parâmetro do método [**ICaptureGraphBuilder2::SetOutputFileName:**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename)


```C++
IBaseFilter *pMux = 0;
IFileSinkFilter *pSink = 0;
hr = pBuild->SetOutputFileName(&CLSID_MyCustomMuxFilter, 
    L"C:\\VidCap.avi", &pMux, &pSink);
```



Para obter mais informações sobre esse uso, consulte [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturando vídeo em um arquivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



