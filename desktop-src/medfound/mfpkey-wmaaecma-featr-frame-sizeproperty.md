---
description: Especifica o tamanho do quadro de áudio usado pelo DSP de Captura de Voz.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: MFPKEY_WMAAECMA_FEATR_FRAME_SIZE propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812a9c7b85a36b730caffe7679cc742a3bc029546a12839afd95a8c8ab58bfeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973285"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a>Propriedade MFPKEY \_ WMAAECMA \_ FRAME \_ \_ SIZE

Especifica o tamanho do quadro de áudio usado pelo DSP de Captura de Voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="default-value"></a>Valor padrão

0

## <a name="applies-to"></a>Aplica-se A

-   [DSP de Captura de Voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O algoritmo AEC (cancelamento de eco acústico) processa amostras de áudio PCM um quadro por vez. O valor dessa propriedade é o tamanho do quadro de áudio, em exemplos. Antes de definir essa propriedade, você deve definir a [propriedade \_ MFPKEY WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) como VARIANT \_ TRUE.

O DSP de Captura de Voz dá suporte aos seguintes tamanhos de quadro:

-   80
-   128
-   160
-   240
-   256
-   320

Se o valor dessa propriedade for zero, o DSP selecionará o tamanho do quadro com base no modo do sistema e no formato de saída.

No entanto, para o melhor desempenho, é recomendável que os aplicativos usem o valor padrão. Se o modo de processamento for somente matriz de microfone, o valor padrão será 320 amostras. Para todos os outros modos de processamento, o valor padrão é 160 amostras. Para obter mais informações sobre os modos de processamento do DSP de Captura de Voz, consulte [MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE](mfpkey-wmaaecma-system-modeproperty.md).

Após a primeira chamada para [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) ou [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), você pode ler essa propriedade para obter o tamanho real do quadro em uso, mesmo quando [**MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE**](mfpkey-wmaaecma-feature-modeproperty.md) for false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[DSP de Captura de Voz](voicecapturedmo.md)
</dt> </dl>

 

 
