---
description: Especifica se o codificador principal usa o &\# 0034; Mais&\# 0034; recurso.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: Propriedade MFPKEY_ENHANCED_WMA (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1c7ddc0e7bfb6d62d51e535f10b257eac6f2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752388"
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

Essa propriedade está disponível somente para o Windows Media Audio sem perdas.

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

 

 
