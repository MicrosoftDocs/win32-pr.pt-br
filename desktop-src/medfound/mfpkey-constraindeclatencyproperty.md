---
description: Especifica se o codificador é restrito por um requisito de latência de decodificador máximo.
ms.assetid: 054e445e-fc71-4d4f-9e9f-f5ff71f0b4ee
title: Propriedade MFPKEY_CONSTRAINDECLATENCY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343bcc9bd365b9f1321b200baa203fc27784594c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790501"
---
# <a name="mfpkey_constraindeclatency-property"></a>\_Propriedade MFPKEY CONSTRAINDECLATENCY

Especifica se o codificador é restrito por um requisito de latência de decodificador máximo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**BOOL do VT \_**

## <a name="default-value"></a>Valor padrão

**VARIANTE \_ falso**

## <a name="remarks"></a>Comentários

Se você deixar essa propriedade com seu valor padrão de **variante \_ false**, o codificador enumerará um conjunto padrão de modos que têm cerca de 1500 milissegundos de latência de decodificador. Se você definir essa propriedade como **Variant \_ true**, também deverá especificar uma latência máxima de decodificador definindo a propriedade [**MFPKEY \_ MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) . Nesse caso, o codificador cria modos que atendem ao requisito de latência e enumera apenas esses modos. O codificador garante que os requisitos de preroll (tamanho do buffer do decodificador) sejam menores ou iguais a **MFPKEY \_ MAXDECLATENCYMS**.

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

 

 
