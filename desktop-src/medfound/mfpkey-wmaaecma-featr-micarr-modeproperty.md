---
description: Especifica como o DSP de Captura de Voz executa o processamento de matriz de microfone.
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: MFPKEY_WMAAECMA_FEATR_MICARR_MODE propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb948ff15655ccbdc0bf647194b2f6d3d7d1a40c36da32f6d65479152c76c3e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953516"
---
# <a name="mfpkey_wmaaecma_featr_micarr_mode-property"></a>Propriedade MFPKEY \_ WMAAECMA \_ \_ MICARR \_ MODE

Especifica como o DSP de Captura de Voz executa o processamento de matriz de microfone.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="default-value"></a>Valor padrão

MICARRAY \_ SINGLE \_ BEAM

## <a name="applies-to"></a>Aplica-se A

-   [DSP de Captura de Voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O valor dessa propriedade é um membro da [enumeração MIC \_ ARRAY \_ MODE.](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) O valor padrão é MICARRAY \_ SINGLE \_ BEAM. Antes de definir essa propriedade, você deve definir a [propriedade \_ MFPKEY WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) como VARIANT \_ TRUE.

O DSP usa essa propriedade somente quando o processamento da matriz de microfone está habilitado.

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

 

 
