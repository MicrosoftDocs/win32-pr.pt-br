---
description: Especifica a janela de buffer, em milissegundos, para um codificador configurado para usar a codificação de VBR média controlável.
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: Propriedade MFPKEY_DYN_VBR_BAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e117c2852f660b015bcdd95224178730d2e2a1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751508"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a>\_Propriedade MFPKEY dyn \_ VBR \_ BAVG

Especifica a janela de buffer, em milissegundos, para um codificador configurado para usar a codificação de VBR média controlável.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**\_I4 VT**

## <a name="remarks"></a>Comentários

Se as propriedades [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) e [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) estiverem definidas como **Variant \_ true**, o codificador usará a codificação de taxa de bits média controlável. Nesse caso, o codificador se configura de acordo com o valor dessa propriedade e a propriedade [**MFPKEY \_ dyn \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md) .

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

 

 
