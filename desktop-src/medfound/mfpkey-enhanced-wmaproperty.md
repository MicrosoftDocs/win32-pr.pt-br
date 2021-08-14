---
description: Especifica se o codificador principal usa o &\# 0034; Mais&\# 0034; recurso.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: Propriedade MFPKEY_ENHANCED_WMA (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab3fdcd3087773ea760615224b148bd497c1f89114c0f761a7d2f90fb0b5a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738013"
---
# <a name="mfpkey_enhanced_wma-property"></a>\_Propriedade WMA MFPKEY Enhanced \_

Especifica se o codificador principal usa o recurso "Plus".

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**\_UI4 VT**

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

essa propriedade só está disponível para Windows sem perdas de áudio de mídia.

Se você deixar essa propriedade com seu valor padrão de 0 ou se defini-la como 1, o codificador principal decidirá se a parte "Plus" deve ser usada. Se você definir essa propriedade como 2, o codificador principal não usará o recurso "Plus".

Essa propriedade altera os tipos de mídia enumerados, portanto, se você defini-lo, deverá fazê-lo antes de definir o tipo de saída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista ou Windows 7<br/>                                                   |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
