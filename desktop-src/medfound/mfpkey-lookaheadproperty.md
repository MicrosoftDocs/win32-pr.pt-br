---
description: Especifica o número de quadros após o quadro atual que o codec avaliará antes de codificar o quadro atual.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: Propriedade MFPKEY_LOOKAHEAD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a024c4d0be6ef7ab16c4bf51f290b01de3282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761016"
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

O objeto gravador do SDK do Windows Media Format espera que o codec codifique cada exemplo imediatamente. Como resultado, esse recurso não funciona corretamente no software que usa o objeto do gravador (incluindo o Windows Media Encoder e o Windows Media Player). Todas as extensões de unidade de dados associadas a quadros de vídeo serão anexadas ao quadro de saída errado. O número de quadros pelos quais as extensões de unidade de dados são colocadas incorretas é igual ao número de quadros de antecipação que são usados.

Os valores de lookahead válidos variam de 0 a 16 quadros. O valor recomendado é 16.

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

 

 




