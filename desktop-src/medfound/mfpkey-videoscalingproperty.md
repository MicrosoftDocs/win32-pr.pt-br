---
description: Especifica se o codec usará a otimização de escala de vídeo.
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: Propriedade MFPKEY_VIDEOSCALING (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2dc069d70b167dd8da6cb308d70149aec1028f3aaf4e50b5c1cc8ab11104c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887646"
---
# <a name="mfpkey_videoscaling-property"></a>\_Propriedade MFPKEY VIDEOSCALING

Especifica se o codec usará a otimização de escala de vídeo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCVideoScaling

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

O dimensionamento de vídeo é um tipo de otimização perceptiva que pode melhorar a qualidade visual do vídeo codificado em taxas de bits baixas. A otimização de escala de vídeo reduz os artefatos pronunciados, mas pode sacrificar os detalhes da imagem. Essa otimização afeta o intervalo Luma do vídeo codificado conforme descrito abaixo, mas não afeta a resolução física do vídeo de saída.

Essa propriedade pode ser definida como um dos valores a seguir.



| Valor | Descrição                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| 0     | O dimensionamento de vídeo não será usado.                                                                                       |
| 1     | O codificador usará otimização de escala de vídeo conservadora. O intervalo de Luma será dimensionado de 0... 255 para 26... 229. |
| 2     | O codificador usará otimização agressiva de escala de vídeo. O intervalo de Luma será dimensionado de 0... 255 para 31... 224.   |



 

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

 

 




