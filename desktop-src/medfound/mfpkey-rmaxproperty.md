---
description: Especifica a taxa de bits de pico, em bits por segundo, usada para reprodução de taxa de bits de variável (VBR) restrita de 2 passagens.
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: Propriedade MFPKEY_RMAX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3568e0a3ee506640200413a5dc222c7cccec2215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165360"
---
# <a name="mfpkey_rmax-property"></a>\_Propriedade MFPKEY RMAX

Especifica a taxa de bits de pico, em bits por segundo, usada para reprodução de taxa de bits de variável (VBR) restrita de 2 passagens.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMaxBitrate

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

Sem padrão.

## <a name="remarks"></a>Comentários

Esse valor representa a taxa de bits de pico para reprodução. O valor de [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) é usado para descrever o buffer em termos dessa taxa de bits; na verdade, a VBR restrita é semelhante à taxa de bits constante (CBR) usando esse valor como a taxa de bits. No entanto, um fluxo de VBR restrito pode ser reproduzido em uma taxa de bits inferior, desde que o buffer seja aumentado.

Você deve definir esse valor para codificação de VBR de duas passagens de pico restrita. Depois de começar a processar amostras, você não deve consultar esse valor até concluir a codificação do fluxo. O codificador interpreta uma solicitação para esse valor como um sinal de que a sessão de codificação está acima; o próximo exemplo que você processa é tratado como o início de uma nova sessão.

Normalmente, esse valor é de duas a três vezes maior que o valor de [MFPKEY \_ RAVG](mfpkey-ravgproperty.md).

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

 

 




