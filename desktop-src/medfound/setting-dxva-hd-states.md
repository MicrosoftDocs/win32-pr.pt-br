---
description: Definindo Estados de DXVA-HD
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Definindo Estados de DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91766e3eb10399d908ab361e13db4b94fe07b653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092694"
---
# <a name="setting-dxva-hd-states"></a>Definindo Estados de DXVA-HD

Durante o processamento de vídeo, o dispositivo de alta definição (DXVA-HD) de aceleração de vídeo do Microsoft DirectX mantém um estado persistente de um quadro para o outro. Cada Estado tem um padrão documentado. Depois de configurar o dispositivo, defina os Estados que você deseja alterar de seus padrões. Antes de processar cada quadro, atualize todos os Estados que devem ser alterados.

> [!Note]  
> Esse design difere do DXVA-VP. No DXVA-VP, o aplicativo deve especificar todos os parâmetros de VP com cada quadro.

 

Os Estados do dispositivo se enquadram em duas categorias:

-   Os Estados de *fluxo* aplicam cada fluxo de entrada separadamente. Você pode aplicar configurações diferentes a cada fluxo.
-   Os Estados *blit* se aplicam globalmente a todo o blit de processamento de vídeo.

Os Estados de fluxo a seguir são definidos.



| Estado do fluxo                                   | Descrição                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **DXVAHD \_ de \_ estado de fluxo \_ D3DFORMAT**           | Formato de vídeo de entrada.                                                                                             |
| **\_formato de \_ quadro de estado de fluxo DXVAHD \_ \_**       | Entrelaça.                                                                                                    |
| **\_espaço de \_ cor de entrada de estado de fluxo DXVAHD \_ \_ \_** | Espaço de cores de entrada. Esse estado especifica o intervalo de cores RGB e a matriz de transferência YCbCr para o fluxo de entrada. |
| **\_taxa de \_ saída de estado de fluxo DXVAHD \_ \_**        | Taxa de quadros de saída. Esse estado controla a conversão de taxa de quadros.                                                   |
| **\_Rect de \_ origem de estado de fluxo DXVAHD \_ \_**        | Retângulo de origem.                                                                                               |
| **\_Rect de \_ destino de estado de fluxo DXVAHD \_ \_**   | Retângulo de destino.                                                                                          |
| **DXVAHD \_ de \_ estado de fluxo \_ alfa**               | Planar alfa.                                                                                                   |
| **\_paleta de \_ Estados de fluxo DXVAHD \_**             | Paleta de cores. Esse Estado se aplica somente aos formatos de entrada palettized.                                             |
| **\_chave de \_ Luma de estado de fluxo DXVAHD \_ \_**           | Chave Luma.                                                                                                       |
| **\_taxa de \_ proporção do estado de fluxo DXVAHD \_ \_**       | Taxa de proporção de pixel.                                                                                             |
| **Filtro de estado de fluxo de DXVAHD \_ \_ \_ \_ xxxx**        | Configurações de filtro de imagem. O driver pode dar suporte a brilho, contraste e outros filtros de imagem.                    |



 

Os seguintes Estados de blit são definidos:



| Estado blit                                   | Descrição                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| **\_ \_ \_ target Rect de estado DXVAHD BLT \_**         | Retângulo de destino.                                                            |
| **\_cor do \_ plano de fundo do estado DXVAHD BLT \_ \_**    | Cor do plano de fundo.                                                            |
| **\_espaço de \_ cor de saída de estado DXVAHD BLT \_ \_ \_** | Espaço de cores de saída.                                                          |
| **\_ \_ preenchimento alfa do estado DXVAHD BLT \_ \_**          | Modo de preenchimento alfa.                                                             |
| **\_restrição de \_ estado de BLT DXVAHD \_**         | Restrição. Esse estado controla se o dispositivo downsamples a saída. |



 

Para definir um estado de fluxo, chame o método [**IDXVAHD \_ VideoProcessor:: SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) . Para definir um estado blit, chame o método [**IDXVAHD \_ VideoProcessor:: SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) . Em ambos os métodos, um valor de enumeração Especifica o estado a ser definido. Os dados de estado são fornecidos usando uma estrutura de dados específica de estado, que o aplicativo converte para um tipo **void \*** .

O exemplo de código a seguir define o formato de entrada e o retângulo de destino para o fluxo 0 e define a cor do plano de fundo como preto.


```C++
HRESULT SetDXVAHDStates(HWND hwnd, D3DFORMAT inputFormat)
{
    // Set the initial stream states.

    // Set the format of the input stream

    DXVAHD_STREAM_STATE_D3DFORMAT_DATA d3dformat = { inputFormat };

    HRESULT hr = g_pDXVAVP->SetVideoProcessStreamState(
        0,  // Stream index
        DXVAHD_STREAM_STATE_D3DFORMAT,
        sizeof(d3dformat),
        &d3dformat
        );

    if (SUCCEEDED(hr))
    { 
        // For this example, the input stream contains progressive frames.

        DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { DXVAHD_FRAME_FORMAT_PROGRESSIVE };
        
        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index
            DXVAHD_STREAM_STATE_FRAME_FORMAT,
            sizeof(frame_format),
            &frame_format
            );
    }

    if (SUCCEEDED(hr))
    { 
        // Compute the letterbox area.

        RECT rcDest;
        GetClientRect(hwnd, &rcDest);

        RECT rcSrc;
        SetRect(&rcSrc, 0, 0, VIDEO_WIDTH, VIDEO_HEIGHT);

        rcDest = LetterBoxRect(rcSrc, rcDest);

        // Set the destination rectangle, so the frame is displayed within the 
        // letterbox area. Otherwise, the frame is stretched to cover the 
        // entire surface.

        DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA DstRect = { TRUE, rcDest };

        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index 
            DXVAHD_STREAM_STATE_DESTINATION_RECT,
            sizeof(DstRect),
            &DstRect
            );
    }

    if (SUCCEEDED(hr))
    { 
        DXVAHD_COLOR_RGBA rgbBackground = { 0.0f, 0.0f, 0.0f, 1.0f };  // RGBA

        DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA background = { FALSE, rgbBackground };

        hr = g_pDXVAVP->SetVideoProcessBltState(
            DXVAHD_BLT_STATE_BACKGROUND_COLOR,
            sizeof (background),
            &background
            );
    }

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



