---
description: Especifica se o codificador deve usar um tamanho de quadro preferencial fornecido no número de amostras por quadro.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: Propriedade MFPKEY_REQUESTING_A_FRAMESIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c39d1d9ecdba27e46a1e49949f1607fc60d53501d321e49c4899f9b8928ccf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555426"
---
# <a name="mfpkey_requesting_a_framesize-property"></a>MFPKEY \_ solicitando \_ uma \_ Propriedade frameize

Especifica se o codificador deve usar um tamanho de quadro preferencial fornecido no número de amostras por quadro.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**BOOL do VT \_**

## <a name="remarks"></a>Comentários

Para especificar um tamanho de quadro preferencial, defina as propriedades a seguir.

-   Defina **MFPKEY \_ solicitando \_ um \_ frameize** como Variant \_ true.
-   Defina [**MFPKEY \_ de \_ quadros preferenciais**](mfpkey-preferred-framesizeproperty.md) para o número de amostras desejado em cada quadro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista ou Windows 7<br/>                                                   |
| Cabeçalho<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
