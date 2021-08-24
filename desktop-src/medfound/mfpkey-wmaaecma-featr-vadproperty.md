---
description: Especifica o tipo de detecção de atividade de voz que o DSP de Captura de Voz executa.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: MFPKEY_WMAAECMA_FEATR_VAD propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17e23662a8c6966a64140311f24c9af00dc53454cea19c025451698ddbbbd0dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953506"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a>Propriedade \_ VAD MFPKEY WMAAECMACALR \_ \_

Especifica o tipo de detecção de atividade de voz que o DSP de Captura de Voz executa.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="default-value"></a>Valor padrão

0

## <a name="applies-to"></a>Aplica-se A

-   [DSP de Captura de Voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O valor dessa propriedade é um membro da enumeração [ \_ AEC VAD \_ MODE.](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) A saída da detecção de atividade de voz é um número de 0 a 3, calculado para cada quadro de áudio. O DSP codifica o resultado no bit mais baixo dos dois primeiros exemplos de áudio em cada quadro de áudio. O significado do valor depende do modo especificado.

O código a seguir mostra como extrair os resultados dos dados de áudio. Neste exemplo, *pOutput* é um ponteiro para o início de um quadro de áudio nos dados de saída.


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



O valor padrão dessa propriedade é 0 (desabilitado). Antes de definir essa propriedade, você deve definir a [propriedade \_ MFPKEY WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) como VARIANT \_ TRUE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
