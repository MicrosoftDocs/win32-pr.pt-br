---
description: Especifica se os modos enumerados pelo codificador são Limeted àqueles que atendem a um requisito de qualidade fornecido pelo \_ VBRQUALITY desejado do MFPKEY \_ .
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: Propriedade MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761003"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a>MFPKEY \_ restringir a \_ \_ Propriedade VBRQUALITY enumerada

Especifica se os modos enumerados pelo codificador são Limeted àqueles que atendem a um requisito de qualidade fornecido pelo [**\_ \_ VBRQUALITY desejado do MFPKEY**](mfpkey-desired-vbrqualityproperty.md).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**BOOL do VT \_**

## <a name="default-value"></a>Valor padrão

**VARIANTE \_ falso**

## <a name="remarks"></a>Comentários

Para enumerar modos de VBR que atendam a um determinado requisito de qualidade, defina as propriedades do codificador a seguir.

-   Defina [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) como **Variant \_ true**.
-   Defina **MFPKEY \_ restringir \_ enumerated \_ VBRQUALITY** para **Variant \_ true**.
-   Defina [**MFPKEY \_ desired \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) para a qualidade desejada. Para modos sem perdas, defina a qualidade desejada como 100.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista ou Windows 7<br/>                                                   |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
