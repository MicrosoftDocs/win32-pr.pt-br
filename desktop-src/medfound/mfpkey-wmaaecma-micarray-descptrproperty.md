---
description: Especifica a geometria da matriz do microfone para o DSP de captura de voz.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: Propriedade MFPKEY_WMAAECMA_MICARRAY_DESCPTR (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813266"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a>\_Propriedade MFPKEY WMAAECMA \_ MICARRAY \_ DESCPTR

Especifica a geometria da matriz do microfone para o DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_blob VT

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O valor dessa propriedade é uma estrutura [**de \_ \_ \_ geometria da matriz do MIC KSAUDIO**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) . Essa estrutura é definida no arquivo de cabeçalho KsMedia. h. Para obter a geometria da matriz do microfone, consulte o dispositivo de áudio para obter a \_ propriedade de geometria da matriz do MIC de áudio KSPROPERTY \_ \_ \_ chamando o método **IKsControl:: KSPROPERTY** no dispositivo. Para obter mais informações sobre matrizes de microfone, baixe o white paper [como criar e usar matrizes de microfone para o Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

Defina essa propriedade se você estiver usando o DSP no modo de filtro e o processamento da matriz de microfone estiver habilitado. Se você estiver usando o DSP no modo de origem, o DSP consultará automaticamente o dispositivo para obter as informações de geometria.

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

 

 
