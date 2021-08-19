---
description: Especifica se o codificador usa a codificação de VBR média controlável.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: Propriedade MFPKEY_AVGCONSTRAINED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e7231cb3807be8f4467592ac0138a75ea277bdf8a13dfb3564d3572036e7ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874073"
---
# <a name="mfpkey_avgconstrained-property"></a>\_Propriedade MFPKEY AVGCONSTRAINED

Especifica se o codificador usa a codificação de VBR média controlável.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**BOOL do VT \_**

## <a name="default-value"></a>Valor padrão

**VARIANTE \_ falso**

## <a name="remarks"></a>Comentários

Se essa propriedade e a propriedade [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) forem definidas como **Variant \_ true**, o codificador usará a codificação de VBR média controlável. Nesse caso, o codificador se configura de acordo com os valores de [**MFPKEY \_ dyn \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) e [**MFPKEY \_ dyn \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
