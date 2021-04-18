---
description: Especifica o nível máximo de volume desejado de conteúdo de áudio de saída.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: Propriedade MFPKEY_WMADRC_PEAKTARGET (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c40fa68e2b580c5d3e8550d6e46c9f6b9fe4bfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807222"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a>\_Propriedade MFPKEY WMADRC \_ PEAKTARGET

Especifica o nível máximo de volume desejado de conteúdo de áudio de saída.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMADRCPeakTarget

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

Consulte Observações.

## <a name="remarks"></a>Comentários

Você pode definir esse valor no decodificador para a finalidade do controle de intervalo dinâmico, mas terá efeito somente se a propriedade [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) for definida.

Se você solicitar o controle de intervalo dinâmico do decodificador quando essa propriedade não for definida, o codec calculará um valor padrão.

Use as propriedades [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) e [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) para calcular os valores apropriados para essa propriedade.

Para obter mais informações sobre o controle de intervalo dinâmico, consulte o artigo da Web [recursos de codec do Windows Media Audio Professional](/previous-versions/ms867218(v=msdn.10)).

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

 

 
