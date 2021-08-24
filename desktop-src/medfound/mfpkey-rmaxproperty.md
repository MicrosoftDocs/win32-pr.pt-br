---
description: Especifica a taxa de bits de pico, em bits por segundo, usada para reprodução restrita de VBR (taxa de bits variável de 2 pass).
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: MFPKEY_RMAX propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e80f679d0ed1213a54a4f22bc5d8bfc79f41b93fa05c446c8b6ed0f589183b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398396"
---
# <a name="mfpkey_rmax-property"></a>Propriedade MFPKEY \_ RMAX

Especifica a taxa de bits de pico, em bits por segundo, usada para reprodução restrita de VBR (taxa de bits variável de 2 pass).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMaxBitrate

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="default-value"></a>Valor padrão

Sem padrão.

## <a name="remarks"></a>Comentários

Esse valor representa a taxa de bits de pico para reprodução. O valor de [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) é usado para descrever o buffer em termos dessa taxa de bits; na verdade, a VBR restrita é semelhante à CBR (taxa de bits constante) usando esse valor como a taxa de bits. No entanto, um fluxo de VBR restrito pode ser tocado de volta a uma taxa de bits menor, desde que o buffer seja aumentado.

Você deve definir esse valor para codificação VBR de duas passs com restrição de pico. Depois de começar a processar exemplos, você não deve consultar esse valor até terminar a codificação do fluxo. O codificador interpreta uma solicitação para esse valor como um sinal de que a sessão de codificação terminou; o próximo exemplo que você processa é tratado como o início de uma nova sessão.

Normalmente, esse valor é de duas a três vezes maior que o valor [de MFPKEY \_ LTDG.](mfpkey-ravgproperty.md)

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

 

 




