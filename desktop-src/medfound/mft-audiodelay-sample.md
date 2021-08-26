---
description: Exemplo de AudioDelay do MFT \_
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: MFT_AudioDelay exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4af3d89c7dda4a67a2fece09ff9e6d3bc0a63927e94b259df40334fd9ba29b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012666"
---
# <a name="mft_audiodelay-sample"></a>Exemplo de AudioDelay do MFT \_

Mostra como implementar um efeito de áudio como uma transformação Media Foundation (MFT). O MFT de atraso de áudio aceita áudio PCM como entrada, aplica um efeito de atraso (eco) e saída dos dados de áudio modificados.

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes Microsoft Media Foundation interfaces:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Uso

O exemplo \_ de MFT AudioDelay cria uma DLL que é um servidor COM para o MFT. Antes de usar o MFT, você deve registrar a DLL. Você pode usar a ferramenta TopoEdit para criar uma topologia que inclui o atraso de áudio MFT. Para obter mais informações sobre TopEdit, consulte [TopoEdit](topoedit.md). Você também pode modificar o [Exemplo de PlaybackFX](/previous-versions//bb970336(v=vs.85)) para usar o MFT. Você precisará modificar a função AddBranchToPartialTopology em Player.cpp. Altere a seguinte linha de:

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

O valor DELAYMFT do CLSID é declarado no arquivo \_ de header AudioDelayUuids.h na pasta de exemplo MFT \_ AudioDelay.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível no repositório [Windows github de exemplos clássicos.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Media Foundation transformação](media-foundation-transforms.md)
</dt> <dt>

[Exemplo de \_ escala de cinza MFT](mft-grayscale-sample.md)
</dt> <dt>

[Escrevendo um MFT personalizado](writing-a-custom-mft.md)
</dt> </dl>

 

 
