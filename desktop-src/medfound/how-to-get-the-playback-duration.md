---
description: Este tópico descreve como obter a duração da reprodução de um arquivo de mídia usando o MFPlay.
ms.assetid: b1ea4f21-55d1-47b0-b6d3-8951dce79f7c
title: Como obter a duração da reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21dd98a916109c8fb3d0ad3311643b1ffdc0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749955"
---
# <a name="how-to-get-the-playback-duration"></a>Como obter a duração da reprodução

\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. \]

Este tópico descreve como obter a duração da reprodução de um arquivo de mídia usando o MFPlay.

**Para obter a duração da reprodução**

1.  Chame [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) ou [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) para criar um item de mídia para o arquivo.
2.  Chame [**IMFPMediaItem:: getDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration). Especifique **o \_ PositionType do MFP de \_ 100 NS** para o primeiro parâmetro. A duração é retornada como um **PROPVARIANT** que contém um **valor \_ inteiro grande** . A duração é fornecida em unidades de 100 a nanossegundos.

O exemplo a seguir mostra a etapa 2:


```C++
#include <propvarutil.h>

HRESULT GetPlaybackDuration(IMFPMediaItem *pItem, ULONGLONG *phnsDuration)
{
    PROPVARIANT var;

    HRESULT hr = pItem->GetDuration(MFP_POSITIONTYPE_100NS, &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt64(var, phnsDuration);
        PropVariantClear(&var);
    }

    return hr;
}
```



## <a name="requirements"></a>Requisitos

O MFPlay requer o Windows 7.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o MFPlay para reprodução de áudio/vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



