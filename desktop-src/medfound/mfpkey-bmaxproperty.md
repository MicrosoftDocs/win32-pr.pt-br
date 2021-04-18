---
description: Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa de bits de pico (especificada por MFPKEY \_ RMAX).
ms.assetid: ef27b179-4d9b-4ce7-867a-f62b0f9b735d
title: Propriedade MFPKEY_BMAX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaca172e97c27e6e8d97902fbe3c969efc933eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811532"
---
# <a name="mfpkey_bmax-property"></a>\_Propriedade MFPKEY BMAX

Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits variável restrita (VBR) em sua taxa de bits de pico (especificada por [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCBMax

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

Sem padrão.

## <a name="remarks"></a>Comentários

Você deve definir esse valor para a codificação de taxa de bits de pico restrita. Depois de começar a processar amostras, você não deve consultar esse valor até concluir a codificação do fluxo. O codec interpreta uma solicitação para esse valor como um sinal de que a sessão de codificação está acima; o próximo exemplo que você processa é tratado como o início de uma nova sessão.

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

 

 




