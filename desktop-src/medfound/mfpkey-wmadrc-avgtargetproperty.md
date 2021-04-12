---
description: Especifica o nível de volume médio desejado de conteúdo de áudio de saída.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: Propriedade MFPKEY_WMADRC_AVGTARGET (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4503161ac6e392a50fd7535592b84ea92d6136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165299"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




