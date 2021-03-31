---
description: Especifica quantos buffers o alocador de vídeo do exemplo cria para cada amostra de vídeo.
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: Atributo MF_SA_BUFFERS_PER_SAMPLE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d658ae72c53d986b364b2b6a3f405ae0052ea3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647568"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a>\_Buffers de SA de MF \_ \_ por \_ atributo de exemplo

Especifica quantos buffers o alocador de vídeo do exemplo cria para cada amostra de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Se você usar a interface [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) para alocar amostras de vídeo, poderá usar esse atributo para criar amostras de vídeo que contenham vários buffers. Por exemplo, se o valor do atributo for 2, o alocador criará dois buffers de vídeo para cada amostra de vídeo. Defina o atributo no parâmetro *pAttributes* do método [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .

O valor padrão é 1. Se o atributo não estiver definido, o alocador criará amostras de vídeo que contenham um único buffer por amostra.

Esse atributo destina-se principalmente a transformações de Media Foundation (MFTs) que dão suporte à saída 3D estéreo, na seguinte situação:

-   A MFT dá suporte à Microsoft DirectX Graphics Infrastructure (DXGI).
-   O MFT aloca seus próprios exemplos de saída.
-   O MFT usa a interface [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) para alocar os exemplos de saída.
-   O formato de vídeo 3D usa um buffer separado para cada exibição.

Se todos esses critérios forem verdadeiros, o MFT deverá definir o valor do atributo como 2 (um buffer por exibição).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




