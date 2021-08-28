---
description: Especifica a taxa média de bits, em bits por segundo, usada para codificação VBR (taxa de bits variável) de duas passes.
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: MFPKEY_RAVG propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90fd5435498a8a0c247d9363f02e2e767b46c5ab17ce36cc5a41feab54ed5277
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113286"
---
# <a name="mfpkey_ravg-property"></a>Propriedade MFPKEY \_ LTDG

Especifica a taxa média de bits, em bits por segundo, usada para codificação VBR (taxa de bits variável) de duas passes.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCAvgBitrate

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="remarks"></a>Comentários

No VBR restrito e irr pouco restrito, esse valor é a taxa média de bits durante a duração do conteúdo.

Você deve definir esse valor para ambos os modos de codificação VBR de duas passões. Depois de começar a processar exemplos, você não deve consultar esse valor até terminar a codificação do fluxo. O codificador interpreta uma solicitação para esse valor como um sinal de que a sessão de codificação terminou; o próximo exemplo que você processa é tratado como o início de uma nova sessão.

Essa propriedade também pode ser lida no final de uma sessão de codificação VBR de 1 passagem.

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

 

 




