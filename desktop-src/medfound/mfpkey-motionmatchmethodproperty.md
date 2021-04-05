---
description: Especifica o método a ser usado para a correspondência de movimento.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: Propriedade MFPKEY_MOTIONMATCHMETHOD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09496e714633dd394f55122b7461f29a2daa3656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921397"
---
# <a name="mfpkey_motionmatchmethod-property"></a>\_Propriedade MFPKEY MOTIONMATCHMETHOD

Especifica o método a ser usado para a correspondência de movimento.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMotionMatchMethod

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

Essa propriedade pode ser definida como um dos valores a seguir.



| Valor | Método usado                       |
|-------|-----------------------------------|
| 0     | soma de diferenças absolutas (SAD) |
| 1     | Hadamard                          |
| -1    | Macrobloco.              |



 

A soma das diferenças absolutas (triste) é um método mais rápido, mas menos preciso do que a transformação Hadamard. A transformação Hadamard é mais precisa, mas computacionalmente intensiva. O modo adaptável macrobloco fornece um comprometimento razoável entre os dois métodos, escolhendo dinamicamente entre as duas transformações, selecionando a transformação Hadamard somente quando apropriado.

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

 

 




