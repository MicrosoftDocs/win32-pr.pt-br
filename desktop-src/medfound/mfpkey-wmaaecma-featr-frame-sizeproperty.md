---
description: Especifica o tamanho do quadro de áudio usado pelo DSP de captura de voz.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: Propriedade MFPKEY_WMAAECMA_FEATR_FRAME_SIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5623cf3d26b968c7e7745fa0c01c69c034505cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761211"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a>\_ \_ \_ Propriedade tamanho do quadro do MFPKEY WMAAECMA \_

Especifica o tamanho do quadro de áudio usado pelo DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O algoritmo AEC (cancelamento de eco acústico) processa amostras de áudio PCM um quadro por vez. O valor dessa propriedade é o tamanho do quadro de áudio, em exemplos. Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.

O DSP de captura de voz dá suporte aos seguintes tamanhos de quadro:

-   80
-   128
-   160
-   240
-   256
-   320

Se o valor dessa propriedade for zero, o DSP selecionará o tamanho do quadro com base no modo do sistema e no formato de saída.

No entanto, para obter o melhor desempenho, é recomendável que os aplicativos usem o valor padrão. Se o modo de processamento for somente matriz de microfone, o valor padrão será 320 exemplos. Para todos os outros modos de processamento, o valor padrão é 160 exemplos. Para obter mais informações sobre os modos de processamento do DSP de captura de voz, consulte [MFPKEY \_ WMAAECMA \_ System \_ Mode](mfpkey-wmaaecma-system-modeproperty.md).

Após a primeira chamada para [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) ou [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), você pode ler essa propriedade para obter o tamanho real do quadro em uso, mesmo quando o [**\_ modo de \_ recurso \_ MFPKEY WMAAECMA**](mfpkey-wmaaecma-feature-modeproperty.md) for false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
