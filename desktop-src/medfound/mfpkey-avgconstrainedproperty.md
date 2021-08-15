---
description: Especifica se o codificador usa codificação VBR de controle médio.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: MFPKEY_AVGCONSTRAINED propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e7231cb3807be8f4467592ac0138a75ea277bdf8a13dfb3564d3572036e7ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874073"
---
# <a name="mfpkey_avgconstrained-property"></a>Propriedade MFPKEY \_ AVGCONSTRAINED

Especifica se o codificador usa codificação VBR de controle médio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

**BOOL da VT \_**

## <a name="default-value"></a>Valor padrão

**VARIANT \_ FALSE**

## <a name="remarks"></a>Comentários

Se essa propriedade e a [**propriedade \_ VBRENABLED MFPKEY**](mfpkey-vbrenabledproperty.md) são definidas como **VARIANT \_ TRUE,** o codificador usa a codificação VBR de controle médio. Nesse caso, o codificador se configura de acordo com os valores de [**MFPKEY \_ DYN \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) e [**MFPKEY \_ DYN \_ VBR \_ LTDG.**](mfpkey-dyn-vbr-ravgproperty.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
