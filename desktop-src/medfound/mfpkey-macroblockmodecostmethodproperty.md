---
description: Especifica o método de custo usado pelo codec para determinar qual modo de macrobloco usar.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: Propriedade MFPKEY_MACROBLOCKMODECOSTMETHOD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289219300a79c67565891c48cec848851c17bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761015"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a>\_Propriedade MFPKEY MACROBLOCKMODECOSTMETHOD

Especifica o método de custo usado pelo codec para determinar qual modo de macrobloco usar.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMacroblockModeCostMethod

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

Essa propriedade pode ser definida como um dos valores a seguir.



| Valor | Método usado                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| 0     | TRISTE/Hadamard. Esta opção configura o codec para usar apenas distorção ao calcular o custo.             |
| 1     | Custo da área de trabalho remota. Esta opção configura o codec para considerar a taxa e a distorção ao calcular o custo. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MFPKEY \_ MOTIONMATCHMETHOD](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




