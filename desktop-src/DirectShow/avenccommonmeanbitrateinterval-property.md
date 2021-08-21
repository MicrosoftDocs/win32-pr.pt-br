---
description: Especifica o intervalo de tempo durante o qual a taxa de bits média se aplica. Essa propriedade é usada em conjunto com a propriedade AVEncCommonMeanBitRate.
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: Propriedade AVEncCommonMeanBitRateInterval (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5cbd463ea67e281183dccde937f16978634e4103670b0e82b90b96139da5296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159788"
---
# <a name="avenccommonmeanbitrateinterval-property"></a>Propriedade AVEncCommonMeanBitRateInterval

Especifica o intervalo de tempo durante o qual a taxa de bits média se aplica. Essa propriedade é usada em conjunto com a propriedade [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) .

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonMeanBitRateInterval**

## <a name="property-value"></a>Valor da propriedade

Esta propriedade tem um intervalo linear de valores. Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Comentários

Para a codificação de taxa de bits variável (VBR) de duas passagens, o valor zero indica que o intervalo de tempo é a duração total do conteúdo. Para a codificação de taxa de bits constante de passagem única (CBR), o valor zero indica que o codificador seleciona o intervalo (normalmente 0,5 segundos).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | aplicativos Windows 2000 Professional \[ desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows \[ aplicativos da área de trabalho do servidor 2000 \| aplicativo UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




