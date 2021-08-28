---
description: Especifica o número de quadros após o quadro atual que o codec avaliará antes de codificar o quadro atual.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: Propriedade MFPKEY_LOOKAHEAD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa5b11abbacc19a4a66dda785d628b1f5d67f636a0f02c7392402ad64a7c3926
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113326"
---
# <a name="mfpkey_lookahead-property"></a>\_Propriedade LOOKAHEAD de MFPKEY

Especifica o número de quadros após o quadro atual que o codec avaliará antes de codificar o quadro atual.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCLookAhead

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

Quando o codec usa antecipadamente, ele pode codificar o vídeo com mais eficiência.

o objeto do gravador do SDK do formato de mídia Windows espera que o codec codifique cada exemplo imediatamente. como resultado, esse recurso não funciona corretamente no software que usa o objeto do gravador (incluindo Windows Media Encoder e Windows Media Player). Todas as extensões de unidade de dados associadas a quadros de vídeo serão anexadas ao quadro de saída errado. O número de quadros pelos quais as extensões de unidade de dados são colocadas incorretas é igual ao número de quadros de antecipação que são usados.

Os valores de lookahead válidos variam de 0 a 16 quadros. O valor recomendado é 16.

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

 

 




