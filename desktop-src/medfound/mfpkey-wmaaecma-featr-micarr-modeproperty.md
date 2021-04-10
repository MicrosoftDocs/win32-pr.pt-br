---
description: Especifica como o DSP de captura de voz executa o processamento de matriz de microfone.
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: Propriedade MFPKEY_WMAAECMA_FEATR_MICARR_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf8ffcae465e8abfddedb3e6d6dded683bb2bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164924"
---
# <a name="mfpkey_wmaaecma_featr_micarr_mode-property"></a>\_Propriedade do \_ \_ \_ modo MICARR do MFPKEY WMAAECMA

Especifica como o DSP de captura de voz executa o processamento de matriz de microfone.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

MICARRAY \_ \_ feixe único

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O valor dessa propriedade é um membro da enumeração do [ \_ \_ modo de matriz MIC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) . O valor padrão é MICARRAY \_ Single \_ feixe. Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.

O DSP usa essa propriedade somente quando o processamento da matriz de microfone está habilitado.

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

 

 
