---
title: Configurando fluxos de captura de tela
description: Configurando fluxos de captura de tela
ms.assetid: 974e679f-0bf6-412b-9e80-43370de7605a
keywords:
- fluxos, configurando fluxos de captura de tela
- codecs, configurando fluxos de captura de tela
- fluxos de captura de tela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8200c4a6e733c2bb7f908b79cb73dbb2c3244dc4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916968"
---
# <a name="configuring-screen-capture-streams"></a>Configurando fluxos de captura de tela

Os fluxos que usam o codec de tela vídeo 9 do Windows Media® são configurados por aplicativos da mesma maneira que os fluxos de vídeo normais. No entanto, se você definir o nível de complexidade do vídeo como 0, o gravador irá ignorar qualquer conjunto de valores de qualidade de vídeo com [**IWMVideoMediaProps:: setquality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality). Para obter mais informações, consulte [obtendo bons resultados com o codec de tela do Windows Media Video 9](getting-good-results-with-the-windows-media-video-9-screen-codec.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurando fluxos**](configuring-streams.md)
</dt> <dt>

[**Configuração comum a todos os fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurando fluxos de vídeo**](configuring-video-streams.md)
</dt> </dl>

 

 




