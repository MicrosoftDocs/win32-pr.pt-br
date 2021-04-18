---
description: Especifica se o codificador deve usar um tamanho de quadro preferencial fornecido no número de amostras por quadro.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: Propriedade MFPKEY_REQUESTING_A_FRAMESIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3355e84318ba4ad7995ac5ad0f002f4d70767b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760531"
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
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
