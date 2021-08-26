---
description: Especifica uma representação numérica da desvantagem entre a suavização de movimento e a qualidade da imagem da saída do codec.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: MFPKEY_CRISP propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 177ae5e9d1c8a9aba359000e04483c8e45c44f823c9db924155dd5ef3d5989a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954256"
---
# <a name="mfpkey_crisp-property"></a>Propriedade MFPKEY \_ CRISP

Especifica uma representação numérica da desvantagem entre a suavização de movimento e a qualidade da imagem da saída do codec.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCCrisp

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="default-value"></a>Valor padrão

75

## <a name="remarks"></a>Comentários

Esse valor inteiro pode variar de 0 a 100. Quanto maior o valor, mais o codec otimizará a codificação para a qualidade da imagem de quadros individuais, o que geralmente reduz a suavidade de movimento.

Essa propriedade deve ser definida somente para codificação CBR (taxa de bits constante). As otimizações para codificação VBR (taxa de bits variável) funcionam de maneira diferente.

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

 

 




