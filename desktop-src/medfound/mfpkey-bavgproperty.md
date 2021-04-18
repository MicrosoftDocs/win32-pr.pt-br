---
description: Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits de variável restrita (VBR) em sua taxa de bits média (especificada por MFPKEY \_ RAVG).
ms.assetid: 7eabceb5-976e-4ebc-9042-9c203044634c
title: Propriedade MFPKEY_BAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cc9984b803fc37c84fee032f95098c52a9b47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781616"
---
# <a name="mfpkey_bavg-property"></a>\_Propriedade MFPKEY BAVG

Especifica a janela de buffer, em milissegundos, de um fluxo de taxa de bits de variável restrita (VBR) em sua taxa de bits média (especificada por [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCBAvg

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

Nenhum valor padrão, mas o codec calculará um valor apropriado com base nas outras configurações de taxa de bits restritas.

## <a name="remarks"></a>Comentários

Esse valor é calculado pelo codec após a passagem da codificação final. Você não deve consultar esse valor até que a codificação seja concluída. O codec interpreta uma solicitação para esse valor como um sinal de que a sessão de codificação está acima; o próximo exemplo que você processa é tratado como o início de uma nova sessão.

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

 

 




