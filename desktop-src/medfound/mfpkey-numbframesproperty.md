---
description: Especifica o número de quadros de previsão bidirecionais (quadros B).
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: Propriedade MFPKEY_NUMBFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3b0655a4a5e24b92f9699b198f10232de8edf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748919"
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

Por padrão, o Windows Media Video 9 usa apenas intraframes (I-frames), também conhecido como quadros-chave ou quadros de ancoragem, que são quadros totalmente codificados e quadros de previsão (quadros P), que são codificados como uma diferença do I-frame anterior. Os quadros B são diferentes dos quadros P porque armazenam as diferenças do quadro anterior e as diferenças do quadro a seguir.

Quando você configura o codec para usar os quadros B, ele usará o número especificado de quadros B entre cada par de quadros do tipo I ou P.

Por exemplo, se uma sequência de quadros sem quadros B for "IPPPPPPPPI", a mesma codificação de sequência com dois quadros B seria "IBBPBBPBBI".

Para a maior parte do conteúdo, um ou dois quadros B são apropriados. Em taxas de dados mais altas, um quadro B normalmente é a melhor opção. Três ou mais raramente são úteis.

O intervalo válido de valores para essa propriedade é de 0 a 7.

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

 

 




