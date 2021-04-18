---
description: Exemplo de AudioDelay de MFT \_
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: Exemplo de MFT_AudioDelay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d382ce7d1c5e9475bef85f11ef9754345e123b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753050"
---
# <a name="mft_audiodelay-sample"></a>Exemplo de AudioDelay de MFT \_

Mostra como implementar um efeito de áudio como uma Media Foundation transformação (MFT). A MFT de atraso de áudio aceita áudio PCM como entrada, aplica um efeito de atraso (eco) e gera os dados de áudio modificados.

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes interfaces de Microsoft Media Foundation:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Uso

O \_ exemplo AudioDelay de MFT cria uma DLL que é um servidor com para o MFT. Antes de usar o MFT, você deve registrar a DLL. Você pode usar a ferramenta TopoEdit para criar uma topologia que inclui a MFT de atraso de áudio. Para obter mais informações sobre TopoEdit, consulte [TopoEdit](topoedit.md). Você também pode modificar o [exemplo PlaybackFX](/previous-versions//bb970336(v=vs.85)) para usar o MFT. Será necessário modificar a função AddBranchToPartialTopology no Player. cpp. Altere a seguinte linha de:

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

Para:

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

O valor CLSID \_ DelayMFT é declarado no arquivo de cabeçalho AudioDelayUuids. h na pasta de \_ exemplo MFT AudioDelay.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[Exemplo de escala de cinza da MFT \_](mft-grayscale-sample.md)
</dt> <dt>

[Gravando uma MFT personalizada](writing-a-custom-mft.md)
</dt> </dl>

 

 
