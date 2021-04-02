---
description: Especifica a qualidade da saída.
ms.assetid: 7b45633b-7f1c-4951-a462-ad6240b9ca31
title: Propriedade MFPKEY_WMRESAMP_FILTERQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4027d4bc3c0306240986cf632e171fa9a59ed18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164918"
---
# <a name="mfpkey_wmresamp_filterquality-property"></a>\_Propriedade MFPKEY WMRESAMP \_ FILTERQUALITY

Especifica a qualidade da saída.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="applies-to"></a>Aplica-se A

-   [DSP de reamostragem de áudio](audioresampler.md)

## <a name="remarks"></a>Comentários

O intervalo válido dessa propriedade é de 1 a 60, inclusive. Valores mais altos produzem saída de qualidade mais alta, mas apresentam mais latência. Um valor de 1 é essencialmente o mesmo que a interpolação linear.

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

 

 
