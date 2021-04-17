---
description: O MFT de estabilização de vídeo é uma Microsoft Media Foundation transformação (MFT) que executa a estabilização de imagem em um fluxo de vídeo.
ms.assetid: BBC42190-08E4-4C3B-972A-FD30621A6CC1
title: MFT Estabilização de Vídeo (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65eb64b05e41842b1f7b3ad2e49a6c064be08f0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769366"
---
# <a name="video-stabilization-mft"></a>Estabilização de Vídeo MFT

O MFT de estabilização de vídeo é uma Microsoft Media Foundation transformação (MFT) que executa a estabilização de imagem em um fluxo de vídeo.

## <a name="clsid"></a>CLSID

\_CMSVIDEODSPMFT CLSID

## <a name="interfaces"></a>Interfaces

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMediaExtension**](/uwp/api/Windows.Media.IMediaExtension?view=winrt-19041)

## <a name="input-formats"></a>Formatos de entrada

As combinações de tipo de mídia de entrada e subtipo aceitas pelo MFT de estabilização de vídeo para vídeo descompactado são:

-   **vídeo de MEDIATYPE \_**
-   **MEDIASUBTYPE \_ NV12**
-   **MEDIASUBTYPE \_ YUY2**

## <a name="output-formats"></a>Formatos de saída

As combinações de tipo e subtipo de mídia de saída aceitas pelo MFT de estabilização de vídeo são:

-   **vídeo de MEDIATYPE \_**
-   **MEDIASUBTYPE \_ NV12**

O tipo de mídia de entrada deve ser definido antes do tipo de mídia de saída. Na maioria das situações, o suporte a formato limitado não é um problema porque o pipeline insere automaticamente as conversões de cor necessárias.

O componente MFT de estabilização de vídeo é capaz de alterar o formato dinâmico quando a entrada é alterada. Quando o tamanho da imagem de entrada for alterado ou o subtipo for alterado, ele irá disparar uma alteração de formato dinâmico no fluxo de saída.

A MFT de estabilização de vídeo fará a conversão de cores nos seguintes casos:

-   Quando o formato de entrada é **MEDIASUBTYPE \_ YUY2**.
-   Quando o modo de compatibilidade do Microsoft DirectX 9,0 é usado.

### <a name="attributes"></a>Atributos

Os atributos a seguir têm suporte pelo MFT de estabilização de vídeo por meio da interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

-   O [modo MF \_ VIDEODSP \_ ](mf-videodsp-mode.md) do atributo coloca a MFT de estabilização de vídeo no modo de estabilização ou no modo de passagem. O aplicativo deve chamar [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) no **\_ \_ tipo VIDEODSP** do GUID MF com um inteiro correspondente a um dos seguintes valores válidos: **MFVideoDSPMode \_ estabilization** = 4, **MFVideoDSPMode \_ PassThrough** = 1. O \_ modo MF VIDEODSP \_ pode ser alterado a qualquer momento durante a reprodução. Isso causa uma alteração no modo dinâmico. A saída mudará para estabilizada ou passará após 16 ou 2 quadros (dependendo do modo de latência) depois que o atributo for alterado.
-   O atributo [MF de \_ baixa \_ LATÊNCIA](mf-low-latency.md) coloca o MFT de estabilização de vídeo no modo de baixa latência ou no modo de alta qualidade. O aplicativo deve chamar [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) na **\_ baixa \_ latência de MF** de GUID com um inteiro correspondente a um dos seguintes valores válidos: baixa latência = 1 alta qualidade = 0
-   O atributo [MF \_ SA \_ D3D11 \_ BINDFLAGS](mf-sa-d3d11-bindflags.md) é usado pelo pipeline para especificar os sinalizadores de associação de D3D11 para criar os exemplos de saída com. Qualquer combinação de valores da enumeração [**\_ \_ sinalizador de associação D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) é válida.
-   A **contagem de \_ \_ amostra de \_ saída \_ \_ mínima do atributo MF SA** é usada pelo pipeline para especificar o número mínimo de amostras para as quais esse componente deve dar suporte na saída.
-   O atributo [MFSampleExtension \_ VideoDSPMode](mfsampleextension-videodspmode.md) é definido em cada exemplo produzido por estabilização para indicar o [ \_ \_ modo de VIDEODSP de MF](mf-videodsp-mode.md) em vigor aplicado a esse exemplo (se a amostra foi estabilizada ou não). Em determinadas condições, os exemplos não podem ser estabilizados (devido à alta carga do sistema ou solicitações pelo usuário). Esse atributo tem os mesmos valores que o \_ atributo de modo MF VIDEODSP \_ (**\_ estabilização de MFVideoDSPMode** e **\_ passagem de MFVideoDSPMode**). Para obter o valor deste atributo, os aplicativos devem chamar [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) no GUID **MFSampleExtension \_ VideoDSPMode**.

## <a name="remarks"></a>Comentários

Uma instância do DSP de estabilização de vídeo pode ser criada de uma das seguintes maneiras:

-   Chamando [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). O DSP de estabilização de vídeo é registrado na categoria de **\_ efeito de \_ vídeo \_ da categoria MFT** .
-   Chamando a função COM **CoCreateInstance** passando-a para o CLSID **CLSID \_ CMSVideoDSPMFT**. Para usar esse método, você deve incluir wmcodecdsp. h e vincular em wmcodecdspuuid. lib.

Além disso, o DSP de estabilização de vídeo dá suporte à instanciação usando Windows Runtime como uma extensão de mídia do Windows. Ele é definido no [**Windows. Media. VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041), e seu nome completo é "Windows. Media. VideoEffects. VideoStabilization".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Camerauicontrol. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Processadores de sinais digitais](windowsmediadigitalsignalprocessors.md)
</dt> <dt>

[**Windows.Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)
</dt> </dl>

 

 
