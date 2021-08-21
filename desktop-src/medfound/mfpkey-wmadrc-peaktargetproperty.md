---
description: Especifica o nível máximo de volume desejado do conteúdo de áudio de saída.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: MFPKEY_WMADRC_PEAKTARGET propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79f54d15978bb3f6a34c015886d2aeb2a8ec48a0069669e81ea40bbd79353902
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973225"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a>Propriedade MFPKEY \_ WMADRC \_ PEAKTARGET

Especifica o nível máximo de volume desejado do conteúdo de áudio de saída.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMADRCPeakTarget

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="default-value"></a>Valor padrão

Consulte Observações.

## <a name="remarks"></a>Comentários

Você pode definir esse valor no decodificador para fins de controle de intervalo dinâmico, mas ele terá um efeito somente se a propriedade [ \_ \_ DRCMODE MFPKEY WCODEC](mfpkey-wmadec-drcmodeproperty.md) estiver definida.

Se você solicitar o controle de intervalo dinâmico do decodificador quando essa propriedade não estiver definida, o codec calculará um valor padrão.

Use as [propriedades MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) e [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) para calcular os valores apropriados para essa propriedade.

Para obter mais informações sobre o controle de intervalo dinâmico, consulte o artigo da [Web Windows De áudio de Professional recursos do Codec](/previous-versions/ms867218(v=msdn.10)).

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

 

 
