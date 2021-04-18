---
description: Especifica a taxa média de bits, em bits por segundo, usada para codificação de 2 passagens, taxa de bits variável (VBR).
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: Propriedade MFPKEY_RAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad15d2445dc2acea1e91f4d01fad6e7bd83edb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791503"
---
# <a name="mfpkey_ravg-property"></a>\_Propriedade MFPKEY RAVG

Especifica a taxa média de bits, em bits por segundo, usada para codificação de 2 passagens, taxa de bits variável (VBR).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCAvgBitrate

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="remarks"></a>Comentários

Em uma VBR restrita e irrestrita, esse valor é a taxa média de bits na duração do conteúdo.

Você deve definir esse valor para ambos os modos de codificação de VBR de duas passagens. Depois de começar a processar amostras, você não deve consultar esse valor até concluir a codificação do fluxo. O codificador interpreta uma solicitação para esse valor como um sinal de que a sessão de codificação está acima; o próximo exemplo que você processa é tratado como o início de uma nova sessão.

Essa propriedade também pode ser lida no final de uma sessão de codificação de VBR de 1 passagem.

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

 

 




