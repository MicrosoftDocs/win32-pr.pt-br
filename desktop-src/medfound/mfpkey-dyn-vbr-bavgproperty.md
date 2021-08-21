---
description: Especifica a janela de buffer, em milissegundos, para um codificador configurado para usar a codificação VBR de controle médio.
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: MFPKEY_DYN_VBR_BAVG propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77ba4d3f3d7a5587a7c8aa90771f58accd8a80864dd5a875c6c580eb9e29e01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738156"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a>Propriedade \_ \_ BAVG de VBR de DYN MFPKEY \_

Especifica a janela de buffer, em milissegundos, para um codificador configurado para usar a codificação VBR de controle médio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

**VT \_ I4**

## <a name="remarks"></a>Comentários

Se as propriedades [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) e [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) estão definidas como **VARIANT \_ TRUE,** o codificador usará a codificação VBR com controle médio. Nesse caso, o codificador configura-se de acordo com o valor dessa propriedade e a propriedade [**MFPKEY \_ DYN \_ VBR \_ LTDG.**](mfpkey-dyn-vbr-ravgproperty.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
