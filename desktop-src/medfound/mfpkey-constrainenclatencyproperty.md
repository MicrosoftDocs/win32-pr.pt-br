---
description: Especifica se o codificador é restrito por um requisito máximo de latência.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: MFPKEY_CONSTRAINENCLATENCY propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172b92b0b4d39602f0535b8bf1ef4456a896972e56c6da10f6585e5221fa7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113416"
---
# <a name="mfpkey_constrainenclatency-property"></a>Propriedade MFPKEY \_ CONSTRAINENCLATENCY

Especifica se o codificador é restrito por um requisito máximo de latência.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

**BOOL da VT \_**

## <a name="default-value"></a>Valor padrão

**VARIANT \_ FALSE**

## <a name="remarks"></a>Comentários

Se você deixar essa propriedade com seu valor padrão **de VARIANT \_ FALSE**, o codificador enumera um conjunto padrão de modos que têm cerca de 2.000 milissegundos de latência do codificador. Se você definir essa propriedade como **VARIANT \_ TRUE,** também deverá especificar uma latência máxima do codificador definindo a propriedade [**MFPKEY \_ MAXENCLATENCYMS.**](mfpkey-maxenclatencymsproperty.md) Nesse caso, o codificador cria modos que atendem ao requisito de latência e enumera apenas esses modos. O codificador garante um exemplo de saída assim que o codificador tiver recebido entrada por um período igual a **MFPKEY \_ MAXENCLATENCYMS**.

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

 

 
