---
description: Especifica a taxa média de bits, em bits por segundo, para um codificador configurado para usar a codificação de VBR média controlável.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: Propriedade MFPKEY_DYN_VBR_RAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8103d36db5a9e946449231943e076c26258eec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921401"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a>\_Propriedade MFPKEY dyn \_ VBR \_ RAVG

Especifica a taxa média de bits, em bits por segundo, para um codificador configurado para usar a codificação de VBR média controlável.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**\_I4 VT**

## <a name="remarks"></a>Comentários

Se as propriedades [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) e [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) estiverem definidas como **Variant \_ true**, o codificador usará a codificação de taxa de bits média controlável. Nesse caso, o codificador se configura de acordo com o valor dessa propriedade e a propriedade [**MFPKEY \_ dyn \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
