---
description: Especifica o número de quadros de previsão bidirecionais (quadros B).
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: Propriedade MFPKEY_NUMBFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfcf103da1d629c90209aef4badd604651d73af3e9101cac0f613b47c82883e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555412"
---
# <a name="mfpkey_numbframes-property"></a>\_Propriedade MFPKEY NUMBFRAMES

Especifica o número de quadros de previsão bidirecionais (quadros B).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCNumBFrames

## <a name="data-type"></a>Tipo de Dados

VT-I4

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

por padrão, Windows vídeo de mídia 9 usa apenas intraframes (I-frames), também conhecido como quadros-chave ou quadros de ancoragem, que são quadros totalmente codificados e quadros de previsão (quadros P), que são codificados como uma diferença do I-frame anterior. Os quadros B são diferentes dos quadros P porque armazenam as diferenças do quadro anterior e as diferenças do quadro a seguir.

Quando você configura o codec para usar os quadros B, ele usará o número especificado de quadros B entre cada par de quadros do tipo I ou P.

Por exemplo, se uma sequência de quadros sem quadros B for "IPPPPPPPPI", a mesma codificação de sequência com dois quadros B seria "IBBPBBPBBI".

Para a maior parte do conteúdo, um ou dois quadros B são apropriados. Em taxas de dados mais altas, um quadro B normalmente é a melhor opção. Três ou mais raramente são úteis.

O intervalo válido de valores para essa propriedade é de 0 a 7.

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

 

 




