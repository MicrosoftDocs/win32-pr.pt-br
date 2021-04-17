---
description: Especifica o tipo de detecção de atividade de voz que o DSP de captura de voz executa.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: Propriedade MFPKEY_WMAAECMA_FEATR_VAD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e41b8ad80d909a0285b266587d02c09c08d794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782441"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a>\_ \_ \_ Propriedade VAD do MFPKEY WMAAECMA

Especifica o tipo de detecção de atividade de voz que o DSP de captura de voz executa.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O valor dessa propriedade é um membro da enumeração do [ \_ \_ modo de VAD do AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) . A saída da detecção de atividade de voz é um número de 0 a 3, calculada para cada quadro de áudio. O DSP codifica o resultado no menor bit dos primeiros dois exemplos de áudio em cada quadro de áudio. O significado do valor depende do modo especificado.

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



O valor padrão dessa propriedade é 0 (desabilitado). Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
