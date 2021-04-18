---
description: Especifica se o codificador é restrito por um requisito de latência máxima.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: Propriedade MFPKEY_CONSTRAINENCLATENCY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f880006bf2aba04196547a79e74f94a7210edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810700"
---
# <a name="mfpkey_constrainenclatency-property"></a>\_Propriedade MFPKEY CONSTRAINENCLATENCY

Especifica se o codificador é restrito por um requisito de latência máxima.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**BOOL do VT \_**

## <a name="default-value"></a>Valor padrão

**VARIANTE \_ falso**

## <a name="remarks"></a>Comentários

Se você deixar essa propriedade com o valor padrão de **Variant \_ false**, o codificador enumerará um conjunto padrão de modos que têm cerca de 2000 milissegundos de latência do codificador. Se você definir essa propriedade como **Variant \_ true**, também deverá especificar uma latência máxima do codificador definindo a propriedade [**MFPKEY \_ MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) . Nesse caso, o codificador cria modos que atendem ao requisito de latência e enumera apenas esses modos. O codificador garante um exemplo de saída assim que o codificador recebeu entrada para um período de tempo igual a **MFPKEY \_ MAXENCLATENCYMS**.

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

 

 
