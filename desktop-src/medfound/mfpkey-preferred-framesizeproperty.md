---
description: Especifica o número preferencial de amostras por quadro.
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: Propriedade MFPKEY_PREFERRED_FRAMESIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe04ad37c6cd684e3179cbd16328346fd6f11dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770592"
---
# <a name="mfpkey_preferred_framesize-property"></a>\_ \_ Propriedade frameize de MFPKEY preferencial

Especifica o número preferencial de amostras por quadro.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**\_UI4 VT**

## <a name="remarks"></a>Comentários

Para especificar um tamanho de quadro preferencial, defina as propriedades a seguir.

-   Defina [**MFPKEY \_ solicitando \_ um \_ frameize**](mfpkey-requesting-a-framesizeproperty.md) como **Variant \_ true**.
-   Defina **MFPKEY \_ de \_ quadros preferenciais** para o número de amostras desejado em cada quadro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista ou Windows 7<br/>                                                   |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
