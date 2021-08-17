---
description: Especifica uma altura intermediária de quadro para vídeo codificado.
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: Propriedade MFPKEY_FORCEFRAMEHEIGHT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6e3d423fe96173829b31a889764d5423db88b5c882d853b3e0f770d17dd4691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463446"
---
# <a name="mfpkey_forceframeheight-property"></a>\_Propriedade MFPKEY FORCEFRAMEHEIGHT

Especifica uma altura intermediária de quadro para vídeo codificado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCForceFrameHeight

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="remarks"></a>Comentários

Você pode definir esse valor e a propriedade [MFPKEY \_ FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md) para forçar o codificador a codificar o fluxo de vídeo com um tamanho de quadro menor do que os tamanhos de quadro de entrada ou de saída. Quando decodificado, o vídeo será redimensionado para sua resolução de entrada original.

As dimensões de quadro válidas em qualquer eixo são de 2 a 8192 pixels. As dimensões do quadro devem ser divisíveis por 2.

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

 

 




