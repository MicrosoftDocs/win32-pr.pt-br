---
description: Especifica o intervalo usado em pesquisas de movimento.
ms.assetid: b2026f47-ac39-4276-8359-c939b202f00c
title: Propriedade MFPKEY_MOTIONSEARCHRANGE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c557ea1a462192434222e425dccb8b9a0e291986
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165386"
---
# <a name="mfpkey_motionsearchrange-property"></a>\_Propriedade MFPKEY MOTIONSEARCHRANGE

Especifica o intervalo usado em pesquisas de movimento.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMotionSearchRange

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

Essa propriedade pode ser definida como um dos valores a seguir. H denota intervalo horizontal e V denota intervalo vertical. Todos os intervalos são fornecidos em pixels.



| Valor | Intervalo                                |
|-------|--------------------------------------|
| 0     | + 63.75/-64.0 H, + 31.75/-32.0 V       |
| 1     | +127,75/-128 H, +63,75/-64 V     |
| 2     | + 511.75/-512.0 H, + 127.75/-128.0 V   |
| 3     | + 1023.75/-1024.0 H, + 255.75/-256.0 V |
| -1    | Macrobloco-adaptável (automático)      |



 

Essa propriedade controla o tamanho da área do quadro em que o codec pesquisará um elemento que pode ter exibido o movimento entre os quadros. Uma janela de pesquisa maior ajudará a encontrar um movimento mais rápido, mas exigirá mais tempo de CPU. Os requisitos de CPU são aproximadamente dobrados em cada nível.

O modo automático (-1) selecionará dinamicamente o modo mais eficiente.

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

 

 




