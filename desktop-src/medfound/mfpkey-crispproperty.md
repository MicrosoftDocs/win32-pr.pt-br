---
description: Especifica uma representação numérica da compensação entre a suavidade de movimento e a qualidade da imagem da saída do codec.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: Propriedade MFPKEY_CRISP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ff20b37bcedf3995ec3e16178b823c40b352ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661878"
---
# <a name="mfpkey_crisp-property"></a>\_Propriedade MFPKEY Crisp

Especifica uma representação numérica da compensação entre a suavidade de movimento e a qualidade da imagem da saída do codec.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCCrisp

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

75

## <a name="remarks"></a>Comentários

Esse valor inteiro pode variar de 0 a 100. Quanto maior o valor, mais o codec otimizará a codificação para a qualidade da imagem de quadros individuais, o que geralmente reduz a suavidade do movimento.

Essa propriedade deve ser definida somente para a codificação de taxa de bits constante (CBR). As otimizações para a codificação de taxa de bits variável (VBR) funcionam de forma diferente.

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

 

 




