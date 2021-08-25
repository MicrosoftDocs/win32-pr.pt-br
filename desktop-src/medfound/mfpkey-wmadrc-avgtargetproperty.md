---
description: Especifica o nível de volume médio desejado de conteúdo de áudio de saída.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: Propriedade MFPKEY_WMADRC_AVGTARGET (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1cdd3143d7ca91be3856c9eaf3b7daecbfd80bff53fbd36c20c830dcb64e1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887606"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a>\_Propriedade MFPKEY WMADRC \_ AVGTARGET

Especifica o nível de volume médio desejado de conteúdo de áudio de saída.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMADRCAverageTarget

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

Consulte Observações.

## <a name="remarks"></a>Comentários

Você pode definir esse valor no decodificador para a finalidade do controle de intervalo dinâmico, mas terá efeito somente se a propriedade [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) for definida.

> [!Note]  
> Não é recomendável definir o valor de destino médio. O ajuste do valor médio não afeta a diferença entre sons altos e suaves. Em vez disso, ele corta ou aumenta o volume médio geral que pode causar distorção indesejável durante a reprodução.

 

Se você solicitar o controle de intervalo dinâmico do decodificador quando essa propriedade não for definida, o codec calculará um valor padrão.

Use as propriedades [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) e [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) para calcular os valores apropriados para essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




